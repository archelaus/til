## Converting OPML (Outline Processor Markup Language) to plain text using Vim!
Today I discovered a nifty trick to convert OPML files into plain text using Vim. OPML files are commonly used for outlining and organizing information, but sometimes you just need the raw text without all the XML tags.

Execute the following command: 
```
%s/.*text="\([^"]*\)".xmlUrl="\([^"]*\)".*/• \1 - \2
```
This ingenious regex-based command replaced all XML tags with an empty string throughout the entire file.
