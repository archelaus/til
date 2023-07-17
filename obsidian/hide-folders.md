## Hiding folders in Obsidian using CSS

TIL that you can utilize a CSS snippet to exclude certain elements from being displayed in the explorer view. By using the following CSS code:
```css
div[data-path='path_from_vault'], 
div[data-path='path_from_vault'] + div.nav-folder-children 
{
    display: none;
}
```
Note that this does not affect their visibility in the graph or tag panel.

### To enable CSS snippets
1. Go to Settings -> Appearance.
2. Scroll down to find the folder icon beside CSS snippets.
3. Create a new file in that folder with any name ending in .css.
4. Paste the provided CSS code into the file.
5. Replace 'resources' in the code with the folder name you want to hide.
6. Restart Obsidian or click the Refresh icon next to the folder icon you modified.
