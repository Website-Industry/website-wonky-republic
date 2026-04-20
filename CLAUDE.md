# CLAUDE.md — Wonky Republic

Contexte complet du projet de site pour Claude Code.

---

## Le projet

**Wonky Republic** est un label musical fictif / alter ego créatif de Marc Charton (alias Markichou), musicien et producteur basé à Toulouse.

Le site est le point d'entrée unique vers l'univers du label : musique, artistes, sets, galerie.

Structure actuelle : site statique HTML/CSS, une page par section, hébergement simple (Netlify ou équivalent).


---

## La mascotte et première artiste : Carlotta

**Carlotta** est le personnage central du label. C'est un flamant rose en peluche cousu sur une casquette à motifs tropicaux (hibiscus, feuilles, fond noir). Elle a des dreads grises, un ruban rouge au cou, et un pendentif flamant.

### Carte d'identité officielle

| Champ | Valeur |
|---|---|
| Nom | CARLOTTA |
| Pronoms | ielle |
| Surnom | Ambassadrice du Faux Pas |
| Espèce | Flamant rose mutant, genre textile |
| Taille | 15 cm (sans les dreads) |
| Couleur | Rose chaud / gris lilas (chevelure) |
| Accessoires | Dreads grises, ruban rouge au cou, casquette tropicale |
| Résidence | Sur la tête de Markichou |
| Profession | Agent de sécurité des basses |
| Nationalité | Wonky Republic |

**Signes particuliers :**
- Est toujours d'accord avec Markichou
- Refuse la tropical house et tout ce qui ressemble à un apéro LinkedIn
- Mord si on lui touche les dreads

---

## Le label : Wonky Republic

**Tagline :** Électronique tordue pour corps désaxés et oreilles curieuses.

**Genre :** Wonky Psybass, Glitch Bass, électronique expérimentale

**Roster actuel :** Carlotta (seule artiste pour l'instant). D'autres artistes à venir (MERJ, projet solo de Marc).

---

## Identité visuelle

### Palette de couleurs

```css
--rose:   #ff3e8a   /* couleur principale, accents, néon */
--violet: #cc66ff   /* secondaire, pronoms, aka */
--dark:   #05000d   /* fond principal */
--card:   #0a0012   /* fond des cartes */
```

### Typographies (Google Fonts)

| Usage | Font |
|---|---|
| Logo / titres décoratifs | Righteous |
| Grands titres (noms d'artistes) | Bebas Neue |
| Italique / sous-titres élégants | Playfair Display Italic |
| Corps de texte / champs / mono | IBM Plex Mono |

### Motifs et ambiance

- Fond sombre quasi noir avec radial gradients rose/violet subtils
- Motif floral SVG répété en fond (pétales géométriques, opacité très faible)
- Bordures et séparateurs : `rgba(255,62,138,0.15)` à `0.3`
- Glow sur les éléments importants : `text-shadow` et `box-shadow` rose
- Barcode décoratif en footer
- Séparateur de section : ligne dégradée + titre centré entre deux lignes
- Style "document officiel décalé" pour les cartes (carte d'identité)

### Éléments récurrents

```html
<!-- Séparateur de section -->
<div class="section-header">
  <div class="section-line"></div>
  <div class="section-title">* Titre *</div>
  <div class="section-line r"></div>
</div>

<!-- Nav fixe -->
<nav> ... logo Righteous gradient + liens IBM Plex Mono uppercase ... </nav>

<!-- Footer -->
<footer> logo + barcode décoratif + référence WR-001 </footer>
```

---

## Contenu actuel du site

### Section Hero (index.html)
- Photo de Carlotta (HD, base64 embarquée)
- Nom + pronom ielle en rose
- Aka : Ambassadrice du Faux Pas
- Description + tags (Wonky Psybass, Glitch, Sécu des basses)
- Bouton vers la playlist Spotify

### Section Playlist
- Embed Spotify thème sombre
- Playlist : Wonky Glitch Bass
- URL : `https://open.spotify.com/playlist/4uRnAh1AWA70JberpllU2a`

### Section Sets
- Set La Fesste — 9 mai 2025
- Lien Mixcloud à venir après le set
- Badge "Enregistrement à venir"

### Section Galerie
- Masonry 3 colonnes
- 2 photos de Carlotta actuellement
- Placeholders "+ photo" pour les futures photos

### Page Artistes (artistes.html)
- Grille 3 colonnes
- Carlotta en carte active
- 2 cartes fantômes "Bientôt sur le label"
- Barre de filtres par genre (décorative pour l'instant)

---

## Ce qui est prévu / à venir

- Lien Mixcloud pour le set La Fesste (9 mai)
- Ajouter des photos dans la galerie (section masonry)
- Page ou section pour les autres artistes du label : MERJ (duo Marc + Jess, chant improvisé + électronique), projet solo de Marc (nom en cours : COTT ou FOND)
- QR code au verso de la carte de visite Carlotta (lien vers ce site)
- hébergé sur Vercel

---

## Conventions de code

- HTML statique
- Utiliser les variables CSS (`var(--rose)`, etc.) pour toute couleur
- Garder la cohérence typographique (voir tableau polices ci-dessus)
- Toujours tester que le rendu est propre sur mobile en priorité

---

## Markichou

Marc Charton, musicien autodidacte depuis 20 ans, producteur Ableton Live depuis 12 ans, batteur de longue date, basé à Toulouse. Enseigne la MAO (Sawup, Ghost-Note). Projet solo en cours de naming (COTT ou FOND). Duo MERJ avec Jess (chant improvisé). Références sonores : Photay, Siriusmo, Aphex Twin.
