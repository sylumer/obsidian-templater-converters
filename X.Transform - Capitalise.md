<%* /* Transform the selected text to capitalise each word in the selected text */ -%>
<%* 
String.prototype.capitalise = function()
{
	return this.replace(/(?:^|\s|["'([{])+\S/g, strMatch => strMatch.toUpperCase());
};
tR = tp.file.selection().capitalise();
%>