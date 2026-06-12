# 📝 RÉTROSPECTIVE ÉCRITE : L'IMPORTANCE DU HTML SÉMANTIQUE & LA MAÎTRISE DU BOX MODEL

**Candidat :** Géovanie KOUCHIKO  
**Filière :** Développement Web & Mobile  
**Projet :** IMeN (Ecosystem Generator) & CV Sémantique et Stylisé

---

### Introduction
Cette semaine d'évaluation intensive a marqué un tournant important dans ma vision du développement web. En me forçant d'abord à livrer un projet au rendu visuel totalement **"brut"** et dépourvu de feuille de style CSS, cet exercice m'a permis de comprendre une règle fondamentale de notre industrie : *un code de qualité doit d'abord être d'une propreté chirurgicale et parfaitement compréhensible par une machine avant d'être stylisé pour l'œil humain.*

Dans un second temps, l'intégration de la feuille de style a éprouvé ma capacité à appliquer une charte graphique moderne en me reposant exclusivement sur la rigueur du modèle de boîte, sans aucun artifice ni contournement technique.

---

### 1. La sémantique : Donner du sens plutôt que du style
Durant ce projet, j'ai appris que le HTML5 sémantique ne consiste pas simplement à agencer des blocs, mais à attribuer un sens précis à chaque information. Utiliser des balises génériques (comme `<div>` ou `<span>`) revient à masquer la structure d'un bâtiment derrière une couche de peinture. 

Dans mon code, chaque zone a été pensée pour sa fonction :
* L'identité est isolée dans un `<header>`.
* Le cœur du parcours est encapsulé dans un `<main>`.
* Les blocs d'informations complémentaires occupent un `<aside>`.
* Les coordonnées professionnelles utilisent la balise experte `<address>`.

---

### 2. Les trois piliers industriels du HTML sémantique
À travers cette expérience de rendu brut, j'ai mesuré l'impact direct de la sémantique sur trois aspects couplés de la production web :

* **L'Accessibilité Universelle (A11y) :** En l'absence de CSS, un code sémantique permet aux lecteurs d'écran utilisés par les personnes malvoyantes de cartographier et lire mon CV de manière fluide.
* **La Performance SEO (Référencement) :** Les robots des moteurs de recherche ne jugent pas les couleurs, mais la structure. Une hiérarchie claire (`<h1>`, `<h2>`, `<section>`) leur permet de mieux indexer le site.
* **La Maintenance et la Robustesse :** En inspectant mon code, n'importe quel collaborateur peut comprendre l'architecture du projet en un coup d'œil. De plus, la validation à 100% au **validateur W3C** élimine les erreurs de syntaxe.

---

### 3. L'Évolution Graphique : Dompter le Box Model (Modèle de Boîte)
Le passage à la phase de stylisation a nécessité une transition technique majeure : habiller la structure sémantique existante sans jamais altérer le code HTML, tout en garantissant un comportement d'affichage 100% prévisible.

* **Le choix du Border-Box :** Par défaut, le navigateur ajoute les marges intérieures et les bordures à la largeur initiale d'un élément (`content-box`), ce qui génère régulièrement des bugs d'affichage ou des cassures de flux. Pour neutraliser ce comportement, j'ai appliqué la règle universelle `* { box-sizing: border-box; }`. Les dimensions de mes boîtes sont ainsi devenues mathématiquement fiables.
* **Contrôle des flux Block et Inline-Block :** J'ai exploité les propriétés natives des éléments pour aérer l'interface. Le conteneur principal `.cv-container` (élément de type `Block`) a été centré proprement grâce à une largeur maximale bloquée et des marges latérales automatiques (`margin: 0 auto;`). À l'inverse, les liens de contact, initialement de type *Inline*, ont été convertis en `inline-block`. Cette approche chirurgicale a permis de leur assigner un `padding` interne pour créer de véritables boutons d'interface UI modernes, tout en les maintenant alignés horizontalement.

---

### 4. Fluidité des Unités et Accessibilité Numérique
L'esthétique finale du projet repose sur des choix techniques orientés vers l'expérience utilisateur et l'adaptabilité :
* **Transition vers le REM :** Pour rompre avec la rigidité des pixels (`px`), l'intégralité des tailles de police et des espacements structurels (`margin`, `padding`) a été convertie en unités relatives `rem`. Le CV s'adapte ainsi dynamiquement et harmonieusement si un utilisateur modifie les préférences de zoom ou de texte de son navigateur.
* **Design inclusif et état `:focus` :** Soucieux de l'accessibilité continue, j'ai personnalisé l'état `:focus` des boutons de contact en y associant un halo lumineux subtil (`box-shadow`). Cette attention technique permet aux recruteurs et utilisateurs naviguant exclusivement au clavier (via la touche `TAB`) de repérer instantanément l'élément actif à l'écran.

---

### Conclusion
L'industrialisation de mon espace de travail sous **Linux Ubuntu via WSL** et l'application de la méthode **FORGE** m'ont donné les clés d'une gestion de projet rigoureuse. Associer cette rigueur système à une exigence chirurgicale sur le code HTML sémantique et à une maîtrise mathématique du Box Model CSS me donne des bases saines, solides et durables pour la suite de mon parcours de développeur.