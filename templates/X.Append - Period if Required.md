<%* /* Add a period to the end of each line in the selection where it does not already end in a period */ -%>
<% tp.file.selection().replaceAll(/\.$/mgi, "").replaceAll(/^(.*?)$/mgi, "$1.") %>