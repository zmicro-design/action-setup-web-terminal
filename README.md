# GitHub Action to setup Web Terminal

![https://github.com/zmicro-design/action-setup-web-terminal](https://img.shields.io/github/v/release/zmicro-design/action-setup-web-terminal)
![https://github.com/zmicro-design/action-setup-web-terminal](https://github.com/zmicro-design/action-setup-web-terminal/workflows//Publish/badge.svg)

### Usage

| option | required | description |
| ------ | -------- | ----------- |
| report_url | false | report url to |

### Example

```yml
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Setup Docker
        uses: zmicro-design/action-setup-web-terminal@v1
```

### License

[MIT](./LICENSE)
