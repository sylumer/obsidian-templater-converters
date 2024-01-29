<%* /* Transform the selected text to sentence case inclusive of unicode normalisation (using NFC mode for canonical decomposition/composition) */ -%>
<%* 
String.prototype.toSentenceCase = function()
{
	return this.normalize().replace(/(^\w{1}|\.\s*\w{1})/gi, function(toReplace)
	{
		return toReplace.toUpperCase();
	});
}
tR = tp.file.selection().toSentenceCase();
%>