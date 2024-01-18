<!--
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## ステップ2: あなたのcodespaceにカスタムイメージを追加しましょう！

_素晴らしい仕事です！ 🎉 VS Codeを使用して最初のcodespaceを作成し、コードをプッシュしました！_

リポジトリのdev containerを設定することで、そのリポジトリ用に作成されたどのcodespaceでも、特定のプロジェクトに取り組むために必要なすべてのツールとランタイムを備えたカスタマイズされた開発環境を提供することができます。

**dev containerとは何ですか？** dev containerは、完全な機能を備えた開発環境を提供するために特別に設定されたDockerコンテナです。codespaceで作業する際は常に、仮想マシン上のdev containerを使用しています。

dev containerファイルは、codespaceを実行するデフォルトイメージをカスタマイズしたり、VS Codeの設定を行ったり、カスタムコードを実行したり、ポートを転送したりするためのJSONファイルです！

`devcontainer.json`ファイルを追加してカスタムイメージを設定しましょう。

### :keyboard: アクティビティ: devcontainer.jsonファイルを追加してcodespaceをカスタマイズする

1. リポジトリの**Code**タブに戻り、**Add file**ドロップダウンボタンをクリックし、`Create new file`をクリックします。
1. 空のテキストフィールドプロンプトに次の内容をタイプまたは貼り付けてファイルに名前を付けます。

   ```
   .devcontainer/devcontainer.json
   ```

1. 新しい **.devcontainer/devcontainer.json** ファイルの本文に、次の内容を追加します：

   ```jsonc
   {
   // この設定に名前を付ける
   "name": "はじめてのCodespace！",
   // ベースのcodespaceイメージを使用する
   "image": "mcr.microsoft.com/vscode/devcontainers/universal:latest",

   "remoteUser": "codespace",
   "overrideCommand": false
   }
   ```

1. **Commit changes**をクリックし、その後**Commit changes directly to the `main` branch**を選択します。
1. リポジトリの**Code**タブに戻り、新しいcodespaceを作成します。
1. ページの中央にある緑色の**Code**ボタンをクリックします。
1. ポップアップされるボックスの**Codespaces**タブをクリックします。
1. タブ上の`+`記号をクリックします。これにより、mainブランチ上に新しいcodespaceが作成されます。（ここに他のcodespaceがリストされていることに注意してください。）

   > codespaceが起動されるまで約2分間待ちます。

1. 前回と同様に、新しいcodespaceが実行されていることを確認します。

   使用されているイメージがGitHub Codespaces用に提供されているデフォルトイメージであることに注意してください。これにはPython、Node.js、Dockerなどのランタイムとツールが含まれています。完全なリストはこちらを参照：https://aka.ms/ghcs-default-image。 開発チームは、必要な前提条件がインストールされている任意のカスタムイメージを使用できます。詳細については、[codespace image](https://aka.ms/configure-codespace)を参照してください。

1. 約20秒待ってからこのページをリフレッシュします。そうすると、[GitHub Actions](https://docs.github.com/en/actions)によってREADMEの内容が次の指示に置き換えます。
