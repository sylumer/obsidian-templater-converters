<%* /* Reduces multiple consecutive newline characters to a single newline character */ -%>
<% tp.file.selection().replaceAll(/(\n+)/gi, "\n") %>