#LESSON 

---
Nous allons approfondir le modèle client-serveur en explorant une partie du protocole HTTP que vous avez probablement déjà vue : les codes d'état HTTP.

Lorsqu'un serveur répond à un client, il indique un code d'état dans sa réponse. Les codes d'état indiquent si la requête HTTP a été traitée avec succès ou non et, en cas d'erreur, ils contiennent des informations sur le type d'erreur qui s'est produite. Le code d'état permet au navigateur de savoir comment traiter les données renvoyées avec la réponse.

Examinez les statuts HTTP ci-dessous et voyez si l'un d'entre eux vous semble familier.

![obsidian](https://content.codecademy.com/programs/code-foundations-path/web-dev-survey/table.svg)


---
Ce cours aborde le modèle client-serveur en se concentrant sur une composante du protocole HTTP (Hypertext Transfer Protocol) : les codes d'état HTTP. Ces codes d'état sont utilisés lorsqu'un serveur répond à une requête émise par un client. Voici une explication plus détaillée :

1. **Modèle Client-Serveur :**
   - Le modèle client-serveur implique une interaction entre un client (demandeur de données) et un serveur (fournisseur de données). Dans le contexte d'HTTP, le serveur répond à une requête du client avec un code d'état.

2. **Protocole HTTP :**
   - HTTP est un protocole de communication utilisé sur l'internet pour le transfert de données. Il est essentiel dans le fonctionnement du World Wide Web.

3. **Codes d'État HTTP :**
   - Lorsqu'une requête HTTP est traitée par un serveur, celui-ci renvoie un code d'état dans sa réponse. Ces codes indiquent si la requête a été exécutée avec succès ou s'il y a eu une erreur, et ils fournissent des détails sur la nature de l'erreur.

4. **Traitement des Réponses par le Navigateur :**
   - Les codes d'état sont cruciaux pour le traitement des données par le navigateur. Ils informent le navigateur sur la manière dont il doit traiter les informations renvoyées avec la réponse du serveur.

5. **Exemples de Codes d'État HTTP :**
   - Le cours semble se concentrer sur la présentation d'exemples de codes d'état HTTP. Ces codes sont généralement des nombres à trois chiffres qui décrivent l'état de la requête. Par exemple, le code "200 OK" signifie que la requête a été traitée avec succès, tandis que le code "404 Not Found" indique que la ressource demandée n'a pas été trouvée.

En résumé, ce cours explore la composante des codes d'état HTTP dans le modèle client-serveur. Ces codes sont cruciaux pour la communication entre le client (par exemple, un navigateur) et le serveur, informant sur le succès ou l'échec de la requête et guidant le traitement des données par le navigateur.

---
# Instructions

1. Le navigateur affiche actuellement un site web qu'Alex a créé pour présenter des photos et des descriptions de ses animaux de compagnie. Si vous cliquez sur les liens Chiens ou Chats, vous pourrez obtenir plus d'informations sur les chiens et les chats d'Alex.
2. Ensuite, cliquez sur l'icône de fichier dans le coin supérieur gauche de l'éditeur de texte. Vous verrez les différents fichiers HTML que le serveur est prêt à envoyer au navigateur lorsque ces liens sont cliqués. Ces fichiers HTML correspondent aux différentes pages web affichées dans le navigateur. Lorsque le lien Chiens est cliqué, le serveur envoie le fichier dogs.html au client.
3. Essayez les liens Chiens et Chats maintenant !
4. Créons une réponse d'état 404 en faisant une demande pour une ressource inexistante. Alex n'a pas construit de page web pour répertorier ses tortues ! Cliquez sur le lien Tortues pour voir le navigateur afficher le code d'état 404.

---
*cats.html*
```html
<body>

  <h1>Meet My Cats</h1>

  <p><a href='index.html'>Back to Home</a></p>

  <h3>Mr. Whiskers</h3>

  <img src='https://content.codecademy.com/programs/code-foundations-path/web-dev-survey/ludemeula-fernandes-451948-unsplash.jpg' width='200px'/>

  <p>For Mr. Whiskers, life is all about cat naps and cat nip.</p>

  <h3>Zippy</h3>

  <img src='https://content.codecademy.com/programs/code-foundations-path/web-dev-survey/erik-jan-leusink-104677-unsplash.jpg' width='200px'/>

  <p>Zippy is a cool cat! Only problem is: she thinks she's a dog.</p>

</body>
```
*dogs.html*
```html
<body>

  <h1>Meet My Dogs</h1>

  <p><a href='index.html'>Back to Home</a></p>

  <h3>Frank</h3>

  <img src="https://content.codecademy.com/programs/code-foundations-path/web-dev-survey/sarandy-westfall-603305-unsplash.jpg" width="150px"/>

  <p>This is my pug Frank. He like naps and short walks to the kitchen.</p>

  <h3>Pete</h3>

  <img src="https://content.codecademy.com/programs/code-foundations-path/web-dev-survey/conner-baker-369081-unsplash.jpg" width="250px"/>

  <p>Pete is a well mannered chap. He's friendly with just about everyone, except squirrels. Pete does not like squirrels.</p>

</body>
```
*index.html*
```html
<body>

  <img src='https://content.codecademy.com/programs/code-foundations-path/web-dev-survey/pets.jpg' width='400px'/>

  <p>Hi, I'm Alex. Welcome to my website dedicated to my pets! They are the cutest buckets of joy you'll ever lay your eyes on! Check them out here:</p>

  <ul>

    <li><a href="dogs.html">Dogs</a></li>

    <li><a href="cats.html">Cats</a></li>

    <li><a href="turtles.html">Turtles</a></li>

  </ul>

</body>
```

---

# Exercice :

Associez chaque description de code d'état HTTP à son code correspondant en utilisant les informations fournies dans le cours.

A. "200 OK" B. "404 Not Found" C. "500 Internal Server Error" D. "301 Moved Permanently" E. "403 Forbidden"

1. Ce code d'état indique que la requête a été traitée avec succès, et les données demandées sont incluses dans la réponse.
    
2. Ce code d'état signifie que la ressource demandée n'a pas été trouvée sur le serveur.
    
3. Ce code d'état indique une erreur interne du serveur, généralement en raison d'un problème de configuration ou de programmation.
    
4. Ce code d'état est utilisé pour rediriger le client vers une nouvelle URL permanente.
    
5. Ce code d'état signifie que le serveur refuse de répondre à la requête, souvent en raison d'une absence d'autorisation.
    

Associez chaque description à la lettre correspondante.

---
  
# Correction de l'exercice :

1. A. "200 OK" - Ce code d'état indique que la requête a été traitée avec succès, et les données demandées sont incluses dans la réponse.
    
2. B. "404 Not Found" - Ce code d'état signifie que la ressource demandée n'a pas été trouvée sur le serveur.
    
3. C. "500 Internal Server Error" - Ce code d'état indique une erreur interne du serveur, généralement en raison d'un problème de configuration ou de programmation.
    
4. D. "301 Moved Permanently" - Ce code d'état est utilisé pour rediriger le client vers une nouvelle URL permanente.
    
5. E. "403 Forbidden" - Ce code d'état signifie que le serveur refuse de répondre à la requête, souvent en raison d'une absence d'autorisation.
    

Cela conclut la correction de l'exercice. N'hésitez pas à poser d'autres questions si vous en avez!