# Contributing

English | [日本語](CONTRIBUTING.ja.md)

## Issues

Please use the issue form that fits:

- **Measurement report**: you measured a real box and a dimension differs from the model, or you measured something
  the drawings do not show (such as how far the cover opens).
- **Problem with a model**: a STEP file does not import, a dimension looks wrong, or a part name or color is wrong.
- **Model request**: you would like a model that is not in the list yet. Only boxes for which TAKACHI publishes
  2D drawings but no 3D data are in scope.

Please do not attach TAKACHI drawings, catalog pages or other copyrighted material. Photos of your own measurements
are welcome.

Rights holders: to ask for something to be removed, open any issue (a blank issue is fine).

## Pull requests

Pull requests are accepted **for documentation only** (README, NOTICE, CONTRIBUTING, `docs/`).
STEP files, preview images, `manifest.json`, `CHANGELOG.md` and the model READMEs are generated from the modeling
workspace, so pull requests that change them cannot be merged. Please open an issue instead.

## How measurements are used

A reported value is recorded in the model's source specification together with its origin (the issue number).
The model is then rebuilt and checked against the drawings again, and only then published again.
A model whose geometry changes gets a new revision in `manifest.json` and an entry in `CHANGELOG.md`.
