# practice-intelligence-install

Public release artefacts for the Practice Intelligence self-service client
install: the compiled Bicep deployment template, its derived parameter
manifest, and `release.json` - the one file a firm's Cloud Shell install
script reads from a stable URL to deploy its own dashboard stack without
ever checking out this or any other Practice Intelligence repository.

Published by `practice-intelligence-app`'s release workflow
(`.github/workflows/release.yml`; see that repo's `docs/RELEASING.md`). Each
release is tagged `pi-app-v<version>` and carries:

- `pi-app-template.json` - the compiled Bicep template
- `pi-app-parameters.json` - its full parameter list, generated from the
  compiled template so it cannot drift
- `release.json` - the manifest the install script fetches: image digest,
  template URL and hash, and the exact format of the secrets the install
  creates

This repository holds no source code of its own.
