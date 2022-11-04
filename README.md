# Upload translation files

This Github Action uses [official SimpleLocalize CLI](https://github.com/simplelocalize/simplelocalize-cli).

Learn more: https://simplelocalize.io/docs/integrations/github-actions/

## Usage

```yml
name: 'My project'
on:
  push:
    branches: [ main, master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Upload translations
        uses: simplelocalize/upload@latest
        with:
          apiKey: <YOUR_API_KEY>
          uploadPath: ./{lang}/translations.json
          uploadFormat: single-language-json
          uploadOptions: "PUBLISH_AFTER_IMPORT,TRIM_LEADING_TRIALING_SPACES" # optional
          languageKey: en # optional, it accepts only one language key
```
