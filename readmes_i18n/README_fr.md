# TransReadMe

Ce projet vise à utiliser l'API d'OpenAI pour traduire un fichier README source en plusieurs langues et générer les fichiers README correspondants. Ce script détecte automatiquement la langue du README source et génère des versions traduites dans les langues cibles.

## Fonctionnalités

- Détection automatique de la langue du README source
- Traduction du fichier README en plusieurs langues cibles
- Enregistrement des fichiers README traduits dans un répertoire spécifié
- Génération du README dans la langue d'affichage par défaut à la racine du répertoire

## Installation

Téléchargez le code dans le répertoire racine du dépôt
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## Configuration

Avant d'utiliser le script, vous devez configurer les éléments suivants :

1. Définissez votre clé API OpenAI
   ```python
   API_KEY = 'your_openai_api_key'
   ```

2. Définissez le chemin du fichier README source
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. Définissez l'URL de l'API OpenAI, le modèle et la température du modèle
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   TEMPERATURE = 0
   ```

4. Définissez le répertoire de stockage des fichiers README traduits
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. Définissez la langue d'affichage par défaut
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. Définissez les langues à traduire
   ```python
   TARGET_LANGUAGES = {
       'es': 'Spanish',
       'fr': 'French',
       'de': 'German',
       'zh-cn': 'Chinese (Simplified)',
       'ja': 'Japanese'
   }
   ```

## Utilisation

Exécutez le script pour générer les fichiers README traduits :
```bash
python translate_readme.py
```

Le script va :
- Lire et traduire le contenu du fichier README source.
- Enregistrer les fichiers README traduits dans le répertoire spécifié, en les nommant au format README_code_langue.md.
- Copier ou traduire le fichier README dans la langue d'affichage par défaut et l'enregistrer dans le fichier README.md à la racine du dépôt.

## Remarques

- La qualité de la traduction dépend des performances de l'API d'OpenAI.
- Veuillez assurer la sécurité de votre clé API et ne pas l'exposer publiquement.