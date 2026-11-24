# browser-kit-host

Prebuilt copies of browser_kit's Chromium host (`cef_host.app`, built on the
[Chromium Embedded Framework](https://github.com/chromiumembedded/cef)), for
apps built without the host inside them. browser_kit downloads one the first
time a browser needs it.

There is no code here, only releases. Each release is one build of the host,
tagged `cef_host-<first 12 characters of its source hash>`. It has one zip
for each Mac architecture, named `cef_host-macos-<arch>-<hash>.zip`.

browser_kit pins each zip's SHA-256 and size. It refuses a download that
doesn't match them, and it runs nothing from the zip before that check
passes. The host is signed ad hoc, not notarized.

CEF is under a BSD license, and Chromium and the code it includes are under
their own licenses. Each release has them next to the zips: `LICENSE.txt`
(CEF) and `CREDITS.html` (Chromium and its third-party code).
