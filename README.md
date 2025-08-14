# MiroThinker-GG-COLAB

## 📌 Description
Ce repository contient un **Google Colab** prêt à l’emploi pour exécuter le modèle **MiroThinker** issu de l’initiative **MiroMind Open Deep Research (ODR) v0.1**.  
L’objectif est de permettre à n’importe quel utilisateur de tester un **LLM open-weight** spécialisé dans la recherche et le raisonnement avancé, directement dans un environnement GPU Colab.

## 🚀 Fonctionnalités
- Chargement **direct depuis Hugging Face** (`miromind-ai/MiroThinker-*`).
- Support de plusieurs tailles de modèles : **8B**, **14B** et **32B**.
- Chargement optimisé en **4-bit** pour réduire la consommation VRAM.
- Exécution sur GPU **T4**, **L4** ou **A100** via Colab.
- Bloc de génération simple pour tester rapidement des prompts.
- Compatible avec les versions **SFT** et **DPO**.

## 📂 Structure du Notebook
- **Cellule 1 — Vérifs & setup** : vérifie l’environnement et la disponibilité GPU.
- **Cellule 2 — Installation des dépendances** : installe `transformers`, `accelerate`, `bitsandbytes` et autres packages nécessaires.
- **Cellule 3 — Choix du modèle** : sélection de la version (`8B`, `14B`, `32B`) et du type (`SFT` ou `DPO`).
- **Cellule 4 — Chargement 4-bit** : configuration et chargement du modèle en VRAM optimisée.
- **Cellule 5 — TEST: Génération simple** : exécution d’un prompt libre pour valider le fonctionnement.

## 📦 Installation et exécution
1. Ouvrir le notebook dans Google Colab.
2. Passer l’exécution en **GPU** :  
   `Exécution > Modifier le type d’exécution > Accélérateur matériel : GPU`
3. Lancer les cellules dans l’ordre.
4. Choisir le modèle Hugging Face dans la **Cellule 3** (ex. : `miromind-ai/MiroThinker-32B-DPO-v0.1`).
5. Saisir un prompt dans la **Cellule 5** pour générer du texte.

## 💡 Conseils d’utilisation
- Sur un **T4 (16 Go)**, privilégier le 8B ou le 14B pour des réponses plus rapides.  
- Le **32B-DPO** est plus qualitatif mais plus lent en 4-bit sur T4.  
- Pour des performances optimales, utiliser un **A100** ou **L4** si disponible.  
- Adapter le `max_new_tokens` selon la longueur souhaitée.

## 📜 Licence
Ce notebook utilise uniquement des **modèles open-weight** publiés par [MiroMindAI](https://huggingface.co/miromind-ai).  
Vérifiez la licence associée à chaque modèle sur Hugging Face avant utilisation.
