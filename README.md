<p align="center">
  <img alt="NSIDC logo" src="https://nsidc.org/themes/custom/nsidc/logo.svg" width="150" />
</p>


# Quarto Demo

What is Quarto? How can I use it?

[`quarto`](https://quarto.org/) is used to generate the [demo
website](https://nsidc.github.io/quarto-demo/) from this
repository via [GitHub Actions](.github/workflows/publish-to-quarto-website.yml)
on pushes to the `main` branch.


## Level of Support

This repository is not actively supported by NSIDC but we welcome issue submissions and
pull requests in order to foster community contribution.

See the [LICENSE](LICENSE) for details on permissions and warranties. Please contact
nsidc@nsidc.org for more information.


## Usage

### Install Quarto

Do not install with Conda, or the tinytex extension will not install correctly. TODO:
Open an issue in GitHub about this.

Please use an [official package](https://quarto.org/docs/download/).


#### Install tinytex for PDF rendering

```
quarto install tinytex
```


### Preview the output

```
quarto preview
```


## Troubleshooting

### Fails to render PDF, `tlmgr` doesn't exist

```
ERROR: Error executing '/home/mfisher/miniconda3/envs/quarto/bin/tlmgr': No such file or directory (os error 2)
```

My first instinct here was to install `texlive-core` from `conda-forge`, however that
currently doesn't include a subdependency
(https://github.com/conda-forge/texlive-core-feedstock/issues/27).

The [recommended course of
action](https://quarto.org/docs/output-formats/pdf-engine.html#installing-tex) is
`quarto install tinytex`, however this is not friendly with conda installations. To get
around this, we use the system install of Quarto, and install other dependencies with
conda.


## License

See [LICENSE](LICENSE).


## Code of Conduct

See [Code of Conduct](CODE_OF_CONDUCT.md).


## Credit

This software was developed by the National Snow and Ice Data Center with funding from
multiple sources.
