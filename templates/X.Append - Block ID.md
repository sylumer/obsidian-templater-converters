<%* /* Insert block ID and copy link */ -%>
<%*
function genRand()
{
	// Convert a random number to a character string
	return ("000" + (Math.random() * 46656) | 0).toString(36).slice(-3);
}

// Generate a short UID for section linking
let strLinkID = "^" + genRand() + genRand();

// Copy a section link to the clipboard
navigator.clipboard.writeText(`[[${tp.file.title}#${strLinkID}]]`);

// Insert the link ID
tR = tp.file.selection() + " " + strLinkID;
%>