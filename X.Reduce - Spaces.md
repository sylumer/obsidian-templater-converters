<%* /* Reduces multiple consecutive space characters to a single space character */ -%>
<% tp.file.selection().replaceAll(/( +)/gi, " ") %>