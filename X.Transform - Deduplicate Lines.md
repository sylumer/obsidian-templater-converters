<%* /* Remove duplicate lines from selected text - the first occurrence remains */ -%>
<%* 
String.prototype.deduplicateLines = function()
{
	//Initialise arrays for lines of original and final contents
    let astrOriginal = this.split("\n");
    let astrDeduplicated = [];

    //Loop through all existing lines
    for (let intIndex = 0; intIndex < astrOriginal.length; intIndex++)
    {
        //When a line isn't already found in the new content, add it in
        if (astrDeduplicated.indexOf(astrOriginal[intIndex]) == -1)
        {
            astrDeduplicated.push(astrOriginal[intIndex]);
        }
    }

    //Return the deduplicated array as a string (no blank line at the end)
    return astrDeduplicated.join("\n");
}
tR = tp.file.selection().deduplicateLines();
%>