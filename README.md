# studiorack-template-sf2
![Release](https://github.com/studiorack/studiorack-template-sf2/workflows/Release/badge.svg)

Audio plugin starter template using SoundFont 2 (SF2) to build bundles using:

* polyphone 2.3.x


## Installation

Install polyphone in order to convert .sf2 files to .sf3:

    https://www.polyphone-soundfonts.com/download


## Usage

Add your .sf2 files into this directory:

    ./


## Testing your plugin

Todo


## Build (manual)

Compress lossless version:

    zip -r ./studiorack-template-sf2.zip *

Create lossy version:

    for file in $(find . -type f -name '*.sf2'); do polyphone -2 -i "$file"; done
    find . -type f -name '*.sf2' -type f -delete

Compress lossy version:

    zip -r ./studiorack-template-sf2-lossy.zip *


## Build (automatic)

Release a plugin version on GitHub by simply creating a version tag:

    git tag v0.0.1
    git push && git push origin --tags

This will run an automated build and release process on GitHub Actions:

    .github/workflows/release.yml


## Resources & guides

* [SoundFont history](https://en.wikipedia.org/wiki/SoundFont)
* [SoundFont 2 structure](https://mrtenz.github.io/soundfont2/)


## Contact

For more information please contact kmturley
