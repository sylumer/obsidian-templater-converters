<%* /* Prefixes entered text to the start of each line in the selection */ -%>
<%*
strPrefix = await tp.system.prompt("Enter a prefix including any separator - e.g. a space", "", true, false);
tR = tp.file.selection().replaceAll(/^(.*)$/gmi, strPrefix + "$1");
%>
