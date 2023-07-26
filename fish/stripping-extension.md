## Strip extension from a filename using Fish's string

TIL: In the fish shell, an elegant and efficient way to strip file extensions from a filename is by utilizing the "string" command.
```fish
string split -m1 -r '.' -f1 <filename>
```
