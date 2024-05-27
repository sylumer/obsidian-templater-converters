<%* /* Remove diacritic characters */ -%>
<% tp.file.selection().normalize("NFD").replace(/\p{Diacritic}/gu, "") %>