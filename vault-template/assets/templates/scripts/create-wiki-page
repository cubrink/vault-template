<%*
// 1. Prompt for the name
const fileName = await tp.system.prompt("Enter Wiki Page Name");

// Handle if user cancels
if (!fileName) {
	// This isn't real code
	// but if a parsing error occurs, templater deletes the 
	// in progress template, which is what we want.
	invalid_code_to_purposely_crash_templater.this.is.intentional
    return;
}

// 2. Check if file already exists
const targetPath = "wiki/" + fileName;
const existingFile = tp.file.find_tfile(targetPath);

if (existingFile) {
    // File already exists - open it and delete temp file
    new Notice("⚠️ Wiki page already exists! Opening existing file...");
    await tp.app.workspace.getLeaf().openFile(existingFile);
    invalid_code_to_crash_templater.this.is.intentional
    return;
}

// 3. No duplicate - move to wiki folder
await tp.file.move(targetPath);

// 4. Apply wiki template
const templateFile = tp.file.find_tfile("assets/templater/templates/wiki.md");
const templateContent = await app.vault.read(templateFile);
await app.vault.modify(tp.file.find_tfile(targetPath), templateContent);
%>
