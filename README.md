## TechBench Dump and API (Static HTML)</h2>
This repository is intended to fetch TechBench content, including older Office downloads, Windows 7 SP1, Windows 8.1 RTM, Windows 10, Windows Server Insider/LTSC Previews, Windows 11, and Windows 10/11 Insider Previews.

## How this project was made
This repository is a self-maintaining TechBench product mirror, hosted on GitHub and updates its dump multiple times daily. Thanks to GitHub Actions, the YAML workflows take care of all the work updating the repository, while you only need to copy the _tb.html_ file to a Software Download URI and overwrite the default page contents with these updated contents.

The design is supposed to be aligned with Microsoft's own **Software Download** URIs, but integrate all known TechBench products in a unified, user-friendly drop-down menu. You can download older versions of Windows from Microsoft directly. I need to note that this mirror does _not_ gain any sort of access to proprietary _Windows IoT_ or _Long-Term Servicing Channel_ and _Volume Licensing_ versions that belong to the **Volume License Center (VLSC)**, the **Microsoft 365 Admin Center**, or **My Visual Studio (MYVS)**.

Microsoft _has_ strictened their requirements since 2021 for TechBench, and older tools no longer work. This HTML page uses the reliability of using Microsoft's own _SDS_ API calls integrated into their API and does not attempt to re-create the logic, just to list multiple download links and let the server handle the logic.

### How this works
1. Like *any other* TechBench modifications, this relies on replacing [Microsoft SDS](https://www.microsoft.com/software-download) (Software Download Service) URIs with a static, modified HTML, that includes a list of dynamically updated product IDs from the TechBench API directly.
2. Using *GitHub Actions*, we automatically update *option-values.json* and *dump.json* every 8 hours, and I now included the static HTML anyone can copy and paste over any Microsoft SDS page, and dynamically update its options as well.

## Note on Insider Previews
Downloading a *Windows Insider Preview*, *Windows Server LTSC Preview*, or *Windows Server Insider Preview* requires a Microsoft account to be signed into the same browser session because the Software Download Service requires this.

## How to use it
1. Go to [https://www.microsoft.com/software-download](https://www.microsoft.com/software-download) or any sub-domain of it ([Windows 11 Software Download](https://www.microsoft.com/software-download/windows11), for example), enter DevTools on Chrome or Edge (Firefox and other browsers have a separate feature that does this), right-click the top of the HTML (beginning with _<html lang="en-US"..._) and select "Edit as HTML", then select all of the contents, remove them, and replace them with the exact contents of _tb.html_.
2. Download any Windows version on TechBench from the drop-down menu, earliest to latest. You must be signed into a Microsoft account before downloading Windows Insider Previews.

This is an example of a user signed into their Microsoft account when trying to download Insider Previews, it successfully shows a Download button:
<img width="1126" height="591" alt="Signed in to MSFT account" src="https://github.com/user-attachments/assets/5503f28b-6328-448f-ac40-3b17f8d998f2" />

For a user not signed into one:
<img width="1341" height="595" alt="Not signed in to MSFT account" src="https://github.com/user-attachments/assets/bfd6e9b0-ad35-42b9-9d0c-c55a5abd87b8" />
