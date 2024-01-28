<%* /* Sort selected lines in reverse numeric order */ -%>
<%*
let astrLines = tp.file.selection().split('\n');
astrLines.sort(function(a, b){return b - a});
tR = astrLines.join('\n');
%>