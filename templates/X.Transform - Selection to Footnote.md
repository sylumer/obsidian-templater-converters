<%* /* Replace the selection with a footnote reference and append a matching footnote definition to the end of the note */ -%>
<%*
// Find the next available footnote number by scanning the note for existing [^n] markers
let arrMatches = [...tp.file.content.matchAll(/\[\^(\d+)\]/g)];
let intNextNum = arrMatches.length > 0 ? Math.max(...arrMatches.map(m => parseInt(m[1], 10))) + 1 : 1;

// If a single space immediately precedes the selection, pull it into the selection so it
// gets consumed by the marker replacement rather than left dangling in the note text
let objEditor = app.workspace.activeEditor.editor;
let objFrom = objEditor.getCursor("from");
let objTo = objEditor.getCursor("to");
if (objFrom.ch > 0 && objEditor.getRange({line: objFrom.line, ch: objFrom.ch - 1}, objFrom) === " ") {
	objEditor.setSelection({line: objFrom.line, ch: objFrom.ch - 1}, objTo);
}

// Capture the footnote text, having dropped any swallowed leading space
let strFootnoteText = tp.file.selection().trim();

// Append the footnote definition to the end of the note
await app.vault.append(app.workspace.getActiveFile(), `\n\n[^${intNextNum}]: ${strFootnoteText}`);

// Replace the (possibly extended) selection with the footnote reference marker
tR = `[^${intNextNum}]`;
%>