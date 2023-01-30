# GitHub Action to setup Web Terminal

![https://github.com/zmicro-design/action-setup-web-terminal](https://img.shields.io/github/v/release/zmicro-design/action-setup-web-terminal)
![https://github.com/zmicro-design/action-setup-web-terminal](https://github.com/zmicro-design/action-setup-web-terminal/workflows//Publish/badge.svg)

### Usage

| option | required | description |
| ------ | -------- | ----------- |
| disable-service | false | do not start up service |
| report-url | false | specify report url |
| use-link | false | use link to visit |

### Example

```yml
# Setup Web Terminal CLI only
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Setup Web Terminal
        uses: zmicro-design/action-setup-web-terminal@v1
```

```yml
# disable Web Terminal service
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Setup Web Terminal
        uses: zmicro-design/action-setup-web-terminal@v1
        with:
          disable-service: true
```

```yml
# Start Web Terminal To Debug, use report url
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Setup Web Terminal
        uses: zmicro-design/action-setup-web-terminal@v1
        with:
          report-url: https://xxxxxxxxxx
```

```yml
# Start Web Terminal To Debug, use link
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Setup Web Terminal
        uses: zmicro-design/action-setup-web-terminal@v1
        with:
          use-link: true
```

### License

[MIT](./LICENSE)
