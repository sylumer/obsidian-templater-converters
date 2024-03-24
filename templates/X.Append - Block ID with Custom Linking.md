<%* /* Insert block ID and copy link with options for customising the link content */ -%>
<%*
function genRand()
{
	// Convert a random number to a character string
	return ("000" + (Math.random() * 46656) | 0).toString(36).slice(-3);
}

// Generate a short UID for section linking and allow the user to customise
let strLinkID = genRand() + genRand();
strLinkID = await tp.system.prompt("Unique Section ID", strLinkID, true, false);
strLinkID = "^" + strLinkID;

// Copy a section link to the clipboard, taking a custom description if desired
let strLinkDescription = await tp.system.prompt("Link description (leave blank for none)", "", true, false);
if (strLinkDescription != "") strLinkDescription = "|" + strLinkDescription
navigator.clipboard.writeText(`[[${tp.file.title}#${strLinkID}${strLinkDescription}]]`);

// Insert the link ID
tR = tp.file.selection() + " " + strLinkID;
%>