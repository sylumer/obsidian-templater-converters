<%* /* Transform the selected text to upper case inclusive of unicode normalisation (using NFC mode for canonical decomposition/composition) */ -%>
<% tp.file.selection().normalize().toUpperCase() %>