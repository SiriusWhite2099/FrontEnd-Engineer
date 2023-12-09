#LESSON 

---
Jusqu'à présent, nous avons vu comment une requête et une réponse uniques sont gérées entre un client et un serveur. Mais la plupart du temps, nos appareils ne font pas une seule demande. Chaque fois que nous chargeons une page web, notre appareil envoie une demande pour chaque fichier qui compose cette page. Ainsi, même lorsque nous ne chargeons qu'une seule page web, cette page peut faire plusieurs demandes afin de récupérer différents éléments de contenu, comme des images.

Comment ce processus fonctionne-t-il lorsque nous présentons plusieurs demandes simultanément ?

Toutes les étapes suivantes se déroulent en une fraction de seconde :

1. Lorsqu'un utilisateur tape une URL et appuie sur la touche Entrée, le serveur traite la demande et renvoie le fichier HTML au client. Les fichiers HTML contiennent le contenu d'un site web ainsi que des liens vers des ressources ou des codes supplémentaires nécessaires à l'affichage correct du site.
2. The browser will begin to search for elements in the HTML file and it will start to make additional HTTP requests for any other external resources used by the HTML file. This often includes: 
	- Une ou plusieurs feuilles de style CSS. CSS est l'abréviation de cascading style sheets (feuilles de style en cascade) ; CSS crée le style et la mise en page d'une page web. Le navigateur demande la feuille de style CSS et, lorsque le serveur la renvoie, le navigateur analyse la feuille de style CSS et commence à appliquer les styles visuels au contenu du site.
	- Le cycle demande-réponse envoie également les ressources du site web, telles que les images et les vidéos, du serveur au navigateur. Si ces fichiers sont volumineux, il peut même y avoir un délai notable avant qu'ils ne soient rendus par le navigateur.
	- Un ou plusieurs fichiers JavaScript. JavaScript rend la page web interactive. Ce langage de programmation est le "comportement" de la page web. Une page web qui n'utilise pas JavaScript est appelée page web statique.

Dans la plupart des navigateurs modernes, ces demandes supplémentaires sont effectuées en parallèle. Cela signifie que ces demandes sont lancées en même temps et que le navigateur n'attend pas de recevoir une ressource avant de demander la suivante.

Toutes les ressources sont généralement affichées dès que possible. Le code HTML sera affiché même si certaines des autres ressources n'ont pas été reçues par le navigateur.

Et voilà ! L'utilisateur peut maintenant interagir avec le site web qu'il a demandé à voir. L'ensemble du processus se déroule généralement en une seconde ou moins, en fonction de la vitesse de la connexion de l'utilisateur, de la taille du site web et même de la distance physique entre le navigateur et le serveur.

![obsidian](https://content.codecademy.com/programs/code-foundations-path/web-dev-survey/html_css_js.gif)

---
Ce cours explique le processus de traitement des requêtes multiples lors du chargement d'une page web, mettant en évidence le fonctionnement simultané des demandes HTTP. Voici un résumé détaillé :

1. **Initiation de la Requête :**
   - Lorsqu'un utilisateur entre une URL et appuie sur Entrée, le serveur traite la demande et renvoie le fichier HTML au client. Ce fichier HTML contient le contenu du site web ainsi que des liens vers d'autres ressources nécessaires.

2. **Recherche et Demande de Ressources Additionnelles :**
   - Le navigateur commence à analyser le fichier HTML et effectue des demandes HTTP supplémentaires pour toutes les ressources externes requises. Cela inclut généralement :
     - Feuilles de style CSS pour le style et la mise en page.
     - Ressources du site web telles que les images et les vidéos.
     - Fichiers JavaScript qui rendent la page interactive.

3. **Traitement en Parallèle :**
   - Les navigateurs modernes effectuent ces demandes supplémentaires en parallèle, ce qui signifie qu'elles sont lancées simultanément. Le navigateur ne nécessite pas d'attendre la réception d'une ressource avant de demander la suivante.

4. **Affichage Progressif :**
   - Les ressources sont généralement affichées dès qu'elles sont disponibles. Le code HTML peut être affiché même si certaines ressources, telles que des images volumineuses, n'ont pas encore été reçues par le navigateur.

5. **Interaction Utilisateur :**
   - Une fois toutes les ressources récupérées, l'utilisateur peut interagir avec le site web. Le processus global se déroule généralement en une seconde ou moins, en fonction de divers facteurs tels que la vitesse de la connexion, la taille du site web et la distance physique entre le navigateur et le serveur.

En résumé, ce cours explique comment les navigateurs gèrent simultanément plusieurs demandes HTTP lors du chargement d'une page web, assurant une expérience utilisateur rapide et interactive. Le processus en parallèle permet d'afficher rapidement le contenu, même si certaines ressources prennent plus de temps à être récupérées.

---
# Exercice :

Associez chaque étape du processus de chargement d'une page web à sa description correspondante :

A. Traitement de la demande initiale par le serveur et renvoi du fichier HTML. B. Recherche d'éléments dans le fichier HTML et initiation de demandes HTTP supplémentaires pour les ressources externes. C. Demande de feuilles de style CSS pour créer le style et la mise en page de la page web. D. Envoi des ressources du site web telles que les images et les vidéos du serveur au navigateur. E. Demande de fichiers JavaScript pour rendre la page web interactive. F. Exécution des demandes supplémentaires en parallèle dans la plupart des navigateurs modernes. G. Affichage progressif des ressources dès qu'elles sont disponibles.

Associez chaque lettre à la description correspondante.

1. L'utilisateur tape une URL et appuie sur Entrée.
2. Le navigateur analyse la feuille de style CSS et applique les styles visuels.
3. Le serveur répond aux demandes en parallèle.
4. Les fichiers JavaScript rendent la page interactive.
5. Les ressources du site web sont affichées progressivement.
6. Le navigateur initie des demandes HTTP supplémentaires pour les ressources externes.
7. Le code HTML est renvoyé au navigateur.

---
# Réponses :

1. A. Traitement de la demande initiale par le serveur et renvoi du fichier HTML.
2. C. Demande de feuilles de style CSS pour créer le style et la mise en page de la page web.
3. F. Exécution des demandes supplémentaires en parallèle dans la plupart des navigateurs modernes.
4. E. Demande de fichiers JavaScript pour rendre la page web interactive.
5. G. Affichage progressif des ressources dès qu'elles sont disponibles.
6. B. Recherche d'éléments dans le fichier HTML et initiation de demandes HTTP supplémentaires pour les ressources externes.
7. A. Le serveur répond aux demandes en parallèle.