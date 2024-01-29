<%* /* Add a period to the end of each line in the selection */ -%>
<% tp.file.selection().replaceAll(/(.*?)$/gmi, "$1.") %>