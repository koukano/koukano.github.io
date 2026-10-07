# 個人学術サイトのトップページ運用

- サイト名・説明・GitHub URLは `_data/academic.json` で変更する。
- トップページとAboutだけが `_layouts/academic.html` と `css/academic.css` を使用する。
- 既存数学記事・分野別一覧は、従来のレイアウト・CSS・数式表示・URLを維持する。
- 数学記事は削除・移動せず、従来どおり `articles/*.md` に追加する。
- トップページの「記事を探す」は記事のMarkdownメタデータからビルド時に自動生成する。転送用ページは除外する。
- 哲学記事を `articles/` に追加する場合は `category: philosophy`、`category_label: 哲学` を指定する。哲学本文には `layout: academic` を使用できる（数学用レイアウトの参考文献を流用しない）。本文の先頭にh1で記事名を置く。
- 記事には `title`、`description`、`category`、`category_label` を記載する。
- 新規記事には実際の公開日 `date: YYYY-MM-DD` を記載する。更新時は実際の更新日 `last_modified_at: YYYY-MM-DD` を更新する。これだけで「最近公開・更新した記事」に反映される。
- 日付の優先順位は `last_modified_at` → `updated` → `date` → `_data/article_updates.json`。
- 既存記事に日付がなかったため、2026年10月8日の改修時にGitの実際のファイル更新日時を `_data/article_updates.json` に記録した。本文を変更せず、公開日を推測しないための初期データ。今後の更新日はMarkdown側で管理する。
- 日付のない新規記事も「記事を探す」には表示されるが、「最近公開・更新した記事」には表示されない。
- 記事URLはJekyllが生成する `page.url` を使用する。既存の `/#topics`、`/#articles`、`/#about` アンカーも維持する。
- 新しい通常ページを追加した場合は `sitemap.xml` に追記する。記事は従来どおり自動追加される。
- 公開手順は `AGENTS.md` に従い、GitHub Pagesの既存の自動ビルド・公開を利用する。
