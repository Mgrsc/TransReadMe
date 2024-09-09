# TransReadMe

Ce projet vise à utiliser l'API d'OpenAI pour traduire un fichier README source en plusieurs langues et générer les fichiers README correspondants. Ce script détectera automatiquement la langue du README source et générera une version traduite dans la langue cible.

## Fonctionnalités

- Détection automatique de la langue du README source
- Traduction du fichier README en plusieurs langues cibles
- Sauvegarde des fichiers README traduits dans le répertoire spécifié
- Génération du README dans la langue d'affichage par défaut à la racine du répertoire

## Installation

Téléchargez le code dans le répertoire racine du dépôt
```
curl -fsSLO https://raw.githubusercontent.com/Mgrsc/TransReadMe/main/trans_readme.py
```

## Configuration

Avant d'utiliser le script, vous devez configurer les éléments suivants :

1. Définir votre clé API OpenAI
   ```python
   API_KEY = 'votre_clé_api_openai'
   ```

2. Définir le chemin du fichier README source
   ```python
   SOURCE_README_PATH = 'readmes_i18n/README_zh-cn.md'
   ```

3. Définir l'URL et le modèle de l'API OpenAI
   ```python
   BASE_API_URL = 'https://xxxx.xxx/v1/chat/completions'
   MODEL = 'gpt-4o'
   ```

4. Définir le répertoire de stockage des fichiers README traduits
   ```python
   OUTPUT_DIR = 'readmes_i18n'
   ```

5. Définir la langue d'affichage par défaut
   ```python
   DEFAULT_DISPLAY_LANGUAGE = 'zh-cn'
   ```

6. Définir les langues à traduire
   ```python
   TARGET_LANGUAGES = {
       'es': 'Espagnol',
       'fr': 'Français',
       'de': 'Allemand',
       'zh-cn': 'Chinois (Simplifié)',
       'ja': 'Japonais'
   }
   ```

## Utilisation

Exécutez le script pour générer les fichiers README traduits :
```bash
python translate_readme.py
```

Le script va :
- Lire et traduire le contenu du fichier README source.
- Sauvegarder les fichiers README traduits dans le répertoire spécifié, en les nommant au format README_code_langue.md.
- Copier ou traduire le fichier README dans la langue d'affichage par défaut et le sauvegarder à la racine du dépôt sous README.md.

## Remarques

- La qualité de la traduction dépend des performances de l'API d'OpenAI.
- Assurez-vous de la sécurité de votre clé API, ne la divulguez pas publiquement.