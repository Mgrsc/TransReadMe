# TransReadMe

このプロジェクトは、OpenAIのAPIを使用して、ソースREADMEファイルを多言語に翻訳し、対応するREADMEファイルを生成することを目的としています。このスクリプトは、ソースREADMEの言語を自動的に検出し、ターゲット言語の翻訳版を生成します。

## 機能

- ソースREADMEの言語を自動検出
- READMEファイルを複数のターゲット言語に翻訳
- 翻訳されたREADMEファイルを指定されたディレクトリに保存
- デフォルト表示言語のREADMEをルートディレクトリに生成

## インストール

コードをリポジトリのルートディレクトリにダウンロードします。
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## 設定

スクリプトを使用する前に、以下の内容を設定する必要があります。

1. OpenAI APIキーを設定します。
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. ソースREADMEファイルのパスを設定します。
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. OpenAI APIのURL、モデル、およびモデル温度を設定します。
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   TEMPERATURE = 0
   ```

4. 翻訳されたREADMEファイルの保存先ディレクトリを設定します。
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. デフォルト表示言語を設定します。
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. 翻訳する言語を定義します。
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

スクリプトを実行して、翻訳されたREADMEファイルを生成します。
```bash
python translate_readme.py
```

スクリプトは以下の処理を行います。
- ソースREADMEファイルの内容を読み込み、翻訳します。
- 翻訳されたREADMEファイルを、指定されたディレクトリにREADME_言語コード.mdの形式で保存します。
- デフォルト表示言語のREADMEファイルを、コピーまたは翻訳して、リポジトリのルートディレクトリにREADME.mdとして保存します。

## 注意事項

- 翻訳品質はOpenAIのAPIの性能に依存します。
- APIキーのセキュリティを確保し、公共の場に公開しないでください。