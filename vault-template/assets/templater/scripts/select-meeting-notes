<%*
// Find files with #meeting/recurring modified in last 6 months
const sixMonthsAgo = Date.now() - (6 * 30 * 24 * 60 * 60 * 1000);

const meetingFiles = app.vault.getMarkdownFiles()
    .filter(file => {
        // Check if modified recently
        if (file.stat.mtime < sixMonthsAgo) return false;
        
        // Check for tag
        const cache = app.metadataCache.getFileCache(file);
        return cache?.tags?.some(tag => tag.tag === "#meeting/recurring") ||
               cache?.frontmatter?.tags?.includes("meeting/recurring");
    });

if (meetingFiles.length === 0) {
    new Notice("No recent recurring meetings found");
    invalid_code_to_crash_templater.this.is.intentional;
    return;
}

// Prompt user to select
const choice = await tp.system.suggester(
    meetingFiles.map(f => f.basename),  // display names
    meetingFiles                         // return values
);

if (!choice) {
    // User cancelled
    invalid_code_to_crash_templater.this.is.intentional;
    return;
}

// Open selected file
await tp.app.workspace.getLeaf().openFile(choice);

// Delete temporary file
invalid_code_to_crash_templater.this.is.intentional;
%>
