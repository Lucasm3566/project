# **_Risques liés à l'utilisation d'une IA pour coder en développement web_**

## **_1. Vulnérabilités de sécurité_**
L’IA peut générer du code sans <strong title="Vérifications côté serveur pour empêcher les données dangereuses.">validations serveur</strong> robustes.  
Elle peut écrire des requêtes <strong title="Langage utilisé pour interagir avec une base de données.">SQL</strong> ou <strong title="Système reliant objets du code et tables de la base.">ORM</strong> facilitant les <strong title="Technique permettant d'injecter du code malveillant.">injections</strong>.  
Les protections <strong title="Injection de JavaScript malveillant.">XSS</strong>, <strong title="Action non désirée exécutée par un utilisateur authentifié.">CSRF</strong> ou la gestion des <strong title="Mécanisme d’identification persistante.">sessions</strong> peuvent être incorrectes.  
Cela expose l’application à une <strong title="Utilisation abusive d'une faille.">exploitation</strong>.

## **_2. Mauvaise compréhension de l’architecture_**
L’IA ne comprend pas toujours le <strong title="Structure globale et organisation du code.">projet</strong>.  
Elle peut créer des <strong title="Fichiers qui ne respectent pas la structure prévue.">fichiers inadéquats</strong> ou violer des <strong title="Règles internes définissant comment écrire le code.">conventions internes</strong>.  
Le code généré crée alors des <strong title="Éléments mal intégrés au reste du système.">incohérences</strong>.  
La <strong title="Accumulation de choix techniques compliquant la maintenance.">dette technique</strong> augmente rapidement.

## **_3. Gestion incorrecte de l’asynchrone_**
L’IA peut mélanger <strong title="Fonction exécutée après une autre.">callbacks</strong>, <strong title="Objet représentant une opération asynchrone.">promesses</strong> et <strong title="Syntaxe moderne pour gérer l'asynchrone.">async/await</strong>.  
Cela provoque des <strong title="Erreurs liées à l'exécution simultanée inattendue.">race conditions</strong> ou laisse des ressources <strong title="Connexions ou fichiers non fermés.">ouvertes</strong>.  
Ces problèmes apparaissent surtout en <strong title="Conditions réelles avec beaucoup de trafic.">charge réelle</strong>.

## **_4. Optimisation insuffisante_**
Le code peut produire des <strong title="Affichages inutiles de composants.">rendus inutiles</strong>.  
L’IA peut ignorer des mécanismes comme le <strong title="Méthode pour éviter des recalculs.">cache</strong>, le <strong title="Fonction qui mémorise un résultat.">memo</strong> ou la <strong title="Méthode pour limiter la quantité de données chargées.">pagination</strong>.  
Certaines opérations sont exécutées <strong title="Les tâches attendent inutilement les unes les autres.">en série</strong>.  
Les <strong title="Vitesse ressentie par l’utilisateur.">performances</strong> diminuent.

## **_5. Incompatibilités navigateur_**
L’IA peut utiliser des <strong title="Fonctionnalités Web récentes non supportées partout.">APIs récentes</strong> sans fallback.  
Elle peut oublier les <strong title="Code permettant la compatibilité avec les navigateurs anciens.">polyfills</strong> ou ignorer les contraintes du <strong title="Appareils mobiles et écrans réduits.">mobile</strong>.  
Le résultat peut fonctionner uniquement sur des systèmes <strong title="Navigateurs modernes ou de développeurs.">modernes</strong>.  
Cela crée un écart entre <strong title="Environnement du développeur.">développement</strong> et <strong title="Utilisation réelle.">usage final</strong>.

## **_6. Mauvaise gestion des dépendances_**
L’IA peut ajouter des <strong title="Bibliothèques externes.">bibliothèques</strong> obsolètes ou à risque.  
Elle peut multiplier les <strong title="Modules importés via npm, yarn, pnpm.">packages</strong>.  
Cela augmente les <strong title="Temps nécessaires pour compiler le projet.">temps de build</strong>.  
Un audit manuel des <strong title="Modules externes utilisés.">dépendances</strong> devient indispensable.

## **_7. Génération d’UI incohérente_**
Les composants peuvent ignorer le <strong title="Système définissant les styles et règles visuelles.">design system</strong>.  
Les attributs <strong title="Indications pour technologies d'assistance.">ARIA</strong> peuvent manquer.  
Le CSS peut devenir <strong title="Sélecteurs trop précis qui empêchent la réutilisation.">trop spécifique</strong>.  
L’interface devient alors <strong title="Styles visuels non uniformes.">hétérogène</strong>.

## **_8. Expositions involontaires côté front_**
L’IA peut inclure des <strong title="Clés permettant d'accéder à des services.">clés API</strong> ou données <strong title="Informations confidentielles.">sensibles</strong>.  
Elles apparaissent dans le <strong title="Code final envoyé au navigateur.">bundle final</strong>.  
Une mauvaise configuration <strong title="Gestion des autorisations de requêtes entre domaines.">CORS</strong> ou des <strong title="Jetons d'identification.">tokens persistants</strong> amplifie la fuite.  
Cela mène à des <strong title="Accès non autorisé aux données.">fuites de données</strong>.

## **_9. Tests insuffisants ou erronés_**
Les tests couvrent seulement des <strong title="Cas où tout fonctionne sans erreur.">cas heureux</strong>.  
Les <strong title="Objets ou fonctions simulées.">mocks</strong> peuvent être incorrects.  
Sans tests de <strong title="Tests garantissant qu'une modification ne casse rien.">régression</strong>, la maintenance devient risquée.  
La <strong title="Robustesse réelle du code.">qualité réelle</strong> reste inconnue.

## **_10. Documentation trompeuse_**
La doc peut sembler <strong title="Correcte visuellement mais fausse dans le contenu.">claire en apparence</strong> mais être incorrecte.  
Cela complique l’<strong title="Analyse et vérification du code.">audit</strong>.  
Elle peut être trop <strong title="Pas adaptée aux spécificités du projet.">générique</strong>.  
Cela crée des <strong title="Mauvaises interprétations.">malentendus</strong>.
