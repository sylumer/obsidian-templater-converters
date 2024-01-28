<%* /* Appends entered text to the end of each line in the selection */ -%>
<%*
strSuffix = await tp.system.prompt("Enter a suffix including any separator - e.g. a space", "", true, false);
tR = tp.file.selection().replaceAll(/^(.*)$/gmi, "$1" + strSuffix);
%>