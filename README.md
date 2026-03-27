# 🧥 Segmentation d'Images avec Hugging Face SegFormer

Un notebook Python qui utilise l'API d'inférence Hugging Face pour détecter et segmenter automatiquement les vêtements et parties du corps dans des images, grâce au modèle **SegFormer B3**.

---

## 📌 Description

Ce projet permet d'analyser des images de personnes et d'identifier pixel par pixel les différents éléments vestimentaires et corporels : chapeau, cheveux, vêtements du haut, pantalon, robe, chaussures, visage, etc.

Le modèle utilisé est [`sayeed99/segformer_b3_clothes`](https://huggingface.co/sayeed99/segformer_b3_clothes), hébergé sur Hugging Face.

---

## 🗂️ Classes détectées

| ID | Classe         | ID | Classe       |
|----|----------------|----|--------------|
| 0  | Background     | 9  | Left-shoe    |
| 1  | Hat            | 10 | Right-shoe   |
| 2  | Hair           | 11 | Face         |
| 3  | Sunglasses     | 12 | Left-leg     |
| 4  | Upper-clothes  | 13 | Right-leg    |
| 5  | Skirt          | 14 | Left-arm     |
| 6  | Pants          | 15 | Right-arm    |
| 7  | Dress          | 16 | Bag          |
| 8  | Belt           | 17 | Scarf        |

---

## ⚙️ Installation

### 1. Cloner le dépôt

```bash
git clone https://github.com/TON_USERNAME/NOM_DU_REPO.git
cd NOM_DU_REPO
```

### 2. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 3. Configurer le token API

Crée un fichier `.env` à la racine du projet :

```
API_TOKEN=ton_token_huggingface_ici
```

> 💡 **Comment obtenir un token ?**
> 1. Crée un compte sur [huggingface.co](https://huggingface.co/)
> 2. Va dans **Settings → Access Tokens**
> 3. Génère un token avec le rôle `read`

---

## 🚀 Utilisation

1. Ajoute tes images (`.jpg` ou `.png`) dans un dossier local
2. Ouvre le notebook `hugging_face_segformer.ipynb` dans Jupyter
3. Modifie la variable `image_dir` avec le chemin de ton dossier d'images
4. Exécute les cellules dans l'ordre

Le notebook propose deux modes :
- **Image unique** : traitement et visualisation d'une seule image
- **Batch** : traitement automatique de plusieurs images avec barre de progression

---

## 📦 Dépendances

```
requests
Pillow
matplotlib
numpy
tqdm
python-dotenv
```

---

## 📁 Structure du projet

```
├── hugging_face_segformer.ipynb   # Notebook principal
├── .env                           # Token API (non versionné)
├── .gitignore                     # Fichiers exclus de Git
├── requirements.txt               # Dépendances Python
└── README.md                      # Ce fichier
```

---

## ⚠️ Sécurité

- Ne commitez **jamais** votre fichier `.env` sur GitHub
- Le fichier `.gitignore` est configuré pour l'exclure automatiquement

---

## 📄 Licence

Ce projet est libre d'utilisation à des fins éducatives.
