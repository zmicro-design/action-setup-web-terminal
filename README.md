# GitHub Action to setup Web Terminal

![https://github.com/zmicro-design/action-setup-web-terminal](https://img.shields.io/github/v/release/zmicro-design/action-setup-web-terminal)
![https://github.com/zmicro-design/action-setup-web-terminal](https://github.com/zmicro-design/action-setup-web-terminal/workflows//Publish/badge.svg)

### Usage

| option | required | description |
| ------ | -------- | ----------- |
| debug | false | start up debug service |
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
      - name: Setup Docker
        uses: zmicro-design/action-setup-web-terminal@v1
```

```yml
# Start Web Terminal To Debug
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Setup Docker
        uses: zmicro-design/action-setup-web-terminal@v1
        with:
          debug: true
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
      - name: Setup Docker
        uses: zmicro-design/action-setup-web-terminal@v1
        with:
          debug: true
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
      - name: Setup Docker
        uses: zmicro-design/action-setup-web-terminal@v1
        with:
          debug: true
          use-link: true
```

### License

[MIT](./LICENSE)
