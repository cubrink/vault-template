---
created: <% tp.date.now("YYYY-MM-DD") %>
tags:
  - wiki
---
# Introduction


# See Also


---
# In Progress

> [!attention]
> This page is #in-progress, the notes below represent potentially meaningful but incomplete content and thoughts

## Notes


---

<%*
const file_name = await tp.system.prompt("Enter Wiki Page Name");

// Handle if the user cancels
if (!file_name) {
	// This is invalid code
	// If templater crashes, the untitled file gets deleted
	// which is the desired behavior
	invalid_code_to_make_templater_crash.this.is.intentional;
	return;
}

// Check if file exists
const target_path = "wiki/" + file_name;
const existing_file = tp.file.find_tfile(target_path);

if (existing_file) {
	// File already exists
	// Open and and delete temp file
	new Notice("Wiki page already exists. Opening existing file...");
	await tp.app.workspace.getLeaf().openFile(existing_file);
	invalid_code_to_make_templater_crash.this.is.intentional;
	return;
}

// No duplicate - move to wiki directory
await tp.file.move(target_path);
%>