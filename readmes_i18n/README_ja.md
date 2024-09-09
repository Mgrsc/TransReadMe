TransReadMe

本プロジェクトは、OpenAIのAPIを使用して、元のREADMEファイルを多言語に翻訳し、対応するREADMEファイルを生成することを目的としています。このスクリプトは、元のREADMEの言語を自動的に検出し、ターゲット言語の翻訳バージョンを生成します。

## 機能

- 元のREADMEの言語を自動検出
- READMEファイルを複数のターゲット言語に翻訳
- 翻訳後のREADMEファイルを指定ディレクトリに保存
- デフォルト表示言語のREADMEをルートディレクトリに生成

## インストール

コードをリポジトリのルートディレクトリにダウンロード
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## 設定

スクリプトを使用する前に、以下の内容を設定してください：

1. OpenAI APIキーを設定
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. 元のREADMEファイルのパスを設定
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. OpenAI APIのURLとモデルを設定
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   ```

4. 翻訳後のREADMEファイルの保存ディレクトリを設定
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. デフォルト表示言語を設定
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. 翻訳する言語を定義
   ```python
   TARGET_LANGUAGES = {
       'es': 'Spanish',
       'fr': 'French',
       'de': 'German',
       'zh-cn': 'Chinese (Simplified)',
       'ja': 'Japanese'
   }
   ```

## 使用方法

スクリプトを実行して翻訳後のREADMEファイルを生成：
```bash
python translate_readme.py
```

スクリプトは以下を行います：
- 元のREADMEファイルの内容を読み取り、翻訳。
- 翻訳後のREADMEファイルを指定ディレクトリに、README_言語コード.mdの形式で保存。
- デフォルト表示言語のREADMEファイルをコピーまたは翻訳後にリポジトリのルートディレクトリにREADME.mdとして保存。

## 注意事項

- 翻訳の品質はOpenAIのAPIのパフォーマンスに依存します。
- APIキーの安全性を確保し、公共の場で露出しないようにしてください。