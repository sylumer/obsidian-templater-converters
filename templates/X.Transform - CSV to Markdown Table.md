<%* /* Convert selected CSV/TSV lines into a Markdown table, treating the first line as the header row */ -%>
<%*
// Parse a single delimited line, respecting double-quoted fields (which may contain the
// delimiter itself, or an escaped "" quote), and strip the surrounding quotes
function parseDelimitedLine(strLine, strDelimiter) {
	let astrFields = [];
	let strField = "";
	let blnInQuotes = false;
	for (let i = 0; i < strLine.length; i++) {
		let strChar = strLine[i];
		if (blnInQuotes) {
			if (strChar === '"' && strLine[i + 1] === '"') {
				strField += '"';
				i++;
			} else if (strChar === '"') {
				blnInQuotes = false;
			} else {
				strField += strChar;
			}
		} else if (strChar === '"') {
			blnInQuotes = true;
		} else if (strChar === strDelimiter) {
			astrFields.push(strField);
			strField = "";
		} else {
			strField += strChar;
		}
	}
	astrFields.push(strField);
	// Trim whitespace and escape any pipe characters so they don't break the Markdown table
	return astrFields.map(strCell => strCell.trim().replaceAll("|", "\\|"));
}

let astrLines = tp.file.selection().split('\n').filter(strLine => strLine.trim() !== '');
let strDelimiter = astrLines[0].includes('\t') ? '\t' : ',';
let aastrRows = astrLines.map(strLine => parseDelimitedLine(strLine, strDelimiter));

let astrOutput = [];
astrOutput.push('| ' + aastrRows[0].join(' | ') + ' |');
astrOutput.push('| ' + aastrRows[0].map(() => '---').join(' | ') + ' |');
for (let i = 1; i < aastrRows.length; i++) {
	astrOutput.push('| ' + aastrRows[i].join(' | ') + ' |');
}

tR = astrOutput.join('\n');
%>