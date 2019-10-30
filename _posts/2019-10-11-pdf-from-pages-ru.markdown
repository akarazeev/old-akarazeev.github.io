---
title: Compile PDF from Pages using Automator
lang: ru
ref: pdffrompages111019
date: 2019-10-11 03:00:01 +03:00
tags:
- Pages
- PDF
- Automator
- Mac
layout: post
header:
  teaser: "/images/pdffrompages.jpg"
---

For those who don't know that the Automator is: [URL](https://support.apple.com/guide/automator/welcome/mac)

In the terminal execute:
```bash
automator compile_pdf.workflow
```

Content of `compile_pdf.workflow`:
```python
set filePath to (POSIX file "/path/to/source/file.pages") as string
set theDestinationFolder to (POSIX file "/path/to/destination/folder") as string

set fileExtension to "pages"
set lastCharacterOffset to 2 + (count fileExtension)

tell application "Pages"
	activate

	tell application "Finder"
		set visible of process "Pages" to false
	end tell

	-- open the file
	set targetDocument to open file filePath

	if filePath ends with ":" then
		set fileName to item -2 of my decoupe(filePath, ":")
	else
		set fileName to item -1 of my decoupe(filePath, ":")
	end if

	set theOriginalName to fileName

	-- remove extension
	set fileName to text 1 thru -lastCharacterOffset of fileName
	# here theDestinationFolder is a text object
	set docPathAndName to theDestinationFolder & fileName & ".pdf"

	repeat 10 times # I added a loop which may be useful if the original document is very long
		try
			export targetDocument to file docPathAndName as PDF
			exit repeat
		on error
			tell me to delay 0.5
		end try
	end repeat
	-- close it
	close targetDocument saving no

	quit
end tell

on decoupe(t, d)
	local oTIDs, l
	set {oTIDs, AppleScript's text item delimiters} to {AppleScript's text item delimiters, d}
	set l to text items of t
	set AppleScript's text item delimiters to oTIDs
	return l
end decoupe
```
