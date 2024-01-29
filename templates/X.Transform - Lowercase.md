<%* /* Transform the selected text to lower case inclusive of unicode normalisation (using NFC mode for canonical decomposition/composition) */ -%>
<% tp.file.selection().normalize().toLowerCase() %>