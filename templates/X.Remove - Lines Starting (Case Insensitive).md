<%* /* Remove any line in the selection that starts with the specified text (case insensitive) */ -%>
<%*
strMatch = await tp.system.prompt("Remove lines starting with", "", true, false);
const re = new RegExp("^" + strMatch + ".*(\n?)", "gmi");
tR = tp.file.selection().replace(re, "");
%>