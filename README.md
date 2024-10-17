# Slide Natureza - Portugal en Images

## Description

**Slide Natureza** est un projet de diaporama interactif développé avec **HTML** et **CSS**, présentant plusieurs destinations emblématiques du Portugal. Chaque "slide" est une carte représentant un lieu précis, avec une image et une description. Ce projet permet aux utilisateurs de naviguer entre les slides via un simple clic, avec des transitions fluides entre les différentes cartes.

## Fonctionnalité principale

Le projet fonctionne en utilisant des boutons radio invisibles. Lorsqu'un bouton radio est sélectionné, la carte correspondante devient plus large, révélant l'image et la description associée. Chaque carte se compose de :
- Une icône numérotée.
- Une description textuelle du lieu.
- Une image d'arrière-plan qui change selon la carte sélectionnée.

Les transitions sont gérées via du **CSS pur**, et les cartes changent de largeur lorsque l'une d'entre elles est activée.

## Détails du fonctionnement du code

### HTML

Le fichier `index.html` contient la structure de la page. Voici les principaux éléments :

- **Input type radio** : Ces inputs cachés sont utilisés pour permettre à l'utilisateur de naviguer entre les différentes cartes.
- **Labels associés aux inputs** : Chaque `label` représente une carte, et lorsqu'il est cliqué, il active son input associé (via l'attribut `for`).
- **Structure des cartes** : Chaque carte contient une icône avec un numéro et une section de description comprenant un titre et un texte.

#### Extrait HTML principal :
```html
<div class="container">
    <input type="radio" name="slide" id="c1" checked>
    <label for="c1" class="card">
        <div class="row">
            <div class="icon">1</div>
            <div class="description">
                <h4>A capital do sul</h4>
                <p>Faro - Discover the Wonders of Nature</p>
            </div>
        </div>
    </label>
    <!-- ... autres cartes ici ... -->
</div>
```

### CSS

Le fichier `styles.css` est responsable de l'apparence visuelle du slider. Les éléments essentiels comprennent :

- **Centrage et mise en page** : Utilisation de **Flexbox** pour aligner les cartes au centre de la page.
- **Effets de transition** : Chaque carte a un effet de transition lorsque l'utilisateur sélectionne une nouvelle carte.
- **Animation des descriptions** : Les descriptions textuelles apparaissent avec un léger décalage et une transition en douceur lorsque la carte est activée.

```CSS
input:checked+label {
  width: 600px;
}

input:checked+label .description {
  opacity: 1;
  transform: translateY(0);
}

.card {
  transition: .6s cubic-bezier(.28, -0.03, 0, 0.99);
}
```

### Explication des principaux concepts utilisés

- **Boutons radio invisibles** : Les boutons radio permettent de garder la sélection active, ce qui est pratique pour contrôler l'affichage des cartes. Ils sont rendus invisibles via `display: none` mais restent fonctionnels.

- **Flexbox pour la disposition** : Flexbox est utilisé pour garantir que les cartes soient alignées horizontalement et centrées à l'écran. Cela simplifie également la mise en page réactive.

- **Transitions CSS** : Les transitions sont appliquées aux cartes pour les rendre interactives et permettre des animations fluides lorsque l'utilisateur sélectionne une carte.


### Fichiers du projet

- `index.html` : Le fichier HTML principal contenant la structure du slider.
- `styles.css` : Le fichier de style définissant l'apparence et les animations du slider.
- `img/` : Ce dossier contient les images utilisées comme arrière-plan pour chaque carte.

### Guide d'utilisation

- **Sélection des cartes** : Cliquez sur une carte pour l'agrandir et afficher les détails du lieu associé.
- **Transitions fluides** : Les cartes se redimensionnent automatiquement lors de la sélection d'une nouvelle carte, et le texte apparaît en douceur.

### Fonctionnalités supplémentaires possibles

Si vous souhaitez améliorer ou ajouter de nouvelles fonctionnalités à ce projet, voici quelques suggestions :

- **JavaScript pour des interactions plus complexes** : Vous pouvez ajouter du JavaScript pour des fonctionnalités comme un contrôle automatique des slides (carrousel automatique) ou des boutons "Précédent" et "Suivant".
- **Amélioration de la réactivité** : Ajouter des media queries pour améliorer l'expérience sur mobile et tablette.
- **Optimisation des images** : Utiliser des versions optimisées des images pour une performance améliorée.

### Contribution

Les contributions sont les bienvenues ! Si vous souhaitez améliorer ce projet ou ajouter de nouvelles fonctionnalités, vous pouvez :

1. Faire un fork de ce dépôt.
2. Créer une nouvelle branche (`git checkout -b feature/nouvelle-fonctionnalite`).
3. Soumettre vos modifications (`git commit -m 'Ajouter nouvelle fonctionnalité'`).
4. Pousser la branche (`git push origin feature/nouvelle-fonctionnalite`).
5. Ouvrir une Pull Request.

### Licence

Ce projet est sous licence MIT. Consultez le [fichier LICENSE](LICENSE) pour plus d'informations.

### Auteur

**Pedro Costa**  
[LinkedIn](https://linkedin.com/in/pedronfcosta/)

### Explication détaillée des sections :
1. **Description et Fonctionnalité principale** : Donne une vue d'ensemble du projet et de son objectif.
2. **Détails du code** : Explique comment le HTML et le CSS fonctionnent ensemble pour créer le diaporama.
3. **Concepts utilisés** : Décompose les techniques spécifiques utilisées (boutons radio invisibles, transitions CSS, etc.).
4. **Fichiers du projet** : Une liste des fichiers inclus dans le projet et leur fonction.
5. **Guide d'utilisation** : Explique comment l'utilisateur peut interagir avec le slider.
6. **Suggestions de fonctionnalités futures** : Propose des idées pour améliorer le projet, telles que l'ajout de JavaScript.
7. **Contribution et Licence** : Indique comment les autres peuvent contribuer et sous quelle licence le projet est partagé.

Cela devrait fournir une vue d'ensemble claire et exhaustive du projet et de son fonctionnement.

