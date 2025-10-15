<%*
// Get the active editor and store cursor position 
const editor = app.workspace.activeEditor?.editor;
const cursorPos = editor?.getCursor();

// Get the current file content
const content = await app.vault.read(tp.file.find_tfile(tp.file.path(true)));

// Split content into lines
const lines = content.split('\n');

// Process sections
const result = [];
let currentSection = [];
let hasContent = false;
let sectionHeader = null;

for (let i = 0; i < lines.length; i++) {
    const line = lines[i];
    
    // Check if this is a header (starts with #)
    if (line.match(/^#{1,}\s/)) {
        // Process previous section
        if (sectionHeader !== null) {
            if (hasContent) {
                result.push(sectionHeader);
                result.push(...currentSection);
            }
        } else if (currentSection.length > 0) {
            // Content before first header
            result.push(...currentSection);
        }
        
        // Start new section
        sectionHeader = line;
        currentSection = [];
        hasContent = false;
    } else {
        // Add line to current section
        currentSection.push(line);
        
        // Check if line has actual content (not just whitespace or decorative horizontal rule)
        const trimmed = line.trim();
        if (trimmed.length > 0 && trimmed !== '---') {
            hasContent = true;
        }
    }
}

// Process final section
if (sectionHeader !== null) {
    if (hasContent) {
        result.push(sectionHeader);
        result.push(...currentSection);
    }
} else if (currentSection.length > 0) {
    // Content with no headers at all
    result.push(...currentSection);
}

// Join result and replace file content
const newContent = result.join('\n');

// Replace the entire file content
await app.vault.modify(tp.file.find_tfile(tp.file.path(true)), newContent);

// Restore cursor position after a brief delay to allow file reload 
if (editor && cursorPos) {
	setTimeout(() => {
		const activeEditor = app.workspace.activeEditor?.editor;
		if (activeEditor) {
			activeEditor.setCursor(cursorPos);
		}
	}, 50);
}

// Return empty string so nothing is inserted at cursor
tR = "";
_%>
