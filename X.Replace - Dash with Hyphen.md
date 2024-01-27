<%* /* Replaces en dashes and em dashes with hyphens */ -%>
<% tp.file.selection().replaceAll(/–|—/gi, "-") %>