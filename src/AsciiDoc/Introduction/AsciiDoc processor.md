1. Parses the document
	1. Normalize the document (applied for files with recognized asciidoc extension, for others simply removes trailing end of line character)
		1. Force the encoding to UTF-8
		2. Strip trailing spaces from each line, including end of line character
2. Based on the backend keyword, passes the structured document from the previous step to a converter. Can be HTML and DocBook (Default: HTML).
3. Brings the lines back together, joins the lines on the line feed character