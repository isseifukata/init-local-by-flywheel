# Init Local by Flywheel

[Local](https://localwp.com/) で新規作成した WordPress サイトを初期化、日本語化するスクリプト。

このスクリプトを実行すると下記の設定が行われます。

- サイトの言語を `日本語` に設定
- タイムゾーンを `東京` に設定
- 日付フォーマットを `Y-m-d` に設定
- 時刻フォーマットを `H:i` に設定
- パーマリンクを投稿名に設定
- リライトルールを更新
- サンプルの投稿、固定ページを削除
- サンプルのコメントを削除
- 下記プラグインをインストール
  - [WP Multibyte Patch](https://ja.wordpress.org/plugins/wp-multibyte-patch/)
  - [Query Monitor](https://ja.wordpress.org/plugins/query-monitor/)
  - [Akismet](https://ja.wordpress.org/plugins/akismet/)
  - [Yoast SEO](https://ja.wordpress.org/plugins/wordpress-seo/)
  - [Tiny MCE Advanced](https://ja.wordpress.org/plugins/tinymce-advanced/)
  - [Duplicate Post](https://ja.wordpress.org/plugins/duplicate-post/)
  - [WP Pagenavi](https://ja.wordpress.org/plugins/wp-pagenavi/)
  - [Custom Post Type UI](https://ja.wordpress.org/plugins/custom-post-type-ui/)
  - [Really Simple SSL](https://ja.wordpress.org/plugins/really-simple-ssl/)
  - [Safe SVG](https://ja.wordpress.org/plugins/safe-svg/)
  - [All in One WP Migration](https://ja.wordpress.org/plugins/all-in-one-wp-migration/)
- WordPress 日本語コアファイルをアップデート

## 使い方

1. Local でサイトを新規作成する。
2. サイトを右クリックして `Open Site SSH` を開く。
3. コンソール上で下記コマンドを実行する。

通常のコマンド

```bash
wp eval 'exec(file_get_contents("https://raw.githubusercontent.com/isseifukata/init-local-by-flywheel/master/default.sh")." > /dev/null", $output); printf("%s\n", implode("\n", $output));'
```

プラグインを入れない場合

```bash
wp eval 'exec(file_get_contents("https://raw.githubusercontent.com/isseifukata/init-local-by-flywheel/master/no-plugin.sh")." > /dev/null", $output); printf("%s\n", implode("\n", $output));'
```
