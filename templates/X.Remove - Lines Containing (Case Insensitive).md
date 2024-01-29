<%* /* Remove any line in the selection that contains the specified text (case insensitive) */ -%>
<%*
strMatch = await tp.system.prompt("Remove lines containing", "", true, false);
const re = new RegExp("^.*" + strMatch + ".*$\n?", "gmi");
tR = tp.file.selection().replace(re, "");
%>