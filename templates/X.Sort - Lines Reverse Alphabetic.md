<%* /* Sort selected lines in reverse alphabetic order */ -%>
<%*
let astrLines = tp.file.selection().split('\n');
astrLines.sort((b, a) => a.localeCompare(b, undefined, {sensitivity: 'base'}));
tR = astrLines.join('\n');
%>