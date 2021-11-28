# Upload translation files to SimpleLocalize i18n editor

This Github Actions uses official and open-source SimpleLocalize CLI.

Learn more: https://github.com/simplelocalize/simplelocalize-cli

Documentation: https://simplelocalize.io/docs/cli/upload-translations/

## ☁️ Example upload action

```yml
name: 'Upload translations'
on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Upload translations
        uses: simplelocalize/upload@1.0.0
        with:
          apiKey: <YOUR_API_KEY>
          uploadPath: ./input-sample.json
          uploadFormat: multi-language-json
```
