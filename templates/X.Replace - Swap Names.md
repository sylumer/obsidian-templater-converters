<%* /* Swaps names in the format "surname, forename" to "forename surname" - useful for organisations where Outlook's address book lists people by surname, but you want a natural order to the names */ -%>
<% tp.file.selection().replaceAll(/(.*), (.*)/gi, "$2 $1") %>