# Tuteur IA - AskGL

Tuteur IA académique pour étudiants en génie logiciel avec système de calcul de notes intégré.

## Fonctionnalités

- **Chatbot IA** : Assistant pédagogique pour les matières informatiques et mathématiques
- **Calcul de Notes** : Système de calcul des moyennes pour les modules de génie logiciel
- **Support Multi-Niveaux** : Niveaux 1, 2 et 3 avec parcours spécialisés (Génie Logiciel, Réseaux et Internet)
- **Interface Moderne** : Design responsive avec thème sombre premium

## Technologies

- **Backend** : FastAPI (Python)
- **Frontend** : HTML/CSS/JavaScript vanilla
- **IA** : OpenAI GPT-4o-mini et Google Gemini 2.0
- **Déploiement** : Vercel

## Installation Locale

```bash
# Cloner le repository
git clone https://github.com/Mdg-clood/TUTEUR-IA.git
cd TUTEUR-IA

# Installer les dépendances
pip install -r requirements.txt

# Configurer les variables d'environnement
cp .env.example .env
# Éditez .env avec vos clés API

# Lancer le serveur
uvicorn main:app --reload --host 0.0.0.0
```

Accédez à http://localhost:8000

## Variables d'Environnement

- `OPENAI_API_KEY` : Clé API OpenAI ou Google Gemini
- `OPENAI_MODEL` : Modèle OpenAI (défaut: gpt-4o-mini)
- `GEMINI_MODEL` : Modèle Gemini (défaut: gemini-2.0-flash-lite)
- `TUTOR_NAME` : Nom du tuteur (défaut: AskGL)

## Déploiement sur Vercel

### Méthode 1 : Via l'interface Vercel

1. Connectez-vous sur [vercel.com](https://vercel.com)
2. Cliquez sur "Add New Project"
3. Importez depuis GitHub : `Mdg-clood/TUTEUR-IA`
4. Configurez les variables d'environnement dans "Environment Variables"
5. Cliquez sur "Deploy"

### Méthode 2 : Via CLI Vercel

```bash
# Installer Vercel CLI
npm i -g vercel

# Se connecter
vercel login

# Déployer
vercel
```

### Variables d'Environnement sur Vercel

Dans les settings du projet Vercel, ajoutez :

```
OPENAI_API_KEY = votre_clé_api
OPENAI_MODEL = gpt-4o-mini
GEMINI_MODEL = gemini-2.0-flash-lite
TUTOR_NAME = AskGL
```

## Structure du Projet

```
ai-tutor-python/
├── api/
│   └── index.py          # Point d'entrée Vercel
├── static/
│   ├── app.js            # JavaScript frontend
│   ├── style.css         # Styles
│   └── hero-logo.png     # Logo
├── templates/
│   ├── index.html        # Page principale
│   └── grades.html       # Page calcul de notes
├── main.py               # Application FastAPI
├── tutor.py              # Logique IA
├── config.py             # Configuration
├── grade_calculator.py   # Calcul des notes
├── modules_config.py     # Configuration des modules
├── requirements.txt      # Dépendances Python
├── vercel.json           # Configuration Vercel
└── .env                  # Variables d'environnement (non commit)
```

## Système de Calcul de Notes

Le système calcule les moyennes selon les coefficients officiels de l'INSTA :

- **Avec TP** : CC=30%, Examen=60%, TP=40%
- **Sans TP** : CC=40%, Examen=60%
- **Validation** : Module validé si moyenne >= 10

## Matières Couvertes

### Informatique et Génie Logiciel
SQL, Python, Java, JavaScript, UML, génie logiciel, algorithmes, structures de données, bases de données, API REST, programmation web, programmation système et réseau, langage C, architecture des ordinateurs, systèmes d'exploitation, réseaux informatiques, data mining, développement mobile, administration système, interface multimédia, laboratoire Internet, systèmes distribués, base de données avancées, introduction à l'analyse des données (datamining), conception et implémentation d'applications objets, analyse des besoins et spécifications logiciels, contrôle qualité et métrique du logiciel, génie logiciel orienté objet, développement web avancé (web services), sécurité des réseaux informatiques, sécurité avancée des réseaux, administration avancée réseaux, cloud computing, cryptographie et sécurité des systèmes d'information, modélisation et conception de bases de données objets, atelier de génie logiciel, théorie des graphes, analyse numérique, programmation linéaire, électronique, électronique numérique, systèmes d'information, exploitation de bases de données relationnelles, programmation orientée objet en Java, programmation modulaire en C, atelier de programmation

### Mathématiques
Analyse, probabilité et statistique, algèbre, systèmes de numération, analyse numérique, théorie des graphes, programmation linéaire

### Physique et Électronique
Mécanique générale, électricité générale, technologie des composants électroniques, optique géométrique

### Langues et Gestion
Anglais, arabe, gestion d'entreprise, entrepreneuriat, compétences entrepreneuriales, comptabilité, économie, organisation et gestion des entreprises, droit de travail, gestion de projet, technique d'expression

## Licence

Ce projet est développé pour l'INSTA (Institut national supérieur des sciences et techniques d'Abéché).
