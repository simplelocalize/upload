# Upload localization files to SimpleLocalize

This Github Actions uses official and open-source SimpleLocalize CLI.

Learn more: https://github.com/simplelocalize/simplelocalize-cli

Documentation: https://simplelocalize.io/docs/cli/upload-translations/

## ☁️ Example upload action

```yml
name: 'Upload translations'
on:
  push:
    branches: [ main, master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Upload translations
        uses: simplelocalize/upload@latest
        with:
          apiKey: <YOUR_API_KEY>
          uploadPath: ./{lang}/translations.json
          uploadFormat: single-language-json
          uploadOptions: "PUBLISH_AFTER_IMPORT,TRIM_LEADING_TRIALING_SPACES" # optional
          languageKey: en # optional, it accepts only one lanauge key
```
