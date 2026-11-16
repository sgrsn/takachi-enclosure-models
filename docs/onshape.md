# Using the models in Onshape / Onshape での使い方

[English](#english) · [日本語](#日本語)

## English

### Import

1. In an Onshape document, click **+** in the tab bar at the bottom left, choose **Import…**, and select the STEP file
   (`<MODEL>.step`, for example `BCAP091207G.step`).
2. Import options:
   - Do **not** flatten the assembly into a single Part Studio. Keeping the assembly keeps one part per component,
     with its name.
   - Do **not** check **Y Axis is up**. The models use +Z up.
   - The STEP file is in millimeters. If Onshape asks for units, choose millimeters.
3. Onshape creates a Part Studio (the geometry) and an Assembly (the placement). Parts are named `<MODEL>_<Role>`,
   for example `BCAP091207G_Base`, `BCAP091207G_TopCover`, `BCAP091207G_Gasket`, `BCAP091207G_Latch`.
   When a role appears more than once, `_1`, `_2`, … is added (for example `BCAP091207G_InsertNutM4_1`).
   All parts are already in the closed position, so you can check fit and interference right away.
4. In the Assembly, **Fix** the base (`<MODEL>_Base`). Fasten the gasket and the insert nuts to the base, and the latch
   (closed position) to the base or the cover, with **Fastened** mates.
5. Clear-cover variants carry the cover color and transparency in the STEP file. If the cover does not look
   transparent, set its **Appearance** in the Assembly (the colors are listed in `manifest.json`).
6. To add holes, connectors or glands, edit the imported parts in the Part Studio, or model the cutting shapes in a new
   Part Studio and remove them with **Boolean → Subtract**.

The screws supplied with the box are not modeled. Use Onshape standard content instead.

### Coordinate system

- Origin: center of the bottom outer face of the base (feet not included)
- +Z: up (toward the cover)
- +X: along the long side of the box
- +Y: toward the hinge (the latch is on the −Y side)
- Units: mm

Each model's README lists the catalog dimensions (W × D × H) and the overall size including ears, hinge, latch and
feet, with the model axis of each dimension.

### Hinge (revolute mate)

The hinge axis and the maximum opening angle of each model are in [`manifest.json`](../manifest.json), under
`models.<BASE>.hinge`:

- `point_mm`: a point on the axis (mm)
- `axis`: the direction of the axis
- `max_open_deg`: the maximum opening angle in degrees (0° = closed)

To make the cover open and close:

1. In the Assembly, fix the base.
2. Place a **Mate connector** on the circular edge of the hinge pin hole in a base knuckle. Its origin must lie on the
   hinge axis and its Z axis must point along the axis direction; use **Flip primary axis** if needed.
3. Place a Mate connector the same way on the circular edge of the pin hole in a cover knuckle.
4. Select both Mate connectors and create a **Revolute** mate. Under **Limits**, set 0° to `max_open_deg`.
5. The latch is modeled in its closed position. Suppress (or delete) the latch's Fastened mate before you open the
   cover.

## 日本語

### 取り込み

1. Onshape のドキュメントで、左下のタブ一覧の **+** から **Import…**（インポート）を選び、STEP ファイル
   （`<型番>.step`。例: `BCAP091207G.step`）を選びます。
2. インポートの設定:
   - アセンブリを 1 つの Part Studio に平坦化するオプションは **使いません**。部品ごとのアセンブリ構造と部品名を
     保つためです。
   - **Y Axis is up** は **チェックしません**。このモデルは +Z が上です。
   - STEP の単位は mm です。単位を聞かれたら mm を選びます。
3. 取り込むと Part Studio（形状）と Assembly（部品の配置）ができます。部品名は `<型番>_<Role>` です
   （例: `BCAP091207G_Base`、`BCAP091207G_TopCover`、`BCAP091207G_Gasket`、`BCAP091207G_Latch`）。
   同じ Role が複数あるときは `_1`、`_2` … が付きます（例: `BCAP091207G_InsertNutM4_1`）。
   全部品が閉じた状態の位置にあるので、そのまま収まりや干渉の確認に使えます。
4. Assembly で本体（`<型番>_Base`）を **Fix** で固定します。ガスケットとインサートナットは本体に、
   ラッチ（閉じた位置）は本体かカバーに、**Fastened** mate で固定します。
5. 透明カバーの型番は、カバーの色と透明度を STEP の外観として持っています。透明に見えないときは、
   Assembly でカバーの **Appearance** を設定してください（色は `manifest.json` にあります）。
6. 穴・コネクタ・グランドの追加工は、取り込んだ部品を Part Studio で編集するか、新しい Part Studio で穴の形を作って
   **Boolean → Subtract** で差し引きます。

付属のビスはモデルに含みません。Onshape の標準部品を使ってください。

### 座標系

- 原点: 本体の底の外面の中心（脚は含まない）
- +Z: 上（カバー側）
- +X: 箱の長辺の方向
- +Y: 蝶番側（ラッチは −Y 側）
- 単位: mm

型番ごとの README に、カタログの外形寸法（W × D × H）と、耳・蝶番・ラッチ・脚を含む全体の大きさを、
それぞれの寸法がモデルのどの軸の向きかと合わせて載せています。

### 蝶番（Revolute mate）

型番ごとの蝶番の軸と最大開き角は [`manifest.json`](../manifest.json) の `models.<BASE>.hinge` にあります。

- `point_mm`: 軸上の 1 点（mm）
- `axis`: 軸の向き
- `max_open_deg`: 最大開き角（度。閉じた状態が 0°）

カバーを開閉できるようにする手順:

1. Assembly で本体を固定します。
2. 本体側の蝶番ナックルにあるピン穴の円エッジに **Mate connector** を置きます。原点が蝶番の軸の上に、
   Z 軸が軸の向きになるようにします（必要なら **Flip primary axis** で向きを合わせます）。
3. カバー側の蝶番ナックルのピン穴の円エッジにも、同じように Mate connector を置きます。
4. 2 つの Mate connector を選んで **Revolute** mate を作り、**Limits** で 0° から `max_open_deg` までを設定します。
5. ラッチは閉じた位置の形です。カバーを開く前に、ラッチの Fastened mate を抑制（または削除）してください。
