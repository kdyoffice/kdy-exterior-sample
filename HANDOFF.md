# KDY Office 外構HP営業サンプル 引き継ぎメモ

このメモは、Codexで進めてきた作業をClaude Codeなど別AIに引き継ぐためのものです。
作業フォルダは以下です。

`/Users/minoru/Documents/Codex/2026-05-09/leeroydotuk-ai-sales-machine-2026-google`

## 目的

ユーザーは、本業のリフォーム営業経験を活かして、職人さん・施工店・一人親方向けに「名刺代わりになる高品質HP制作」を副業として試したい。

飛び込み営業や電話営業は苦手。顔出しも会社バレリスクがあるため避けたい。リアル活動時間も少ないため、まずはサンプルHPとA4チラシを作り、知人経由・保護者つながり・紹介・紙で見せる営業を想定している。

最初のターゲットは、鳥取県西部・島根県東部周辺の外構・エクステリア業者。

## 事業コンセプト

単なるWeb制作ではなく、以下の価値を売る。

- LINEで送れる名刺代わりのHP
- 見積もり相談前の信用材料
- 施工写真・職人写真・お客様の声・料金目安を整理して、問い合わせ前の不安を減らす
- HPがない職人さんでも始めやすい
- LINE公式アカウント、QR付き名刺、紙チラシまで導線として提案できる

営業トークの核は「うちで作りませんか」ではなく、

「こういう見せ方もできますよ」
「今のHP・名刺・施工写真を見せてください」

という押し売りしない形。

## 重要なユーザーの判断・こだわり

- 最初に見せるサンプルの品質が非常に重要。
- パッと見て「すごい」と思われないと問い合わせにはつながらない。
- 安っぽいイラストや濃い緑はNG。
- 実写真・施工写真・Before/After・職人写真が重要。
- 架空サンプルなので一部生成写真は可。ただしBefore/Afterが別の家に見えるなど、不自然なものは避ける。
- サンプルであることは明確にする。
- A4チラシは実際に印刷して見せる前提。PDFで切れないこと、紙面バランスが重要。

## 現在の主なファイル

- `index.html`
  - 架空業者「KDYエクステリア」のサンプルHP。
  - 鳥取県西部・島根県東部対応の外構業者という設定。

- `styles.css`
  - サンプルHP用CSS。
  - 濃い緑ではなく、白・淡いグリーングレー・ティール寄りの爽やかな配色に調整済み。

- `flyer.html`
  - KDY OfficeのA4営業チラシ。
  - 職人さん・施工店・一人親方向け。

- `flyer.css`
  - A4チラシ用CSS。
  - 画面表示と印刷表示でメディアクエリあり。
  - `@media print` はA4 PDF出力用。スマホ用CSSは `@media screen and (max-width: 760px)` にして、PDF出力時にスマホ用が効かないようにしている。

- `flyer-a4.pdf`
  - 現在の最新版A4 PDF。

- `flyer-a4-check.png`
  - PDF確認用に変換した画像。

- `flyer-preview.png`
  - ブラウザ表示確認用の画像。

- `cases/driveway.html`
- `cases/fence.html`
- `cases/carport.html`
  - 施工事例詳細ページ。

- `hearing-sheet.html` / `hearing-sheet.css` / `hearing-sheet.pdf` / `hearing-sheet.txt` / `hearing-sheet.md`
  - 初回ヒアリングシート（A4 1ページ）。
  - 7ブロック構成：基本情報／今ある見せられるもの／強み／困りごと／持っている素材（最重要）／料金感／次回アクション＋さくみメモ。
  - PDFは紙印刷用、txtはiPhoneメモアプリにコピペして使う想定。

- `plans.html` / `plans.css` / `plans.pdf` / `plans.txt`
  - 制作プラン表（A4 1ページ）。
  - 入口S/M/L、セットS/M/L、名刺オプション、維持・運用プランの料金体系。
  - PDFは営業先に手渡す用、txtはLINE/メール本文に貼る用。
  - `plans-check.png` はPDF確認用画像。

- `assets/`
  - サンプルHP・チラシで使う画像群。
  - 代表的なもの:
    - `generated-staff.png`
    - `generated-work-fence.png`
    - `carport-house.jpg`
    - `driveway-house.jpg`
    - `case-driveway-new.png`
    - `case-privacy-fence.png`
    - `case-approach.png`
    - `case-carport-new.png`
    - `case-garden-turf.png`
    - `case-gravel-sideyard.png`
    - `case-gate-mailbox.png`
    - `L_gainfriends_2dbarcodes_GW.png`
      - KDY Office LINE公式アカウントの友だち追加QR。
      - 元ファイルは `/Users/minoru/Downloads/2dbarcodes_GW.zip` から展開。
    - `sample-hp-qr.png`
      - サンプルHP確認用QR。
      - 現在はGitHub Pages公開URLを指している。

## 公開URL

GitHubリポジトリ:

`https://github.com/kdyoffice/kdy-exterior-sample`

サンプルHPの公開URL:

`https://kdyoffice.github.io/kdy-exterior-sample/`

注意:

- GitHub Desktopから公開リポジトリ作成までは完了済み。
- GitHub Pagesは有効化済み。
- GitHubの `Settings > Pages` で Source は `Deploy from a branch`、Branch は `main / root`。
- 2026-05-10時点で `curl -I https://kdyoffice.github.io/kdy-exterior-sample/` は `HTTP/2 200` を確認済み。
- チラシ中央QRの `assets/sample-hp-qr.png` は、このGitHub Pages公開URLを指す。

## 現在のチラシ内容

メインコピー:

「その仕事ぶり、ちゃんと伝わるHPにしませんか。」

リード:

「LINEで送れる名刺代わりに。見積もり相談の前に安心してもらえる、職人さん・施工店向けのホームページを作ります。」

問題提起:

- 紹介されたのに、信用材料がない
- 施工の良さが口だけで伝わらない
- LINEで送れるページがない

作れるもの:

- 施工事例・Before/After
- 代表写真・職人紹介
- お客様の声・口コミ掲載
- 料金目安・対応エリア
- LINE相談・Googleマップ連携
- QR付き名刺デザイン

料金:

- 入口プラン: 5万円〜
- おすすめセット: 18万円〜28万円
  - HP + LINE導線 + QR付き名刺までまとめて整える
- 名刺オプション: 1万円〜4万円
  - デザインのみ1万円
  - QR付き1.5万円〜2万円
  - 現物100枚は2.5万円〜4万円

問い合わせ欄:

「今のHP・名刺・施工写真を見せてください。」

「LINE / 紹介 / メール」

メールアドレス:

`k.d.yoffice.co@gmail.com`

LINE友だち追加URL:

`https://lin.ee/nT7JVWE`

チラシ内のQR配置:

- 中央の「まずはサンプルだけ見てください。」欄
  - `assets/sample-hp-qr.png`
  - サンプルHP確認用QR。
- 右下の問い合わせ欄
  - `assets/L_gainfriends_2dbarcodes_GW.png`
  - KDY Office LINE友だち追加QR。

## LINE公式アカウントについての方針

LINE公式アカウント設定は、オプションとして相性が良い。

ただし、最初から運用代行まで請けると重くなるため、まずは「初期設定支援」に絞るのが良い。

提案範囲:

- LINE公式アカウント開設サポート
- プロフィール設定
- あいさつメッセージ
- リッチメニュー
- 「写真を送って相談」導線
- HP・チラシ・名刺へのLINEリンク/QR設置

注意:

- アカウント開設・ログイン・本人確認などは顧客本人にやってもらう。
- こちらは横で案内する、または画面共有・手順書で支援する形。

## 現在のKDY Office LINE公式アカウント設定

LINE Official Account Manager:

`https://manager.line.biz/account/@287ysmot/`

友だち追加URL:

`https://lin.ee/nT7JVWE`

設定済みの自動応答:

- `相談希望`
- `料金を知りたい`
- `サンプル希望`
- `Default`

`Default` はもともと「個別のお問い合わせを受け付けておりません」という営業上かなり危ない文面だったため、以下の方向へ修正済み。

```txt
メッセージありがとうございます。
内容を確認して、必要に応じて返信いたします。

ご相談の場合は、このまま
「相談希望」
と送ってください。

料金の目安を知りたい場合は
「料金を知りたい」
サンプルを見たい場合は
「サンプル希望」
と送ってください。
```

`相談希望` の自動応答:

```txt
相談希望ありがとうございます。

まずは分かる範囲で大丈夫ですので、以下を教えてください。

1. 業種・仕事内容
例：外構、電気工事、水道設備、リフォームなど

2. 今HPはありますか？
ある / ない / 分からない

3. 相談したい内容
例：HPを作りたい、名刺を作りたい、LINEを整えたい、料金だけ知りたい

4. 施工写真や名刺があれば、必要に応じて送ってください。

いただいた内容を見て、どんな見せ方ができるか一緒に整理します。
```

`料金を知りたい` の自動応答:

```txt
料金の目安はこちらです。

■ 入口プラン
5万円〜
1ページの名刺代わりHPを作成します。

■ おすすめセット
18万円〜28万円
HP・LINE導線・QR付き名刺までまとめて整えます。

■ 名刺オプション
1万円〜4万円
デザインのみ、QR付き名刺、現物100枚の印刷手配まで対応できます。

内容によって変わるため、正確な金額は現在のHP・名刺・施工写真などを確認してからご案内します。

相談したい場合は、このまま
「相談希望」
と送ってください。
```

`サンプル希望` の自動応答（2026-05-10 LINE管理画面に反映済み・確定版）:

```txt
サンプル希望ありがとうございます。

職人さん・施工店向けに作った見本サイトをご案内します。

▼ サンプルHPはこちら
https://kdyoffice.github.io/kdy-exterior-sample/

施工事例、Before/After、料金目安、お客様の声、Googleマップ連携まで入れた、外構業者さん向けの見本です。
※ 架空の業者「KDYエクステリア」のサンプルです。

外構以外の業種（電気・水道・リフォーム・大工など）でも、同じ作りで対応できます。
雰囲気もご希望に合わせて調整できますので、「もっと和風」「もっとシンプル」などのご要望もお気軽にどうぞ。

「自分の業種だとどんな見せ方になるか知りたい」
という場合は、このまま
「相談希望」
と送ってください。
```

リッチメニュー:

- 画像ファイル: `rich-menu-kdy.png`
- 元HTML: `rich-menu.html`
- 3分割:
  - サンプルを見る
  - 料金を見る
  - 相談する
- LINE側で作成済み。
- 推奨アクション:
  - サンプルを見る: テキスト `サンプル希望`
  - 料金を見る: テキスト `料金を知りたい`
  - 相談する: テキスト `相談希望`

## 名刺についての方針

名刺はかなり相性が良い。

理由:

- 職人さんはまだ紙の名刺を使うことが多い。
- QRを載せればHPやLINEにつながる。
- 「HPだけ」よりも使い道が具体化する。

料金案:

- 名刺デザインのみ: 1万円
- QR付き名刺デザイン: 1.5万円〜2万円
- 名刺デザイン + 現物100枚: 2.5万円〜4万円
- HP + LINE + 名刺セット: 18万円〜28万円

印刷は外注想定。
印刷費・仕様・納期・修正回数は明確に分けること。

## 現在のA4チラシ調整履歴と注意点

PDF出力時に一度、スマホ用CSSが効いてA4なのに縦長レイアウトになり、親子職人の写真の下で切れた。

対策:

- スマホ用メディアクエリを `@media screen and (max-width: 760px)` に変更済み。
- `@media print` でA4用のサイズ調整をしている。

また、一度 `overflow: hidden` で強制的に1ページに見せていたが、それは実際には切れているだけだったため注意。
ただし最新版では、印刷時のA4枠そのものに対して `height: 297mm; overflow: hidden;` を使い、余白だけの白紙2ページ目を出さないための保険にしている。
この設定を触る場合は、必ずPDFを再生成して実際に1ページか確認すること。

最新版では、真ん中左の空白に職人写真・施工写真3枚を配置して、紙面バランスを改善済み。

2026-05-10時点の追加修正:

- LINE友だち追加QRをチラシに反映済み。
- メールアドレス `k.d.yoffice.co@gmail.com` を問い合わせ欄に追加済み。
- ユーザー指示により、中央QRはサンプルHP確認用、右下のメール横QRはKDY Office LINE友だち追加用に修正済み。
- サンプルHP確認用QRは `assets/sample-hp-qr.png`。
- `assets/sample-hp-qr.png` は `https://kdyoffice.github.io/kdy-exterior-sample/` を指すQRとして再生成済み。
- メール追加後に白紙2ページ目が出たため、`@media print` 側を調整。
  - `.flyer` を `height: 297mm`
  - `padding: 7mm`
  - `gap: 10px`
  - `overflow: hidden`
  - Hero画像や余白を少し圧縮
- PDF再生成後、`strings flyer-a4.pdf | rg '^/Count '` で `/Count 1` を確認済み。
- 最新PDF `flyer-a4.pdf` は2026-05-10に再生成済み。
- 最新確認画像 `flyer-a4-check.png` では、A4 1ページ内に中央サンプルHP QRと右下LINE QRが収まっている。

PDF生成・確認に使ったコマンド例:

```sh
'/Applications/Google Chrome.app/Contents/MacOS/Google Chrome' \
  --headless=new \
  --disable-gpu \
  --disable-background-networking \
  --disable-sync \
  --user-data-dir=/private/tmp/kdy-chrome-flyer-pdf-gallery \
  --print-to-pdf=/Users/minoru/Documents/Codex/2026-05-09/leeroydotuk-ai-sales-machine-2026-google/flyer-a4.pdf \
  --print-to-pdf-no-header \
  file:///Users/minoru/Documents/Codex/2026-05-09/leeroydotuk-ai-sales-machine-2026-google/flyer.html
```

PDFを画像化して確認:

```sh
sips -s format png flyer-a4.pdf --out flyer-a4-check.png
```

ページ数確認:

```sh
strings flyer-a4.pdf | rg '^/Count '
```

`/Count 1` なら1ページ。

## 2026-05-10 進捗（Claude Code側で対応）

- LINE自動応答 `サンプル希望` を公開URL入り＋他業種対応の確定文面に差し替え（管理画面反映済み）。
- サンプルHPのスマホ表示修正：
  - h1/h2 のスマホ用フォントサイズを縮小（`clamp(28px,7.6vw,38px)` / `clamp(22px,6.4vw,30px)`）。
  - 見出しに `<br>` を入れて改行位置を固定：
    - `外構は、暮らしやすさまで / 考えてつくる。`（2段）
    - `外構で後悔しやすい / ポイントを先に / 一緒に確認します。`（3段）※読点削除済
    - `写真で変化が伝わると、 / 相談前の不安が減ります。`（2段）
    - `外構のこと、まずは写真 / 1枚からご相談ください。`（2段）
  - 「親子で...」「お客様の声」h2 は1段で表示（フォント縮小で自動折り返し回避）。
  - GitHub Desktop経由で push 済（commit `c735521`、`978a00b`、`3ebe506`）。
- 営業用トーク作成（口頭でやり取りせず本要約のみ。会話ログ参照）。
  - 対面30秒トーク（紹介・立ち話兼用）／LINE初接触の最初の1通／食いつかれた時／断られた時の引き方。
- 初回ヒアリングシート完成：`hearing-sheet.{html,css,pdf,txt,md}` を作成。A4 1ページに収まることを `/Count 1` で確認済み。
- 制作プラン整理完了：`plans.{html,css,pdf,txt}` を作成。A4 1ページ確認済み。
  - 入口プラン：5万 / 7万 / 9万。
  - おすすめセット：18万 / 23万 / 28万。
  - セットLは「営業フル装備」へ仕様変更（撮影同行・取材代行はNGなのでリモート完結に：A4チラシ／Googleマップ整備／簡易ロゴ／写真レタッチ15枚／LINE自動応答5本／スライドショー動画1本）。
  - 名刺オプション：1万 / 1.5万 / 2.5万 / 4万。
  - 維持・運用：チケット制 5,000円/件、月額メンテ 1万円/月（3営業日以内対応・24h対応は付けない）、ドメイン代年1,500〜2,000円実費。
  - サーバー代金は Cloudflare Workers + D1 + GitHub Pages 構成で実質無料。維持コストはドメイン代のみ。

## 次にやると良さそうなこと

1. チラシの最終文言チェック
   - 「お借りした写真」など、営業先に違和感がないか確認。
   - “御社”が硬すぎる場合は「あなたのお店」「貴社」などに調整。

2. プラン表PDF（`plans.pdf`）を実際に紙印刷して、サンプルHPサンプル＋A4チラシ＋プラン表の3点セットで営業現場に持ち出す。

3. ヒアリングシート（`hearing-sheet.txt`）をiPhoneメモアプリにコピペし、初回相談時の埋めやすさを実地検証。

4. 業種展開：外構以外（電気・水道・大工・造園・石材店）向けのサンプル設定をいつ作るか検討。
   - 現サンプルのテンプレを流用し、業種別バリエーションを増やすかどうか。

5. リアル営業の振り返り運用
   - 紙で渡した相手・反応・次のアクションを `hearing-sheet` で記録。
   - 月1で「決まった/未決まり/紹介」をリスト化。

6. 月額メンテ／チケット制の導入時に、決済導線を決める（口座振込・PayPay請求書払い・Stripeなど）。

## Claude Codeに渡す時の依頼文例

```txt
このフォルダの HANDOFF.md を読んで、Codexで進めていた作業を引き継いでください。

目的は、KDY Officeの職人さん・施工店向けHP制作営業のために、
サンプルHPとA4チラシをブラッシュアップし、営業に使える状態にすることです。

まずは HANDOFF.md、flyer.html、flyer.css、index.html、styles.css を読んで、
現状を把握してください。

そのうえで、私の次の指示に従って続きから作業してください。
既存の意図やデザイン方針を壊さず、A4 PDFで切れないことを必ず確認してください。
```

## 重要な進め方

- ユーザーは営業の現場感を重視する。
- デザインだけではなく「これを渡した相手がどう感じるか」を一緒に考える。
- 反対意見がある場合は、遠慮せず伝える。ただし代替案も出す。
- 安売りしすぎない。
- でも最初は実績作りが必要なので、入口商品は用意する。
- チラシやサンプルHPは「職人さんが見てわかる言葉」にする。
- 専門用語やWeb制作者目線の説明に寄せすぎない。
