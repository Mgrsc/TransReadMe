# TransReadMe

Este proyecto tiene como objetivo utilizar la API de OpenAI para traducir un archivo README de origen a varios idiomas y generar los archivos README correspondientes. Este script detectará automáticamente el idioma del README de origen y generará la versión traducida en el idioma objetivo.

## Funciones

- Detectar automáticamente el idioma del README de origen
- Traducir el archivo README a varios idiomas objetivo
- Guardar el archivo README traducido en el directorio especificado
- Generar el README en el idioma de visualización predeterminado en el directorio raíz

## Instalación

Descargar el código en el directorio raíz del repositorio
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## Configuración

Antes de usar el script, necesitas configurar lo siguiente:

1. Configurar tu clave API de OpenAI
   ```python
   API_KEY = 'tu_clave_api_de_openai'
   ```

2. Configurar la ruta del archivo README de origen
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. Configurar la URL y el modelo de la API de OpenAI
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   ```

4. Configurar el directorio de almacenamiento del archivo README traducido
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. Configurar el idioma de visualización predeterminado
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. Definir los idiomas a traducir
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

Ejecuta el script para generar el archivo README traducido:
```bash
python translate_readme.py
```

El script:
- Leerá y traducirá el contenido del archivo README de origen.
- Guardará el archivo README traducido en el directorio especificado, nombrándolo en el formato README_código_idioma.md.
- Copiará o traducirá el archivo README en el idioma de visualización predeterminado y lo guardará en el README.md del directorio raíz del repositorio.

## Consideraciones

- La calidad de la traducción depende del rendimiento de la API de OpenAI.
- Asegúrate de la seguridad de la clave API, no la expongas en lugares públicos.