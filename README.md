# Takachi enclosure 3D models (unofficial)

STEP models of TAKACHI waterproof enclosures for which only 2D drawings are published.
Use them to check that boards and parts fit, and to design holes, connectors and cable glands.
Each model is detailed (draft angles, fillets, gasket, latch, insert nuts) and was checked against the official drawings.

タカチ電機工業の防水ボックスのうち、2D 図面だけが公開されている型番の 3D モデル（STEP）です。
基板や部品の収まりの確認、穴・コネクタ・ケーブルグランドの追加工の設計に使えます。
抜き勾配・R・ガスケット・ラッチ・インサートナットまで作り、公式の図面と照合しています。

> [!IMPORTANT]
> **Unofficial.** Not affiliated with or endorsed by TAKACHI. Made only from the 2D drawings on takachi-el.co.jp.
> No warranty: check any dimension that matters for mounting or fit on a real box. Details: [NOTICE.md](NOTICE.md)
>
> **非公式です。** タカチ電機工業とは無関係で、承認も受けていません。公式サイトの 2D 図面だけを元に作りました。
> 無保証です。取付や干渉に関わる寸法は実物で確かめてください。詳しくは [NOTICE.md](NOTICE.md)

## Usage / 使い方

1. Pick a model below and download the STEP file for your color. / 下の一覧から型番を選び、色に合った STEP をダウンロードします。
2. Import it as described in [docs/onshape.md](docs/onshape.md). / [docs/onshape.md](docs/onshape.md) のとおりに取り込みます。

Each file is an assembly in the closed position (base, cover, gasket, latch, insert nuts), in mm, with +Z up.
Hinge axes, opening angles and revisions are in [manifest.json](manifest.json); changes are in [CHANGELOG.md](CHANGELOG.md).

どのファイルも閉じた状態のアセンブリ（本体・カバー・ガスケット・ラッチ・インサートナット）で、単位は mm、+Z が上です。
蝶番の軸・開き角・改訂は [manifest.json](manifest.json)、変更履歴は [CHANGELOG.md](CHANGELOG.md) にあります。

## Models / 型番一覧

<!-- models:begin -->
| Model / 型番 | Catalog W × D × H (mm) / カタログ外形寸法 | Color / 色 | STEP |
|---|---|---|---|
| [BCAP091207](models/BCAP/BCAP091207/) | 90 × 120 × 70 | White gray / ホワイトグレー<br>Clear cover / 透明カバー | [BCAP091207G](models/BCAP/BCAP091207/BCAP091207G.step)<br>[BCAP091207T](models/BCAP/BCAP091207/BCAP091207T.step) |
<!-- models:end -->

## Feedback / ご意見

Measurements, problems and model requests are welcome in [Issues](https://github.com/sgrsn/takachi-enclosure-models/issues/new/choose). See [CONTRIBUTING.md](CONTRIBUTING.md).

実測値の報告・不具合・型番の追加の希望は [Issues](https://github.com/sgrsn/takachi-enclosure-models/issues/new/choose) へどうぞ。[CONTRIBUTING.md](CONTRIBUTING.md) もご覧ください。

## License / ライセンス

The models are licensed under [CC BY 4.0](LICENSE). The license covers only the modeling work in this repository; it gives no rights to TAKACHI's trademarks or drawings.

モデルのライセンスは [CC BY 4.0](LICENSE) です。対象はこのリポジトリのモデル化の成果だけで、タカチの商標や図面の権利は含みません。
