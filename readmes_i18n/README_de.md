# TransReadMe

Dieses Projekt zielt darauf ab, mithilfe der OpenAI-API eine Quell-README-Datei in mehrere Sprachen zu übersetzen und entsprechende README-Dateien zu generieren. Dieses Skript erkennt automatisch die Sprache der Quell-README und generiert Übersetzungsversionen in den Zielsprachen.

## Funktionen

- Automatische Erkennung der Sprache der Quell-README
- Übersetzung der README-Datei in mehrere Zielsprachen
- Speichern der übersetzten README-Dateien in einem angegebenen Verzeichnis
- Generierung einer README-Datei in der Standardsprache im Stammverzeichnis

## Installation

Laden Sie den Code in das Stammverzeichnis des Repositorys herunter
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## Konfiguration

Bevor Sie das Skript verwenden, müssen Sie Folgendes konfigurieren:

1. Legen Sie Ihren OpenAI-API-Schlüssel fest
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. Legen Sie den Pfad zur Quell-README-Datei fest
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. Legen Sie die OpenAI-API-URL, das Modell und die Modelltemperatur fest
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   TEMPERATURE = 0
   ```

4. Legen Sie das Verzeichnis für die Speicherung der übersetzten README-Dateien fest
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. Legen Sie die Standardsprache fest
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. Definieren Sie die zu übersetzenden Sprachen
   ```python
   TARGET_LANGUAGES = {
       'es': 'Spanish',
       'fr': 'French',
       'de': 'German',
       'zh-cn': 'Chinese (Simplified)',
       'ja': 'Japanese'
   }
   ```

## Verwendung

Führen Sie das Skript aus, um die übersetzten README-Dateien zu generieren:
```bash
python translate_readme.py
```

Das Skript wird:
- Den Inhalt der Quell-README-Datei lesen und übersetzen.
- Die übersetzten README-Dateien im angegebenen Verzeichnis speichern, wobei sie im Format README_Sprachcode.md benannt werden.
- Die README-Datei in der Standardsprache kopieren oder übersetzen und als README.md im Stammverzeichnis des Repositorys speichern.

## Hinweise

- Die Übersetzungsqualität hängt von der Leistung der OpenAI-API ab.
- Bitte stellen Sie die Sicherheit Ihres API-Schlüssels sicher und geben Sie ihn nicht in der Öffentlichkeit preis.