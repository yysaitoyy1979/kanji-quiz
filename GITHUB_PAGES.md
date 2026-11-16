# GitHub Pages・リポジトリの公開／非公開ガイド

このドキュメントでは、漢字トレーニングサイトのGitHub Pages公開と、リポジトリの公開範囲を変更する手順を説明します。

> **重要:** GitHub Pagesサイトの公開解除と、リポジトリをPrivateにする操作は別々です。サイトを止めたい場合はPagesを公開解除してください。ソースコードも見せたくない場合は、リポジトリの公開範囲もPrivateに変更します。

## GitHub Pagesでサイトを公開する

このリポジトリはビルド工程のない静的サイトです。`index.html`と問題データのJSONファイルを公開元に配置します。

1. GitHubで [kanji-quizリポジトリ](https://github.com/yysaitoyy1979/kanji-quiz)を開きます。
2. リポジトリ上部の **Settings** を選択します。
3. 左側メニューの **Pages** を開きます。
4. **Build and deployment** の **Source** で **Deploy from a branch** を選びます。
5. **Branch** で公開するブランチ（通常は`main`）とフォルダー（通常は`/(root)`）を選び、**Save** を押します。
6. Pages設定画面に表示されるサイトのURLを開き、公開を確認します。反映には数分かかることがあります。

`index.html`と、以下のJSONファイルをすべて同じ公開元ディレクトリに置いてください。

- `questions_kanji.json`
- `questions_japan.json`
- `questions_yojijukugo.json`
- `questions_kojiseigo.json`
- `questions_kotowaza.json`
- `questions_kanyouku.json`

## GitHub Pagesサイトだけを非公開にする（公開解除）

公開解除すると現在のPagesデプロイが削除され、サイトにアクセスできなくなります。リポジトリの公開範囲やファイルには影響しないため、リポジトリがPublicのままならソースコードは引き続き閲覧できます。

1. リポジトリのメインページを開き、**Settings** を選択します。
2. 左側メニューの **Pages** を開きます。
3. 公開サイトの欄にある **…** メニューを開きます。
4. **Unpublish site** を選び、確認して公開を解除します。

メニューや表示内容はGitHubの画面変更やリポジトリの状態によって異なる場合があります。サイトを再公開する場合は、Pages設定で公開元のブランチとフォルダーを設定し直してください。

## リポジトリをPrivateにする

1. リポジトリのメインページで **Settings** を開きます。
2. **General** のページ末尾にある **Danger Zone** まで移動します。
3. **Change repository visibility** の **Change visibility** を選びます。
4. **Make private** を選択し、画面の案内に従って確認します。

Privateにすると、リポジトリを閲覧できる人が制限されます。GitHub Pagesの利用可否や、公開されるサイトのアクセス制御はGitHubのプラン・設定によって異なります。**ソースコードをPrivateにしただけで、Pagesサイトも必ず非公開になるとは限りません。** サイトも停止したい場合は、Pagesの公開解除を別途行い、実際にサイトへアクセスできなくなったことを確認してください。

## リポジトリを再びPublicにする

1. リポジトリの **Settings → General → Danger Zone** を開きます。
2. **Change repository visibility** の **Change visibility** を選びます。
3. **Make public** を選択し、画面の案内に従って確認します。
4. GitHub Pagesも公開する場合は、**Settings → Pages** で公開元のブランチとフォルダーを設定し、デプロイ後に表示URLを確認します。

## 公開範囲を変更する前の確認

- Publicのリポジトリでは、コードや問題データを誰でも閲覧できます。公開してよい内容だけを置いてください。
- Privateにしても、過去に公開された情報や第三者が取得したコピーを回収できるわけではありません。
- 公開履歴にパスワード、APIトークンなどの秘密情報が含まれていた場合、リポジトリをPrivateにするだけでは不十分です。該当する認証情報を失効・変更してください。
- GitHubの画面やPagesの仕様は変更されることがあります。操作時に表示される説明も確認してください。

## 参考リンク

- [GitHub Pagesの公開解除](https://docs.github.com/en/pages/getting-started-with-github-pages/unpublishing-a-github-pages-site)
- [リポジトリの公開範囲を設定する](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility)
