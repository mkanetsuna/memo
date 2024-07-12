# GitHub Codespacesでのプルリクエスト作成手順

## 1. Codespacesの起動

1. **リポジトリページにアクセス**：
    - GitHubのリポジトリページにアクセスする。

2. **Codespacesを起動**：
    - 画面右上の「Code」ボタンをクリックし、「Codespaces」タブを選択する。
    - 既存のCodespaceを選択するか、新しいCodespaceを作成する。

## 2. 新しいブランチの作成

1. **新しいブランチを作成**：
    - Codespacesが起動したら、ターミナルを開き、新しいブランチを作成する。
    ```sh
    git checkout -b my-new-feature
    ```

## 3. コードの変更とコミット

1. **コードを変更**:
    - エディタでファイルを編集し、変更を加える。

2. **変更をステージング**:
    ```sh
    git add .
    ```

3. **変更をコミット**:
    ```sh
    git commit -m "Add new feature"
    ```

## 4. ブランチのプッシュ

1. **ブランチをリモートにプッシュ**:
    ```sh
    git push origin my-new-feature
    ```

## 5. プルリクエストの作成

1. **GitHub CLI (gh)をインストール**:
    ```sh
    sudo apt update && sudo apt install gh
    ```

2. **GitHub CLIでログイン**:
    ```sh
    gh auth login
    ```

3. **プルリクエストの作成**:
    ```sh
    gh pr create --base main --head my-new-feature --title "Add new feature" --body "This PR adds a new feature."
    ```
    - `--base`: マージ先のブランチ(通常は`main`)
    - `--head`: プルリクエストの元になるブランチ(作成したブランチ`my-new-feature`)
    - `--title`: プルリクエストのタイトル
    - `--body`: プルリクエストの詳細な説明