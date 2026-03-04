# 🧹 Ops Cleaning — Application de gestion opérations

Application web autonome (sans serveur, sans dépendances) pour gérer les opérations d'une entreprise de nettoyage.

## 🚀 Démarrage rapide

1. **Ouvrez `index.html`** dans votre navigateur
2. Allez dans **Import/Export → Charger données démo** pour tester avec des données réalistes
3. Explorez les 9 modules : Dashboard, Planning, Missions, Employés, Sites, Stocks, Objectifs, Paramètres

## 📁 Structure des fichiers

```
ops-cleaning/
├── index.html              # Point d'entrée de l'application
├── app.css                 # Design system complet (~600 lignes)
├── app.js                  # Logique applicative (~300 lignes compressées)
├── config.company.json     # Configuration entreprise (couleurs, règles, types)
├── seed.demo.json          # Données de démonstration
└── data.schema.json        # Schémas de validation des données
```

## 🎨 Personnalisation pour votre entreprise

### 1. Identité visuelle (config.company.json)
Modifiez le fichier `config.company.json` :
```json
{
  "company": {
    "name": "Ma Société",
    "primaryColor": "#votre-couleur",
    "secondaryColor": "#couleur-secondaire"
  }
}
```

Ou directement depuis **Paramètres → Entreprise** dans l'application.

### 2. Types de prestations
Configurez vos propres types (ménage, vitres, bureaux, etc.) avec icônes, couleurs et vitesses de référence dans **Paramètres → Types prestation**.

### 3. Zones géographiques
Définissez vos zones d'intervention avec codes postaux dans **Paramètres → Zones**.

### 4. Règles métier
Ajustez le coût horaire, la marge cible, les temps de trajet et objectifs KPI dans **Paramètres → Règles métier**.

## 💾 Stockage des données

Les données sont stockées localement dans le **localStorage** de votre navigateur. Pour sauvegarder :
- **Export complet** : Import/Export → Tout exporter (JSON)
- **Restore** : Import/Export → Importer le fichier JSON

## 🔧 Modules disponibles

| Module | Description |
|--------|-------------|
| 📊 Dashboard | KPIs temps réel, prochaines missions, charge équipe |
| 📅 Planning | Grille semaine/jour, suggestion automatique, conflits |
| 📋 Missions | CRUD complet, checklists, scores qualité, impression |
| 👥 Employés | Compétences, horaires, zones, coûts |
| 🏢 Sites/Clients | Fiche site, codes accès, historique qualité |
| 📦 Stocks | Alertes seuils, liste réapprovisionnement |
| 🎯 Objectifs | Suivi KPIs, taux completion, CA mensuel |
| ⚙️ Paramètres | Config entreprise, règles métier, types, zones |
| 📤 Import/Export | Backup JSON/CSV, données démo, reset |

## 📱 Responsive

L'application fonctionne sur desktop et mobile. Sur mobile, le menu se replie automatiquement.

## 🖨️ Impression

Les fiches missions sont imprimables via le bouton "Imprimer" dans le détail d'une mission.

---

**Version** : 1.0 | **Compatible** : Chrome, Firefox, Safari, Edge (ES6+)
