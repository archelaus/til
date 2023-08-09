## Exporting list of installed extensions
This a nifty way to copy a `json` of all installed extensions from any Chromium browser to your clipboard.

Head over to `chrome://extensions` or whatever's the equivalent in your browser, and run the following code in your console:
```javascript
copy(document.querySelector('extensions-manager').extensions_.map(({name, version, description, id, manifestHomePageUrl, state}) => ({name, version, description, id, manifestHomePageUrl, state})))
```
Voila! You have backup of all your extensions without using any external tool :)

### Alternative
Another way of doing something similar is heading over to `chrome://system` and clicking on the `Expand` button besides the `🔗 extensions` option. This'll open a list of all your extensions (along with their IDs), which you can now easily copy-paste anywhere you want.
To copy the list programmatically, run the following in the console:
```javascript
copy(document.querySelector('#div-extensions-value').textContent)
```
