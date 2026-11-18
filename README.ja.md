# タカチ防水ボックスの 3D モデル（非公式）

[English](README.md) | 日本語

タカチ電機工業の防水ボックスのうち、2D 図面だけが公開されている型番の 3D モデル（STEP）です。
基板や部品の収まりの確認、穴・コネクタ・ケーブルグランドの追加工の設計に使えます。
抜き勾配・R・ガスケット・ラッチ・インサートナットまで作り、公式の図面と照合しています。

> [!IMPORTANT]
> **非公式です。** タカチ電機工業とは無関係で、承認も受けていません。公式サイトの 2D 図面だけを元に作りました。
> 無保証です。取付や干渉に関わる寸法は実物で確かめてください。詳しくは [NOTICE.ja.md](NOTICE.ja.md)

## 使い方

下の一覧から型番を選び、色に合った STEP をダウンロードしてください。

どのファイルも閉じた状態のアセンブリ（本体・カバー・ガスケット・ラッチ・インサートナット）で、単位は mm です。
原点は本体の底の外面の中心で、+X が長辺の向き、+Y が蝶番の側、+Z が上です。
蝶番の軸・開き角・改訂は [manifest.json](manifest.json)、変更履歴は [CHANGELOG.md](CHANGELOG.md)（英語）にあります。

## 型番一覧

<!-- models:begin -->
| 型番 | カタログ外形寸法 W × D × H (mm) | 色 | STEP |
|---|---|---|---|
| [BCAP091207](models/BCAP/BCAP091207/) | 90 × 120 × 70 | ホワイトグレー<br>透明カバー | [BCAP091207G](models/BCAP/BCAP091207/BCAP091207G.step)<br>[BCAP091207T](models/BCAP/BCAP091207/BCAP091207T.step) |
| [BCAP091208](models/BCAP/BCAP091208/) | 90 × 120 × 85 | ホワイトグレー<br>透明カバー | [BCAP091208G](models/BCAP/BCAP091208/BCAP091208G.step)<br>[BCAP091208T](models/BCAP/BCAP091208/BCAP091208T.step) |
| [BCAP101507](models/BCAP/BCAP101507/) | 100 × 150 × 70 | ホワイトグレー<br>透明カバー | [BCAP101507G](models/BCAP/BCAP101507/BCAP101507G.step)<br>[BCAP101507T](models/BCAP/BCAP101507/BCAP101507T.step) |
| [BCAP101508](models/BCAP/BCAP101508/) | 100 × 150 × 85 | ホワイトグレー<br>透明カバー | [BCAP101508G](models/BCAP/BCAP101508/BCAP101508G.step)<br>[BCAP101508T](models/BCAP/BCAP101508/BCAP101508T.step) |
| [BCAP131508](models/BCAP/BCAP131508/) | 135 × 155 × 85 | ホワイトグレー<br>透明カバー | [BCAP131508G](models/BCAP/BCAP131508/BCAP131508G.step)<br>[BCAP131508T](models/BCAP/BCAP131508/BCAP131508T.step) |
| [BCAP131808](models/BCAP/BCAP131808/) | 135 × 185 × 85.5 | ホワイトグレー<br>透明カバー | [BCAP131808G](models/BCAP/BCAP131808/BCAP131808G.step)<br>[BCAP131808T](models/BCAP/BCAP131808/BCAP131808T.step) |
| [BCAP131810](models/BCAP/BCAP131810/) | 135 × 185 × 100.5 | ホワイトグレー<br>透明カバー | [BCAP131810G](models/BCAP/BCAP131810/BCAP131810G.step)<br>[BCAP131810T](models/BCAP/BCAP131810/BCAP131810T.step) |
<!-- models:end -->

## ご意見

実測値の報告・不具合・型番の追加の希望は [Issues](https://github.com/sgrsn/takachi-enclosure-models/issues/new/choose) へどうぞ。[CONTRIBUTING.ja.md](CONTRIBUTING.ja.md) もご覧ください。

## ライセンス

モデルのライセンスは [CC BY 4.0](LICENSE) です。対象はこのリポジトリのモデル化の成果だけで、タカチの商標や図面の権利は含みません。
