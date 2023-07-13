## Converting OPML to plain text format using sed

This handy technique allows for easy extraction of titles and URLs from OPML files.

To perform the conversion, use the following **sed** command:
```
sed -n '/<outline /{s|.*text="\([^"]*\)".*xmlUrl="\([^"]*\)".*|• \1 - \2|;s|&amp;|\&|g;s|&#39;|\'|g;s|&#34;||g;s|&gt;|>|g;s|&lt;|<|g;p}' input.opml > output.txt
```
This command:
- Extracts text within text and xmlUrl attributes.
- Replaces `&amp;` with &.
- Replaces `&#39;` with a single quote (').
- Removes `&#34;` (double quotes).
- Replaces `&gt;` with >.
- Replaces `&lt;` with <.
