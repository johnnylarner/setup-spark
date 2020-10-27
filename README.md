# setup-spark ✨

<p align="left">
  <a href="https://github.com/vemonet/setup-spark/actions"><img alt="GitHub Actions status" src="https://github.com/vemonet/setup-spark/workflows/Main%20workflow/badge.svg"></a>
</p>


This action sets up a Spark environment for use in actions by:

- optionally installing and adding to PATH a version of Python that is already installed in the tools cache.
- downloading, installing and adding to PATH an available version of Python from GitHub Releases ([actions/python-versions](https://github.com/actions/python-versions/releases)) if a specific version is not available in the tools cache.
- failing if a specific version of Python is not preinstalled or available for download.
- registering problem matchers for error output.

# Usage

See [action.yml](action.yml) for complete rundown of the available parameters.

Basic:
```yaml
steps:
- uses: actions/checkout@v2
- uses: vemonet/setup-spark@v1
  with:
    spark-version: '3.0.1' # Exact version
- run: spark-submit --version
```

# Available versions of Spark

`setup-spark` has only been tested for Apache Spark version `3.0.1`

It has been built based on [jupyter/docker-stack pyspark notebook Dockerfile](jupyter/docker-stack pyspark notebook Dockerfile)

> Feel free to test other Spark version and submit issues or pull requests!

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE).

# Contributions

Contributions are welcome! See our [Contributor's Guide](docs/contributors.md).
