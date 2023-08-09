# Print installed extensions from the html file
```fish
paste (cat Documents/extensions_info_2023_8_9.html | pup 'td:nth-child(3) a text{}' | psub) (cat Documents/extensions_info_2023_8_9.html | pup 'td:nth-child(2) a text{}' | psub) | sort | column -t -s \t
```
