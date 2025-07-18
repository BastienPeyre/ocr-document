# 🚚 Analyseur de Documents de Transport avec OCR

Interface web moderne pour l'analyse automatique de documents de transport routier avec reconnaissance optique de caractères (OCR).

## 🎯 Fonctionnalités

### Interface utilisateur
- **Zone de prompt** : Saisie personnalisée des instructions d'analyse
- **Upload de fichiers** : Support PDF et images avec glisser-déposer
- **Prévisualisation** : Affichage en temps réel des documents uploadés
- **Résultats interactifs** : Visualisation des données extraites avec mise en évidence

### Capacités techniques
- ✅ Support des formats PDF, JPEG, PNG, GIF, BMP
- ✅ Rendu PDF avec PDF.js
- ✅ Interface responsive (Bootstrap 5)
- ✅ Animations et transitions fluides
- ✅ Système de mise en évidence interactive
- ✅ Gestion d'erreurs robuste
- ✅ Mode démo intégré

## 🛠️ Technologies utilisées

- **Frontend** : HTML5, CSS3, JavaScript ES6
- **Frameworks** : Bootstrap 5.3, jQuery 3.7
- **Rendu PDF** : PDF.js 3.11
- **Icons** : Font Awesome 6.0
- **API** : Appels REST en JSON

## 📋 Format des données

### Requête API
```json
{
  "document": "data:application/pdf;base64,JVBERi0xLjQK...",
  "prompt": "Extraire les informations suivantes du document...",
  "filename": "document.pdf",
  "fileType": "application/pdf"
}
```

### Réponse API attendue
```json
{
  "results": [
    {
      "type": "Date de chargement",
      "value": "15/03/2024",
      "coordinates": {
        "x": 150,
        "y": 100,
        "width": 120,
        "height": 25
      }
    }
  ]
}
```

## 🚀 Installation et utilisation

1. **Cloner le repository**
   ```bash
   git clone https://github.com/BastienPeyre/ocr-document.git
   cd ocr-document
   ```

2. **Configurer l'API**
   - Ouvrir `index.html`
   - Modifier la ligne 241 :
   ```javascript
   const API_ENDPOINT = 'https://your-api-endpoint.com/analyze';
   ```

3. **Déployer**
   - Servir les fichiers via un serveur web
   - Ou ouvrir directement `index.html` dans un navigateur

## 🎨 Personnalisation

### Couleurs et thème
Les couleurs principales peuvent être modifiées dans le CSS :
```css
.section-header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

### Types d'informations
Pour ajouter de nouveaux types d'informations à extraire, modifier le prompt par défaut :
```javascript
$('#promptText').val(`Extraire les informations suivantes :
- Nouveau type d'information
- Autre information...`);
```

## 🔧 API Integration

### Endpoint requis
- **URL** : Configurable dans `API_ENDPOINT`
- **Méthode** : POST
- **Content-Type** : application/json
- **Timeout** : 30 secondes

### Gestion des erreurs
- Timeout automatique
- Fallback vers mode démo
- Messages d'erreur utilisateur
- Retry automatique possible

## 📱 Responsive Design

- **Desktop** : Layout 4 zones (2x2)
- **Tablet** : Adaptation automatique
- **Mobile** : Empilement vertical

## 🧪 Mode Démo

Un mode démo est intégré avec des données simulées pour tester l'interface sans backend.

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à :
- Ouvrir des issues pour les bugs
- Proposer des améliorations
- Soumettre des pull requests

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 🔗 Liens utiles

- [Bootstrap Documentation](https://getbootstrap.com/docs/5.3/)
- [jQuery Documentation](https://jquery.com/)
- [PDF.js Documentation](https://mozilla.github.io/pdf.js/)
- [Font Awesome Icons](https://fontawesome.com/)

---

**Développé avec ❤️ pour l'analyse de documents de transport**