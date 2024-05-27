<%* /* Remove diacritic characters */ -%>
<%  tp.file.selection().replace(/[a-zA-Z]/g, c => String.fromCharCode(c.charCodeAt(0) + (c.toLowerCase() < 'n' ? 13 : -13))) %>