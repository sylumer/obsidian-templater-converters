<%* /* Sort selected lines in numeric order */ -%>
<%*
let astrLines = tp.file.selection().split('\n');
astrLines.sort(function(a, b){return a - b});
tR = astrLines.join('\n');
%>