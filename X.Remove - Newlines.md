<%* /* Removes newline characters to merge multiple lines into one contiguous line */ -%>
<% tp.file.selection().replaceAll(/\n/gi, "") %>