<h2>TechBench Dump and API (Static HTML)</h2>
This repository is intended to fetch TechBench content, including older Office downloads, Windows 7 SP1, Windows 8.1 RTM, Windows 10, Windows Server Insider/LTSC Previews, Windows 11, and Windows 10/11 Insider Previews.

<h3>How this works</h3>
1. Like _any other_ TechBench modifications, this relies on replacing [Microsoft SDS](https://www.microsoft.com/software-download) (Software Download Service) URIs with a static, modified HTML, that includes a list of dynamically updated product IDs from the TechBench API directly.
2. Using _GitHub Actions_, we automatically update _option-values.json_ and _dump.json_ every 8 hours, and in the future, planning to include the static HTML anyone can use, and dynamically update its options as well.

<h2>Note on Insider Previews</h3>
Downloading a _Windows Insider Preview_, _Windows Server LTSC Preview_, or _Windows Server Insider Preview_ requires a Microsoft account to be signed into the same browser session because the Software Download Service requires this.
