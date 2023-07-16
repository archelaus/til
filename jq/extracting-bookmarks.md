## Extracting all your bookmarks from your fav Chromium browser

TIL, you can extract your bookmarks fairly easily since they're stored on the disk under `~/.config/BraveSoftware/Brave-Browser/Default` in `Bookmarks` which is \*drumroll\* in json! If you don't use Brave that's no problem at all, other Chromium browsers follow a similar pattern.

Anyway, here's how can you extract all the links from the file using `jq`:

```
jq -r '.. | .error? // empty' <bookmarks_file_path>
```
