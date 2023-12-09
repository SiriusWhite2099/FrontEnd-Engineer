#LESSON 

---
Maintenant qu'Alejandra a mis au point son site web, elle s'est rendu compte qu'elle souhaitait qu'il soit plus interactif. Elle aimerait mettre en place un panier d'achat qui permettrait aux utilisateurs d'acheter des forfaits de voyage directement à partir de son site web.

Pour ce faire, Alejandra devra apprendre le langage JavaScript. Tout site web qui fournit plus que des informations statiques utilise probablement JavaScript d'une manière ou d'une autre. Voici quelques exemples familiers de fonctions de sites web le plus souvent construites avec JavaScript :

- publicités pop-up
- graphiques animés (2D ou 3D)
- audio et vidéo interactifs
- les cartes et autres caractéristiques permettent d'accéder à la position géographique de l'utilisateur
- et bien plus encore !

L'une des caractéristiques de JavaScript est sa capacité à répondre aux événements du navigateur. Ces événements se produisent en temps réel et peuvent être déclenchés par une grande variété d'interactions de l'utilisateur, notamment :

- l'utilisateur qui clique sur un bouton
- l'utilisateur qui appuie sur la touche "Entrée" de son clavier
- un fichier vidéo en cours de chargement
- l'utilisateur redimensionne sa fenêtre
- l'utilisateur survole un texte sur la page web

---
Le cours explique qu'Alejandra souhaite rendre son site web plus interactif en ajoutant une fonctionnalité de panier d'achat pour permettre aux utilisateurs d'acheter des forfaits de voyage directement à partir du site. Pour ce faire, elle doit apprendre le langage JavaScript, qui est couramment utilisé pour rendre les sites web dynamiques.

JavaScript est un langage de programmation qui permet d'ajouter des fonctionnalités interactives à un site web. Il est souvent utilisé pour créer des éléments tels que des publicités pop-up, des graphiques animés, du contenu audio et vidéo interactif, des cartes interactives, et bien d'autres.

Une caractéristique importante de JavaScript est sa capacité à réagir aux événements du navigateur. Ces événements peuvent être déclenchés par diverses interactions de l'utilisateur, comme un clic sur un bouton, l'appui sur la touche "Entrée" du clavier, le chargement d'une vidéo, le redimensionnement de la fenêtre du navigateur, ou même le survol d'un texte sur la page web.

En résumé, JavaScript offre à Alejandra la possibilité d'ajouter des fonctionnalités interactives à son site web, ce qui est essentiel pour créer une expérience utilisateur plus engageante, notamment en permettant aux utilisateurs d'acheter des forfaits de voyage directement depuis le site.

---
# Exercice : 

Imaginez que vous êtes Alejandra, et vous voulez créer une fonctionnalité de panier d'achat sur votre site web. Utilisez JavaScript pour accomplir les tâches suivantes :

1. **Affichage du Panier :** Créez une fonction JavaScript qui affiche le contenu du panier d'achat lorsque l'utilisateur clique sur un bouton "Afficher le Panier".

2. **Ajout d'Articles :** Ajoutez la fonctionnalité permettant à l'utilisateur d'ajouter des forfaits de voyage à son panier d'achat. Vous pouvez simuler cela en créant un tableau d'objets représentant différents forfaits, et en permettant à l'utilisateur d'ajouter un forfait au panier en cliquant sur un bouton à côté de chaque forfait.

3. **Mise à Jour en Temps Réel :** Faites en sorte que le panier se mette à jour en temps réel chaque fois qu'un article est ajouté. Affichez la liste des articles dans le panier ainsi que le coût total.

4. **Gestion des Événements :** Utilisez les événements du navigateur pour déclencher des actions. Par exemple, si l'utilisateur appuie sur la touche "Entrée" tout en étant sur un forfait de voyage, ajoutez automatiquement ce forfait au panier.

5. **Interaction avec l'Utilisateur :** Ajoutez une interaction avec l'utilisateur. Par exemple, si l'utilisateur survole un forfait de voyage, affichez une information supplémentaire sur le forfait.

N'hésitez pas à utiliser des alertes ou des messages console pour simuler ces interactions dans un environnement d'exercice.

---
je vais diviser le code en plusieurs parties distinctes, chaque partie correspondant à un langage de programmation ou à une technologie spécifique. Je vais également fournir une explication pour chaque partie du code.

### HTML (Structure de la page web)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Site Web d'Alejandra</title>
</head>
<body>

<button onclick="afficherPanier()">Afficher le Panier</button>

<!-- Forfaits de voyage -->
<div class="forfait" id="forfait1">
  <h3>Forfait A</h3>
  <p>Prix: $1000</p>
  <button onclick="ajouterAuPanier('Forfait A', 1000)">Ajouter au Panier</button>
</div>

<div class="forfait" id="forfait2">
  <h3>Forfait B</h3>
  <p>Prix: $1500</p>
  <button onclick="ajouterAuPanier('Forfait B', 1500)">Ajouter au Panier</button>
</div>

<!-- Panier d'achat -->
<div id="panier">
  <h2>Panier d'Achat</h2>
  <ul id="listePanier"></ul>
  <p id="totalPanier">Total: $0</p>
</div>

<script>
  // JavaScript code will go here
</script>

</body>
</html>
```

Explication (HTML):
- La structure de base de la page web est définie en HTML.
- Des boutons et des sections sont créés pour les forfaits de voyage et le panier d'achat.
- Des événements `onclick` sont utilisés pour appeler des fonctions JavaScript lorsque les boutons sont cliqués.

### JavaScript (Gestion de l'interaction utilisateur)
```html
<script>
  let panier = [];
  let total = 0;

  function afficherPanier() {
    alert("Contenu du Panier:\n" + panier.map(item => item.nom).join('\n') + "\nTotal: $" + total);
  }

  function ajouterAuPanier(nom, prix) {
    panier.push({ nom, prix });
    total += prix;

    // Mise à jour de l'affichage en temps réel
    afficherContenuPanier();
  }

  function afficherContenuPanier() {
    const listePanier = document.getElementById('listePanier');
    const totalPanier = document.getElementById('totalPanier');

    // Efface le contenu actuel du panier
    listePanier.innerHTML = "";

    // Affiche chaque article dans le panier
    panier.forEach(item => {
      const listItem = document.createElement('li');
      listItem.textContent = `${item.nom} - $${item.prix}`;
      listePanier.appendChild(listItem);
    });

    // Affiche le coût total
    totalPanier.textContent = `Total: $${total}`;
  }
</script>
```

Explication (JavaScript):
- Des variables globales `panier` et `total` sont définies pour stocker les articles du panier et le coût total.
- Trois fonctions sont créées : `afficherPanier`, `ajouterAuPanier`, et `afficherContenuPanier`.
- La fonction `afficherPanier` affiche une alerte avec le contenu du panier.
- La fonction `ajouterAuPanier` ajoute un nouvel article au panier et met à jour l'affichage en temps réel.
- La fonction `afficherContenuPanier` met à jour l'affichage du panier sur la page.

Cela sépare le code HTML de la logique JavaScript, suivant ainsi une pratique de développement web modulaire.



