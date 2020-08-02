# [Go Link Check `glc`](https://github.com/dbtedman/go-link-check)

Link check automation tool.

[![Actions Status](https://github.com/dbtedman/go-link-check/workflows/test/badge.svg)](https://github.com/dbtedman/go-link-check/actions)
[![codecov](https://codecov.io/gh/dbtedman/go-link-check/branch/master/graph/badge.svg)](https://codecov.io/gh/dbtedman/go-link-check)
[![Known Vulnerabilities](https://snyk.io/test/github/dbtedman/go-link-check/badge.svg)](https://snyk.io/test/github/dbtedman/go-link-check)
![Go Version](https://img.shields.io/static/v1?label=Go&message=v1.13&color=blue&style=flat)

-   [How to use this tool?](#how-to-use-this-tool)
-   [What options does it have?](#what-options-does-it-have)
-   [Can I use Docker?](#can-i-use-docker)
-   [How to contribute?](#how-to-contribute)
-   [Is this project secure?](#is-this-project-secure)
-   [How is the project structured?](#how-is-the-project-structured)
-   [License](#license)

## How to use this tool?

Install necessary dependencies, build and run program:

```bash
go mod vendor && go build -mod=vendor -o ./glc && ./glc -url="https://danieltedman.com"
```

You will see output something like the following:

```text
{"level":"debug","msg":"checking: https://github.com/dbtedman","time":"2020-04-20T19:22:52+10:00"}
{"level":"debug","msg":"checking: https://danieltedman.com/cart","time":"2020-04-20T19:22:52+10:00"}
{"level":"debug","msg":"checking: https://www.linkedin.com/in/dbtedman","time":"2020-04-20T19:22:52+10:00"}
{"level":"debug","msg":"checking: https://danieltedman.com/","time":"2020-04-20T19:22:53+10:00"}
{"level":"debug","msg":"checking: https://danieltedman.com/my-work","time":"2020-04-20T19:22:54+10:00"}
{"level":"info","msg":"Results written to file \"results.csv\"","time":"2020-04-20T19:22:55+10:00"}
```

## What options does it have?

To learn more about the available configuration options, view the help.

```bash
./glc -help
```

You will see something like the following.

```text
Usage of ./glc:
  -outFile string
        (optional) Path to output report csv to. (default "results.csv")
  -url string
        Website URL to parse for links to validate.
```

## Can I use Docker?

Yes, [Docker](https://www.docker.com/) can be used to build and run the application.

```bash
docker build --tag glc:latest . && docker run -it --rm glc:latest -url="https://danieltedman.com"
```

## How to contribute?

Read our [Contributing Guide](CONTRIBUTING.md) to learn more about how to contribute to this project.

## Is this project secure?

Read our [Security Guide](SECURITY.md) to learn how security is considered during the development and operation of this plugin.

## How is the project structured?

Read our [Architecture Document](ARCHITECTURE.md) to learn how this project is structured.

## License

The [MIT License](./LICENSE.md) is used by this project.
