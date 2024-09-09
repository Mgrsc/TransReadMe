# TransReadMe

本项目旨在使用OpenAI的API将一个源README文件翻译成多种语言，并生成相应的README文件。这个脚本会自动检测源README的语言，并生成目标语言的翻译版本。

## 功能

- 自动检测源README的语言
- 将README文件翻译成多种目标语言
- 将翻译后的README文件保存到指定目录
- 生成默认展示语言的README至根目录

## 安装

下载代码到仓库根目录
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## 配置

在使用脚本前，你需要配置以下内容：

1. 设置你的OpenAI API密钥
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. 设置源README文件的路径
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. 设置OpenAI API的URL和模型
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   ```

4. 设置翻译后的README文件存放目录
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. 设置默认展示语言
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. 定义要翻译的语言
   ```python
   TARGET_LANGUAGES = {
       'es': 'Spanish',
       'fr': 'French',
       'de': 'German',
       'zh-cn': 'Chinese (Simplified)',
       'ja': 'Japanese'
   }
   ```

## 使用

运行脚本以生成翻译后的README文件：
```bash
python translate_readme.py
```

脚本会：
- 将源README文件的内容读取并翻译。
- 保存翻译后的README文件到指定目录中，以README_语言代码.md的格式命名。
- 将默认展示语言的README文件复制或翻译后保存到仓库根目录的README.md。

## 注意事项

- 翻译质量取决于OpenAI的API表现。
- 请确保API密钥的安全性，不要将其暴露在公共场合。