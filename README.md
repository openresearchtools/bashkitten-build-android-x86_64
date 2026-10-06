# BashKitten Android x86_64 builder

Build-only repository for [BashKitten](https://github.com/openresearchtools/BashKitten).
The workflow checks out the requested exact product commit and builds the native
Android x86_64 browser, Tor and remote client with the existing APK signing identity.

This repository has its own Gecko compiler cache. Gradle dependency downloads
use its repository cache; task outputs are downloadable Actions artifacts and do
not consume the Gecko cache quota. The same workflow source serves ARM64 and
x86_64 from `.github/builders/android.yml` in the product repository.

Download the signed APK and corresponding source/notices from **Actions > Artifacts**
as soon as upload completes. The main product workflow collects that same artifact
independently of other builds. This repository never publishes releases.
