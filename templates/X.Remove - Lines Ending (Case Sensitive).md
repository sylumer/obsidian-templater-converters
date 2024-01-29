<%* /* Remove any line in the selection that ends with the specified text (case sensitive) */ -%>
<%*
strMatch = await tp.system.prompt("Remove lines starting with", "", true, false);
const re = new RegExp("\n?.*" + strMatch + "$", "gm");
tR = tp.file.selection().replace(re, "");
%>