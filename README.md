# Instructions

## Build

This site is generated using [Zola](https://www.getzola.org/).
Install zola and run `zola build` in the root of this repository.

## Deployment

Every push to this repository sets off a workflow to check and rebuild the site.
The artifact of the build is then automatically rsync'd to a web server.
See the `.github` directory for details, but otherwise the deployment process is kept intentionally simple.

# Credits

This site uses [Lexica Ultralegible](https://jacobxperez.github.io/lexica-ultralegible/) fonts, 2020 [Braille Institute of America](https://www.brailleinstitute.org/) and licensed under the [SIL Open Font License, v1.1](https://openfontlicense.org/open-font-license-official-text/).

Font files in `/static` are tracked using Git-LFS and are not present in source archives.
