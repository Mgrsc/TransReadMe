# TransReadMe

This project aims to use OpenAI's API to translate a source README file into multiple languages and generate corresponding README files. The script will automatically detect the language of the source README and generate translated versions in the target languages.

## Features

- Automatically detect the language of the source README
- Translate the README file into multiple target languages
- Save the translated README files to a specified directory
- Generate a README in the default display language in the root directory

## Installation

Download the code to the root directory of the repository
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## Configuration

Before using the script, you need to configure the following:

1. Set your OpenAI API key
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. Set the path of the source README file
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. Set the OpenAI API URL and model
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   ```

4. Set the directory for storing translated README files
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. Set the default display language
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. Define the languages to translate into
   ```python
   TARGET_LANGUAGES = {
       'es': 'Spanish',
       'fr': 'French',
       'de': 'German',
       'zh-cn': 'Chinese (Simplified)',
       'ja': 'Japanese'
   }
   ```

## Usage

Run the script to generate translated README files:
```bash
python translate_readme.py
```

The script will:
- Read and translate the content of the source README file.
- Save the translated README files to the specified directory, named in the format README_language_code.md.
- Copy or translate the default display language README file and save it to the repository's root directory as README.md.

## Notes

- Translation quality depends on the performance of OpenAI's API.
- Ensure the security of the API key and do not expose it in public.