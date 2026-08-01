<h2>TechBench Dump and API (Static HTML)</h2>
This repository is intended to fetch TechBench content, including older Office downloads, Windows 7 SP1, Windows 8.1 RTM, Windows 10, Windows Server Insider/LTSC Previews, Windows 11, and Windows 10/11 Insider Previews.

<h3>How this works</h3>
1. Like *any other* TechBench modifications, this relies on replacing [Microsoft SDS](https://www.microsoft.com/software-download) (Software Download Service) URIs with a static, modified HTML, that includes a list of dynamically updated product IDs from the TechBench API directly.
2. Using *GitHub Actions*, we automatically update *option-values.json* and *dump.json* every 8 hours, and in the future, planning to include the static HTML anyone can use, and dynamically update its options as well.

<h2>Note on Insider Previews</h3>
Downloading a *Windows Insider Preview*, *Windows Server LTSC Preview*, or *Windows Server Insider Preview* requires a Microsoft account to be signed into the same browser session because the Software Download Service requires this.
