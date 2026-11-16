# Contributing / 協力のしかた

## English

### Issues

Please use the issue form that fits:

- **Measurement report**: you measured a real box and a dimension differs from the model, or you measured something
  the drawings do not show (such as how far the cover opens).
- **Bug**: a STEP file does not import, a dimension looks wrong, or a part name or color is wrong.
- **Model request**: you would like a model that is not in the list yet. Only boxes for which TAKACHI publishes
  2D drawings but no 3D data are in scope.

Please do not attach TAKACHI drawings, catalog pages or other copyrighted material. Photos of your own measurements
are welcome.

Rights holders: to ask for something to be removed, open any issue (a blank issue is fine).

### Pull requests

Pull requests are accepted **for documentation only** (README, NOTICE, CONTRIBUTING, `docs/`).
STEP files, preview images, `manifest.json`, `CHANGELOG.md` and the model READMEs are generated from the modeling
workspace, so pull requests that change them cannot be merged. Please open an issue instead.

### How measurements are used

A reported value is recorded in the model's source specification together with its origin (the issue number).
The model is then rebuilt and checked against the drawings again, and only then published again.
A model whose geometry changes gets a new revision in `manifest.json` and an entry in `CHANGELOG.md`.

## 日本語

### Issues

内容に合うフォームを選んでください。

- **実測値の報告**: 実物を測って、モデルと違う寸法があった。または、図面に無い所（カバーの開く角度など）を測った。
- **不具合**: STEP が取り込めない、寸法がおかしい、部品名や色が違う。
- **型番の追加**: 一覧に無い型番のモデルがほしい。タカチが 2D 図面だけを公開していて、3D データが無い製品が対象です。

タカチの図面やカタログのページなど、著作物は添付しないでください。ご自身で測ったときの写真は歓迎します。

権利をお持ちの方へ: 削除のご希望は、どの形式の Issue でもかまいません（空の Issue でも受け付けます）。

### プルリクエスト

プルリクエストは **文書の修正だけ** 受け付けます（README、NOTICE、CONTRIBUTING、`docs/`）。
STEP・プレビュー画像・`manifest.json`・`CHANGELOG.md`・型番ごとの README はモデル作成の作業環境から生成しているので、
これらを変えるプルリクエストは取り込めません。Issue でお知らせください。

### 実測値の扱い

報告された値は、出典（Issue の番号）と一緒にモデルの元の仕様に記録します。そのあとモデルを作り直し、図面との照合を
やり直してから公開し直します。形が変わった型番は `manifest.json` の改訂が上がり、`CHANGELOG.md` に記録されます。
