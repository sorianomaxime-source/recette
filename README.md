# Mon Menu Semaine 🍽️

Une application web moderne pour planifier vos menus hebdomadaires, calculer les calories et générer des listes de courses intelligentes. Inclut désormais une fonctionnalité de scan de recettes par IA !

## ✨ Fonctionnalités

- **Sélection de recettes** : Bibliothèque de recettes avec temps, difficulté et calories par personne
- **Calcul automatique des calories** : Indicateurs colorés (vert < 600 kcal, orange 600-899 kcal, rouge ≥ 900 kcal)
- **Planification hebdomadaire** : Organisation des repas avec suivi des objectifs et du nombre de personnes
- **Liste de courses intelligente** : Génération automatique d'ingrédients regroupés par catégories
- **📷 Scan de recettes par IA** : Analysez des photos de recettes avec Gemini 2.5 Flash (Google AI)
- **Historique des semaines** : Sauvegardez et rechargez vos planifications passées
- **Export Carrefour Drive** : Exportez vos listes de courses au format Carrefour
- **Synchronisation cloud** : Stockage local avec option Supabase
- **Interface responsive** : Design moderne et adaptatif

## 🚀 Installation

1. Téléchargez `index.html`
2. Ouvrez-le dans votre navigateur (Chrome, Firefox, Safari, Edge)
3. Aucune installation requise !

## 📖 Utilisation

### Premiers pas
L'application comporte 5 onglets : **Recettes**, **Semaine**, **Courses**, **Scanner**, **Historique**

### Sélectionner des recettes
- Onglet "Recettes" : Parcourez et sélectionnez des recettes
- Chaque recette affiche : emoji, nom, temps, difficulté, calories avec code couleur

### Planifier la semaine
- Configurez le nombre de repas et de personnes en haut
- Les recettes sélectionnées apparaissent dans "Semaine" avec calcul automatique des calories totales

### Générer les courses
- Onglet "Courses" : Liste d'ingrédients regroupés par catégories
- Cases à cocher pour suivre vos achats

### 📷 Scanner une recette
- Onglet "Scanner" : Fonctionnalité IA pour analyser des photos de recettes
- **Configuration requise** :
  1. Obtenez une clé API gratuite sur [ai.google.dev](https://ai.google.dev)
  2. Entrez votre clé API Google AI dans le champ prévu
  3. Photographiez une fiche recette
  4. Glissez-déposez ou cliquez pour uploader l'image
- L'IA extrait automatiquement : nom, ingrédients, quantités, temps de préparation, calories

### Gérer l'historique
- Sauvegardez vos semaines
- Rechargez ou exportez des planifications passées

## 🛠️ Technologies

- **Frontend** : HTML5, CSS3 (variables CSS), JavaScript ES6+
- **Stockage** : IndexedDB (local) + Supabase (cloud optionnel)
- **IA** : Google Gemini 2.5 Flash pour l'analyse d'images
- **API** : Google AI Studio (clé API requise pour le scan)

## 📁 Structure

```
/
├── index.html    # Application complète (HTML + CSS + JS)
└── README.md     # Documentation
```

## 🎨 Personnalisation

### Seuils caloriques
Modifiez `calStyle(kcal)` dans le code :
```javascript
function calStyle(k) {
  if (k < 600) return { bg:'#EAF3DE', color:'#3B6D11' };  // Vert
  if (k < 900) return { bg:'#FAEEDA', color:'#854F0B' };  // Orange
  return { bg:'#FCEBEB', color:'#A32D2D' };               // Rouge
}
```

### Ajouter des recettes
Utilisez le bouton "+" ou scannez des photos de recettes.

## 🔐 Configuration IA

Pour utiliser le scan de recettes :
1. Créez un compte sur [Google AI Studio](https://ai.google.dev)
2. Générez une clé API gratuite
3. Entrez-la dans l'application (stockée localement uniquement)

## 🤝 Contribution

Contributions bienvenues ! Forkez et proposez vos améliorations.

## 📄 Licence

MIT License - voir [LICENSE](LICENSE) pour les détails.

---

**Développé avec ❤️ pour simplifier votre planification alimentaire**
