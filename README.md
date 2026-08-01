## TechBench Dump and API (Static HTML)</h2>
This repository is intended to fetch TechBench content, including older Office downloads, Windows 7 SP1, Windows 8.1 RTM, Windows 10, Windows Server Insider/LTSC Previews, Windows 11, and Windows 10/11 Insider Previews.

### How this works
1. Like *any other* TechBench modifications, this relies on replacing [Microsoft SDS](https://www.microsoft.com/software-download) (Software Download Service) URIs with a static, modified HTML, that includes a list of dynamically updated product IDs from the TechBench API directly.
2. Using *GitHub Actions*, we automatically update *option-values.json* and *dump.json* every 8 hours, and I now included the static HTML anyone can copy and paste over any Microsoft SDS page, and dynamically update its options as well.

## Note on Insider Previews
Downloading a *Windows Insider Preview*, *Windows Server LTSC Preview*, or *Windows Server Insider Preview* requires a Microsoft account to be signed into the same browser session because the Software Download Service requires this.

## How to use it
1. Go to [https://www.microsoft.com/software-download](https://www.microsoft.com/software-download) or any sub-domain of it ([Windows 11 Software Download](https://www.microsoft.com/software-download/windows11), for example), enter DevTools on Chrome or Edge (Firefox and other browsers have a separate feature that does this), right-click the top of the HTML (beginning with _<html lang="en-US"..._) and select "Edit as HTML", then select all of the contents, remove them, and replace them with the exact contents of _tb.html_.
2. Download any Windows version on TechBench from the drop-down menu, earliest to latest. You must be signed into a Microsoft account before downloading Windows Insider Previews.
