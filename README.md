# Poseigen

Poseigen is a modular ecosystem of Python packages for machine-learning workflows with biological sequence data. This repository is its public landing page and meta-package source; each component's source is maintained separately.

## Component packages

- [poseigen_seaside](https://github.com/Husam94/poseigen_seaside) ([PyPI](https://pypi.org/project/poseigen_seaside/)) — shared utilities, metrics, and visualization.
- [poseigen_chisel](https://github.com/Husam94/poseigen_chisel) ([PyPI](https://pypi.org/project/poseigen_chisel/)) — biological data processing and conversion into ML-ready inputs.
- [poseigen_compass](https://github.com/Husam94/poseigen_compass) ([PyPI](https://pypi.org/project/poseigen_compass/)) — hyperparameter search, candidate scoring, and ensemble evaluation.
- [poseigen_trident](https://github.com/Husam94/poseigen_trident) ([PyPI](https://pypi.org/project/poseigen_trident/)) — neural-network building blocks and training utilities.
- [poseigen_mimic](https://github.com/Husam94/poseigen_mimic) ([PyPI](https://pypi.org/project/poseigen_mimic/)) — unified sequence-embedding architectures built on Trident.
- [poseigen_oyster](https://github.com/Husam94/poseigen_oyster) ([PyPI](https://pypi.org/project/poseigen_oyster/)) — interpretable genomic sequence models with exact position-specific k-mer contributions.

## How the packages fit together

- Seaside provides shared utilities.
- Chisel prepares biological data for modeling.
- Trident provides reusable neural-network and training components.
- Mimic and Oyster build sequence models using Trident.
- Compass supports model selection, optimization, and evaluation.

## Installation

The all-in-one `poseigen` meta-package is not yet published on PyPI. Until its first release, install the components you need individually, for example:

```bash
python -m pip install poseigen_oyster poseigen_trident
```

See each component's repository for its documentation, source, and release history.

## Development and releases

This is a hub, not a monorepo; component source code is not vendored here. See [RELEASE.md](RELEASE.md) for the suite's release process.
