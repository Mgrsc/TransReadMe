# TransReadMe

Este proyecto tiene como objetivo utilizar la API de OpenAI para traducir un archivo README fuente a varios idiomas y generar los archivos README correspondientes. Este script detecta automáticamente el idioma del README fuente y genera versiones traducidas en los idiomas de destino.

## Funcionalidades

- Detección automática del idioma del README fuente
- Traducción del archivo README a varios idiomas de destino
- Guardado de los archivos README traducidos en el directorio especificado
- Generación del README en el idioma de visualización predeterminado en el directorio raíz

## Instalación

Descarga el código al directorio raíz del repositorio
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## Configuración

Antes de usar el script, debes configurar lo siguiente:

1. Configura tu clave de API de OpenAI
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. Configura la ruta del archivo README fuente
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. Configura la URL de la API de OpenAI, el modelo y la temperatura del modelo
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   TEMPERATURE = 0
   ```

4. Configura el directorio donde se guardarán los archivos README traducidos
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. Configura el idioma de visualización predeterminado
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. Define los idiomas a traducir
   ```python
   TARGET_LANGUAGES = {
       'es': 'Spanish',
       'fr': 'French',
       'de': 'German',
       'zh-cn': 'Chinese (Simplified)',
       'ja': 'Japanese'
   }
   ```

## Uso

Ejecuta el script para generar los archivos README traducidos:
```bash
python translate_readme.py
```

El script hará lo siguiente:
- Leerá y traducirá el contenido del archivo README fuente.
- Guardará los archivos README traducidos en el directorio especificado, nombrándolos con el formato README_código_de_idioma.md.
- Copiará o traducirá el archivo README en el idioma de visualización predeterminado y lo guardará como README.md en el directorio raíz del repositorio.

## Notas

- La calidad de la traducción depende del rendimiento de la API de OpenAI.
- Asegúrate de la seguridad de tu clave de API y no la expongas en lugares públicos.