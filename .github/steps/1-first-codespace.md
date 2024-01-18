<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## ステップ1: 最初のcodespaceを作成しコードをプッシュする

**ようこそ！**

**ソフトウェア開発にcodespaceを使用することの大きな利点は？** Codespaceはクラウドでホストされる開発環境です。リポジトリに設定ファイルをコミットすることでGitHub Codespaces用のプロジェクトをカスタマイズできます（configuration-as-codeとも呼ばれます）。これにより、プロジェクトのすべてのユーザーに対して繰り返し可能なcodespaceの設定が作成されます。作成するcodespaceは、GitHubによって仮想マシン上で実行されるDockerコンテナーでホストされます。必要なリソースに応じて使用するマシンのタイプを選択できます。

GitHubは、開発チームがcodespaceをカスタマイズし、最適な構成とパフォーマンスを実現するための幅広い機能を提供しています。例えば、以下のことができます:

- リポジトリからcodespaceを作成する。
- codespaceからリポジトリへコードをプッシュする。
- VS Codeを使用してコードを開発する。
- カスタムイメージでcodespaceをカスタマイズする。
- codespaceを管理する。

GitHub Codespacesを使用して開発を始めるには、テンプレートまたはリポジトリ内の任意のブランチまたはコミットからcodespaceを作成できます。テンプレートからcodespaceを作成する場合、空のテンプレートから始めるか、行っている作業に適したテンプレートを選択できます。

### :keyboard: アクティビティ: codespaceを開始する

**以下のアクティビティを進めるために別のブラウザタブを開くことをお勧めします。そうすることで、これらの指示を参照用に開いたままにしておけます。**

1. リポジトリのトップページから始めます。
1. ページの中央にある緑色の**Code**ボタンをクリックします。
1. ポップアップされるボックス内で**Codespaces**タブを選択し、次に**Create codespace on main**ボタンをクリックします。

   > codespaceが起動されるまで約2分待ちます。
   > **注意**: 仮想マシンを起動しています。

1. codespaceが実行されていることを確認します。ブラウザにはVS Codeのウェブベースエディターが表示され、以下のようなターミナルが存在するはずです:
   ![codespace1](https://user-images.githubusercontent.com/26442605/207355196-71aab43f-35a9-495b-bcfe-bf3773c2f1b3.png)

### :keyboard: アクティビティ: codespaceからリポジトリにコードをプッシュする

1. VS Codeのエクスプローラウィンドウ内のcodespaceから、`index.html`ファイルを選択します。
1. 以下の内容で**h1**ヘッダーを置き換えます：

   ```html
   <h1>Hello from the codespace!</h1>
   ```

1. ファイルを保存します。
   > **注意**: ファイルは自動保存されます。
1. VS Codeのターミナルを使用して、以下のコミットメッセージを入力してファイルの変更をコミットします：

   ```shell
   git commit -a -m "Adding hello from the codespace!"
   ```

1. リポジトリに変更をプッシュします。VS Codeのターミナルで、次を入力します：

   ```shell
   git push
   ```

1. あなたのコードはリポジトリにプッシュされました！
1. リポジトリのホームページに戻り、`index.html`を表示して、新しいコードがリポジトリにプッシュされたことを確認します。
1. 約20秒待ってからこのページをリフレッシュします。そうすると、[GitHub Actions](https://docs.github.com/en/actions)によってREADMEの内容が次の指示に置き換えます。
