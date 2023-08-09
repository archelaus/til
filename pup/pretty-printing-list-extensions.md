# Print installed extensions from the html file
```fish
paste (cat <input.html> | pup 'td:nth-child(3) a text{}' | psub) (cat <input.html> | pup 'td:nth-child(2) a text{}' | psub) | sort | column -t -s \t
```
