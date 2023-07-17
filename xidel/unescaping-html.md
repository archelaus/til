## Unescaping HTML Entities with xidel

To unescape HTML entities using xidel, you can use the `parse-html` function. Here's the command:
```bash
xidel -s - -e 'parse-html($raw)'
```
You can pass the HTML content through a pipe to this command, or you can provide the content directly through the command line.
