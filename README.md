# **_Risques liés à l'utilisation d'une IA pour coder en développement web_**

## **_1. Vulnérabilités de sécurité_**
L’IA peut générer du code sans **validations serveur** robustes, laissant passer des entrées malveillantes.  
Elle peut aussi produire des requêtes **SQL** ou **ORM** mal paramétrées, facilitant les **injections**.  
Les protections **XSS**, **CSRF** ou la gestion des **sessions** peuvent être absentes ou incorrectes.  
Cela entraîne un risque direct d’**exploitation** de l’application en production.

## **_2. Mauvaise compréhension de l’architecture_**
L’IA n’a pas toujours la vision complète du **projet**, surtout dans les environnements modulaires.  
Elle peut placer le code dans des **fichiers inadéquats** ou violer des **conventions internes**.  
Le résultat peut fonctionner en local mais créer des **incohérences** dans l’écosystème existant.  
À terme, cela augmente la **dette technique** et complique la maintenance.

## **_3. Gestion incorrecte de l’asynchrone_**
En JavaScript, l’IA peut mélanger **callbacks**, **promesses** et **async/await** de manière incohérente.  
Cela crée des **race conditions**, des erreurs non catchées ou des comportements imprévisibles.  
Des ressources peuvent rester **ouvertes** (sockets, connexions DB) faute de gestion appropriée.  
Ces problèmes apparaissent souvent seulement en **charge réelle**, rendant le débogage complexe.

## **_4. Optimisation insuffisante_**
Le code généré peut provoquer des **rendus inutiles**, notamment dans React.  
L’IA peut ignorer les mécanismes de **cache**, de **memo** ou de **pagination** efficaces.  
Côté serveur, les appels externes peuvent être effectués **en série** plutôt qu’en parallèle.  
Cela dégrade les **performances** et augmente les **coûts d’infrastructure**.

## **_5. Incompatibilités navigateur_**
L’IA peut utiliser des **APIs récentes** non supportées par certains navigateurs sans fallback.  
Elle peut omettre des **polyfills** ou ignorer les contraintes liées au **mobile**.  
L’application peut fonctionner seulement dans un environnement **moderne**, pas en production réelle.  
Le résultat est un écart important entre **développement** et **usage final**.

## **_6. Mauvaise gestion des dépendances_**
L’IA propose parfois des **bibliothèques** obsolètes, lourdes ou vulnérables.  
Elle peut multiplier inutilement les **packages**, augmentant le risque de faille.  
Cela alourdit les **temps de build** et complique la **maintenance**.  
Un audit manuel des **dépendances** reste indispensable.

## **_7. Génération d’UI incohérente_**
Les composants peuvent ignorer le **design system** ou les standards internes.  
L’accessibilité peut être mal gérée : absence d’attributs **ARIA**, focus incorrect, contrastes insuffisants.  
Le CSS peut devenir **trop spécifique**, difficile à maintenir ou à réutiliser.  
Cela produit une interface **hétérogène** et compliquée à harmoniser.

## **_8. Expositions involontaires côté front_**
L’IA peut proposer d’inclure des **clés API** ou des informations **sensibles** dans le code client.  
Ces données sont alors visibles dans le **bundle final** accessible à tous les utilisateurs.  
Une mauvaise configuration **CORS** ou des **tokens persistants** peuvent amplifier le risque.  
Cela expose l’application à des **fuites de données** ou à l’usage abusif de services backend.

## **_9. Tests insuffisants ou erronés_**
Les tests générés peuvent ne couvrir que des **cas heureux** ou superficiels.  
Ils peuvent utiliser des **mocks** incorrects, donnant l’illusion d’un code fiable.  
L’absence de tests de **régression** rend l’évolution dangereuse.  
Sans vérification humaine, la **qualité réelle** reste incertaine.

## **_10. Documentation trompeuse_**
L’IA peut rédiger une documentation **claire en apparence**, mais incorrecte dans le fond.  
Cette discordance rend l’**audit** du code plus difficile pour les développeurs.  
Elle peut aussi être trop **générique**, ignorant les spécificités du projet.  
Cela provoque des **malentendus** lors de la prise en main ou des revues.
