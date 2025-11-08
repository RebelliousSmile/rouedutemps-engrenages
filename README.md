# La Roue du Temps : Engrenages

Projet **guide de jeu** pour l'univers **La Roue du Temps** (Robert Jordan)

---

## Type de projet

**Guide de jeu complet** : Règles, création de personnages, système de jeu, bestiaire et annexes pour jouer dans l'univers de La Roue du Temps avec le système Engrenages.

## Description

Ce document propose une adaptation complète du système **Engrenages** (d'Alexandre Clavel) pour l'univers de **La Roue du Temps** de Robert Jordan.

Le guide couvre :
- Les règles de base adaptées à l'univers WoT
- La création de personnages avec origines culturelles
- Le système du Pouvoir Unique (*saidin* et *saidar*)
- Les combats et conflits
- Les conseils de maîtrise
- Un bestiaire complet
- Les dimensions parallèles (Tel'aran'rhiod, etc.)
- Des annexes de référence

**Statut actuel :** Version 2.0 - Structure simplifiée (13 chapitres)

---

## Structure du projet

```
rouedutemps-engrenages/
├── README.md                       # Ce fichier
├── sommaire.md                     # Table des matières détaillée (v2.0)
├── main.tex                        # Document LaTeX principal (NOUVEAU)
├── moteur-jeu.md                   # Référence des règles de base
│
├── first-draft/                    # Chapitres en Markdown (13 fichiers)
│   ├── chapitre01_preface_roue_tourne.md
│   ├── chapitre02_guide_visuel_monde.md
│   ├── chapitre03_creation_personnage.md
│   ├── chapitre04_systeme_engrenages_adapte.md
│   ├── chapitre05_pouvoir_unique.md
│   ├── chapitre06_combat_conflits.md
│   ├── chapitre07_guide_maitre_jeu.md
│   ├── chapitre08_aventures_epiques.md
│   ├── chapitre09_bestiaire.md
│   ├── chapitre10_dimensions_paralleles.md
│   ├── chapitre11_glossaire_references.md
│   ├── chapitre12_personnages_prets.md
│   ├── chapitre13_tables_reference.md
│   └── first-draft.docx            # Version Word complète
│
└── .git/                           # Contrôle de version Git
```

---

## Chapitrage (v2.0)

### PREMIÈRE PARTIE : DANS LES FILS DU DESSIN
- Chapitre 1 : Préface - La Roue Tourne
- Chapitre 2 : Guide Visuel du Monde

### DEUXIÈME PARTIE : LES RÈGLES DU JEU
- Chapitre 3 : Création de Personnage
- Chapitre 4 : Le Système des Engrenages Adapté
- Chapitre 5 : Le Pouvoir Unique
- Chapitre 6 : Combat et Conflits

### TROISIÈME PARTIE : MAÎTRISER LA ROUE
- Chapitre 7 : Guide du Maître de Jeu
- Chapitre 8 : Créer des Aventures Épiques

### QUATRIÈME PARTIE : CRÉATURES ET MYSTÈRES
- Chapitre 9 : Bestiaire
- Chapitre 10 : Dimensions Parallèles

### CINQUIÈME PARTIE : ANNEXES
- Chapitre 11 : Glossaire et Références
- Chapitre 12 : Personnages Prêts à Jouer
- Chapitre 13 : Tables de Référence

---

## Compilation PDF

### Prérequis
- Distribution LaTeX complète (TeX Live, MiKTeX, etc.)
- Template `templates/roue-du-temps/roue-du-temps.sty`

### Compilation

```bash
cd "C:\Users\fxgui\Public\JdR\PDFLateX\wot\rouedutemps-engrenages"
pdflatex main.tex
pdflatex main.tex  # Deux passes pour table des matières et références
```

### Via script de compilation

```bash
# PowerShell
.\.claude\scripts\build-pdf.ps1 -ProjectPath "wot\rouedutemps-engrenages"

# Bash
./.claude/scripts/build-pdf.sh "wot/rouedutemps-engrenages"

# Slash command
/build-pdf project="wot/rouedutemps-engrenages" clean="true"
```

**Note :** Le fichier `main.tex` actuel contient des placeholders. Les chapitres en Markdown (`first-draft/*.md`) doivent être transcrits en LaTeX pour une compilation complète.

---

## État d'avancement

### Contenu
- [x] 13 chapitres rédigés en Markdown
- [x] Sommaire structuré v2.0
- [x] Règles de base (moteur-jeu.md)
- [x] Main.tex créé avec structure complète
- [ ] Transcription Markdown → LaTeX
- [ ] PDF final compilé

### Structure
- [x] Projet conforme à l'architecture multi-tenant
- [x] Template WoT v1.0 disponible
- [x] Git initialisé
- [x] README.md créé

---

## Projets Complémentaires

Ce guide fait partie d'une **trilogie de documents** pour jouer dans l'univers de La Roue du Temps :

1. **La Roue du Temps : Engrenages** *(ce projet)* - Guide de jeu complet avec règles et univers
2. **La Roue du Temps : Solo** - Système de jeu en solitaire avec oracles et scénario solo
3. **La Roue du Temps : Scénarios** - Générateur d'aventures et campagnes prêtes à jouer

**Architecture :**
```
rouedutemps-engrenages (SOCLE - prérequis)
       ↓
       ├─→ rouedutemps-solo (optionnel)
       └─→ rouedutemps-scenarios (optionnel)
```

---

## Template utilisé

**Template :** `templates/roue-du-temps/roue-du-temps.sty` (v1.0)

**Commandes spéciales WoT :**
- `\saidin`, `\saidar` : Termes en italique automatique
- `\angreal`, `\telaran` : Autres termes de la Vieille Langue
- `\citationwot{texte}{source}` : Citations WoT
- `\begin{pouvoirbox}{titre}...\end{pouvoirbox}` : Encadré pour tissages
- `\begin{nationbox}{nom}...\end{nationbox}` : Encadré pour nations/peuples
- `\begin{quotebox}...\end{quotebox}` : Citation d'ambiance

**Conventions respectées :**
- Terminologie française officielle
- Italiques pour termes de la Vieille Langue
- Majuscules conceptuelles (La Roue, Le Dessin, Le Pouvoir Unique)
- Orthographe stricte (Aes Sedai invariable, etc.)

---

## Licence / Crédits

### Univers
**La Roue du Temps** est l'œuvre de **Robert Jordan** (et Brandon Sanderson pour les derniers volumes).
- Éditeur original : Tor Books
- Éditeur français : Bragelonne
- **Tous droits réservés aux ayants droit**

### Système de jeu
**Engrenages** est un système de jeu de rôle créé par **Alexandre Clavel**.

### Ce document
- **Nature :** Adaptation non-officielle pour usage personnel uniquement
- **Statut :** Document ouvert aux contributions
- **Contact :** fx.rebellious.smile@gmail.com
- **Version :** 2.0 (2025-11-08)

---

## Contributions

Ce projet est ouvert à toutes les bonnes volontés souhaitant participer.

**Pour contribuer :**
1. Respecter les conventions établies dans `sommaire.md`
2. Suivre les règles de rédaction du CLAUDE.md
3. Contacter fx.rebellious.smile@gmail.com

---

## Historique des versions

**v2.0 (2025-11-08)**
- Restructuration majeure : séparation en 3 projets
- Suppression chapitres 11-16 (déplacés vers rouedutemps-solo et rouedutemps-scenarios)
- Renommage chapitres 17-19 → 11-13
- Création main.tex pour compilation LaTeX
- Sommaire mis à jour avec architecture modulaire

**v1.0 (2025-09-20)**
- Première version complète (19 chapitres)
- Tous les chapitres en Markdown
- Structure monolithique

---

## Support

Pour toute question ou suggestion :
- **Email :** fx.rebellious.smile@gmail.com
- **Documentation :** Voir `sommaire.md` pour structure détaillée
- **Templates :** Voir `templates/roue-du-temps/README.md`

---

**Note :** Ce document est un projet personnel non-officiel. Respectez les droits d'auteur de Robert Jordan et de ses ayants droit.
