<%* /* Sort selected lines in alphabetic order */ -%>
<%*
let astrLines = tp.file.selection().split('\n');
astrLines.sort((a, b) => a.localeCompare(b, undefined, {sensitivity: 'base'}));
tR = astrLines.join('\n');
%>