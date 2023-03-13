<p align="center">
  <img alt="NSIDC logo" src="https://nsidc.org/themes/custom/nsidc/logo.svg" width="150" />
</p>


# Quarto Demo

What is Quarto? How can I use it?


## Level of Support

* This repository is fully supported by NSIDC. If you discover any problems or bugs,
  please submit an Issue. If you would like to contribute to this repository, you may fork
  the repository and submit a pull request. 
* This repository is not actively supported by NSIDC but we welcome issue submissions and
  pull requests in order to foster community contribution.

See the [LICENSE](LICENSE) for details on permissions and warranties. Please contact
nsidc@nsidc.org for more information.


## Usage

### Run the slides

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
