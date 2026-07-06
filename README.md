# 幹事の道具箱（kanji-tools）

飲み会の幹事を助ける無料Webツール集。静的サイト（HTML/CSS/JSのみ・ビルド不要）。

## 中身
| ファイル | 内容 | 狙う検索ワード例 |
|---|---|---|
| `index.html` | 玄関ページ（ツール一覧・SEOの要） | 幹事 ツール、飲み会 便利 |
| `warikan.html` | 傾斜割り勘の計算 | 傾斜 割り勘、割り勘 計算、飲み会 傾斜 |
| `team.html` | チーム分け・席替え | チーム分け、班分け、席替え ランダム |
| `roulette.html` | 罰ゲームルーレット | 罰ゲーム ルーレット、お題 ルーレット |
| `styles.css` | 全ページ共通のデザイン | — |

## ローカルで見る
このフォルダで:
```
python -m http.server 8790
```
→ ブラウザで http://localhost:8790

## 公開する（無料・独自ドメイン不要）— Cloudflare Pages
1. https://dash.cloudflare.com/ で無料アカウント作成
2. 左メニュー **Workers & Pages** → **Create** → **Pages** → **Upload assets**
3. この `kanji-tools` フォルダを**丸ごとドラッグ＆ドロップ**
4. プロジェクト名（例 `kanji-toolbox`）→ Deploy
5. `https://kanji-toolbox.pages.dev` で即公開（HTTPS付き）

※ Netlify（https://app.netlify.com/drop）でもフォルダをドロップするだけで同様に公開できる。

## 公開後にやること（収益化）
1. **Google Search Console** に登録 → サイトを追加 → サイトマップ送信
   - まず「表示回数」が立つかを見る。これが動かなければ内容を増やす。
2. **Google AdSense** を申請（数ページ＋独自性のある文章が必要。各 `*.html` のフッター解説文がその役割）
   - 承認後、各HTMLの `<!-- AdSense はここ -->` 部分に発行タグを貼る。
3. `<link rel="canonical">` と OGP の `https://example.com/` を**実際のURL**に置換。

## 次に増やすツール候補（同じ型で量産可能）
- 会費シミュレータ（一次会＋二次会の合算・男女別会費）
- 出欠・集金チェック表
- あみだくじ
- 順番決め（発表順・席順）
- 宴会タイムスケジュール作成
