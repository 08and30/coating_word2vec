# coating_word2vec

Word2Vec / Doc2Vec を用いたコーティング分野のテキスト分析を行うためのプロジェクトです。

## 現在の構成

現時点ではプロジェクトの初期構成のみを用意しています。

```text
.
├── data/
└── notebook/
    ├── doc2vec/
    └── word2vec/
```

- `data/`: 学習・評価に使用するデータを配置します。
- `notebook/word2vec/`: Word2Vec 関連のノートブックを配置します。
- `notebook/doc2vec/`: Doc2Vec 関連のノートブックを配置します。

## 前提環境

- Python 3.13 で動作確認する想定です。
- Jupyter Notebook または JupyterLab を使用します。
- 必要な Python パッケージは、実装内容に合わせて依存関係ファイルを追加して管理してください。

## セットアップ

Windows の PowerShell では、次のように仮想環境を作成して有効化できます。

```powershell
py -3.13 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
```

依存関係ファイルが追加された後は、プロジェクトルートで次のコマンドを実行してください。

```powershell
python -m pip install -r requirements.txt
```

## 使い方

1. 分析対象のデータを `data/` に配置します。
2. `notebook/word2vec/` または `notebook/doc2vec/` にノートブックを追加します。
3. Jupyter を起動します。

```powershell
jupyter lab
```

### ScienceDirect API

`notebook/01_word2vec/02_word2vec.ipynb` は、ScienceDirect URLを取得するときに
`SCIENCEDIRECT_API_KEY` 環境変数のAPIキーを使用します。APIキーをソースコードや
ノートブックに書き込まないでください。

PowerShellでは、Jupyterを起動する前に次のように設定します。

```powershell
$env:SCIENCEDIRECT_API_KEY = "取得したAPIキー"
jupyter lab
```

学習済みモデル、大規模な中間生成物、実験結果はリポジトリに含めず、必要に応じて外部ストレージなどで管理してください。

## 開発時の注意

- 個人情報、認証情報、API キーなどの秘密情報をコミットしないでください。
- データの出典、ライセンス、前処理方法を各データセットまたはノートブックに記録してください。
- 再現性を保つため、依存パッケージのバージョンを依存関係ファイルで固定・管理してください。

## ライセンス

ライセンスは未定です。公開・配布する前に、プロジェクトの利用条件に合ったライセンスを追加してください。
