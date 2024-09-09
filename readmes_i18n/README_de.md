# TransReadMe

Dieses Projekt zielt darauf ab, mithilfe der OpenAI-API eine Quell-README-Datei in mehrere Sprachen zu übersetzen und die entsprechenden README-Dateien zu erstellen. Dieses Skript erkennt automatisch die Sprache der Quell-README und erstellt eine Übersetzung in die Zielsprache.

## Funktionen

- Automatische Erkennung der Sprache der Quell-README
- Übersetzung der README-Datei in mehrere Zielsprachen
- Speichern der übersetzten README-Datei in einem angegebenen Verzeichnis
- Erstellen einer README in der Standardsprache im Stammverzeichnis

## Installation

Laden Sie den Code in das Stammverzeichnis des Repositories herunter
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## Konfiguration

Vor der Verwendung des Skripts müssen Sie Folgendes konfigurieren:

1. Ihren OpenAI API-Schlüssel festlegen
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. Den Pfad zur Quell-README-Datei festlegen
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. Die URL und das Modell der OpenAI API festlegen
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   ```

4. Das Verzeichnis für die übersetzten README-Dateien festlegen
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. Die Standardsprache für die Anzeige festlegen
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. Die zu übersetzenden Sprachen definieren
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

Führen Sie das Skript aus, um die übersetzten README-Dateien zu erstellen:
```bash
python translate_readme.py
```

Das Skript wird:
- Den Inhalt der Quell-README lesen und übersetzen.
- Die übersetzten README-Dateien im angegebenen Verzeichnis speichern, im Format README_Sprachenkürzel.md.
- Die README-Datei in der Standardsprache im Stammverzeichnis des Repositories kopieren oder übersetzen und als README.md speichern.

## Hinweise

- Die Übersetzungsqualität hängt von der Leistung der OpenAI-API ab.
- Achten Sie auf die Sicherheit des API-Schlüssels und vermeiden Sie dessen Veröffentlichung in der Öffentlichkeit.