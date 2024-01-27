<%* /* Replaces the bullet character with a hyphen - useful for converting copied bullets to Markdown */ -%>
<% tp.file.selection().replaceAll("•", "-") %>