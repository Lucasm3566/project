# **_Risques liés à l'utilisation d'une IA pour coder en développement web_**

## **_1. <a href="https://www.google.com/search?q=Vulnérabilités+de+s%C3%A9curit%C3%A9" target="_blank">Vulnérabilités de sécurité</a>_**
L’IA peut générer du code sans <a href="https://www.google.com/search?q=validations+serveur" target="_blank"><strong>validations serveur</strong></a> robustes.  
Elle peut écrire des requêtes <a href="https://www.google.com/search?q=SQL" target="_blank"><strong>SQL</strong></a> ou <a href="https://www.google.com/search?q=ORM" target="_blank"><strong>ORM</strong></a> facilitant les <a href="https://www.google.com/search?q=injections" target="_blank"><strong>injections</strong></a>.  
Les protections <a href="https://www.google.com/search?q=XSS" target="_blank"><strong>XSS</strong></a>, <a href="https://www.google.com/search?q=CSRF" target="_blank"><strong>CSRF</strong></a> ou la gestion des <a href="https://www.google.com/search?q=sessions" target="_blank"><strong>sessions</strong></a> peuvent être incorrectes.  
Cela expose l’application à une <a href="https://www.google.com/search?q=exploitation" target="_blank"><strong>exploitation</strong></a>.

## **_2. <a href="https://www.google.com/search?q=Mauvaise+compr%C3%A9hension+de+l%E2%80%99architecture" target="_blank">Mauvaise compréhension de l’architecture</a>_**
L’IA ne comprend pas toujours le <a href="https://www.google.com/search?q=projet" target="_blank"><strong>projet</strong></a>.  
Elle peut créer des <a href="https://www.google.com/search?q=fichiers+inad%C3%A9quats" target="_blank"><strong>fichiers inadéquats</strong></a> ou violer des <a href="https://www.google.com/search?q=conventions+internes" target="_blank"><strong>conventions internes</strong></a>.  
Le code généré crée alors des <a href="https://www.google.com/search?q=incoh%C3%A9rences" target="_blank"><strong>incohérences</strong></a>.  
La <a href="https://www.google.com/search?q=dette+technique" target="_blank"><strong>dette technique</strong></a> augmente rapidement.

## **_3. <a href="https://www.google.com/search?q=Gestion+incorrecte+de+l%E2%80%99asynchrone" target="_blank">Gestion incorrecte de l’asynchrone</a>_**
L’IA peut mélanger <a href="https://www.google.com/search?q=callbacks" target="_blank"><strong>callbacks</strong></a>, <a href="https://www.google.com/search?q=promesses" target="_blank"><strong>promesses</strong></a> et <a href="https://www.google.com/search?q=async/await" target="_blank"><strong>async/await</strong></a>.  
Cela provoque des <a href="https://www.google.com/search?q=race+conditions" target="_blank"><strong>race conditions</strong></a> ou laisse des ressources <a href="https://www.google.com/search?q=ouvertes" target="_blank"><strong>ouvertes</strong></a>.  
Ces problèmes apparaissent surtout en <a href="https://www.google.com/search?q=charge+r%C3%A9elle" target="_blank"><strong>charge réelle</strong></a>.

## **_4. <a href="https://www.google.com/search?q=Optimisation+insuffisante" target="_blank">Optimisation insuffisante</a>_**
Le code peut produire des <a href="https://www.google.com/search?q=rendus+inutiles" target="_blank"><strong>rendus inutiles</strong></a>.  
L’IA peut ignorer des mécanismes comme le <a href="https://www.google.com/search?q=cache" target="_blank"><strong>cache</strong></a>, le <a href="https://www.google.com/search?q=memo" target="_blank"><strong>memo</strong></a> ou la <a href="https://www.google.com/search?q=pagination" target="_blank"><strong>pagination</strong></a>.  
Certaines opérations sont exécutées <a href="https://www.google.com/search?q=en+s%C3%A9rie" target="_blank"><strong>en série</strong></a>.  
Les <a href="https://www.google.com/search?q=performances" target="_blank"><strong>performances</strong></a> diminuent.

## **_5. <a href="https://www.google.com/search?q=Incompatibilit%C3%A9s+navigateurs" target="_blank">Incompatibilités navigateur</a>_**
L’IA peut utiliser des <a href="https://www.google.com/search?q=APIs+r%C3%A9centes" target="_blank"><strong>APIs récentes</strong></a> sans fallback.  
Elle peut oublier les <a href="https://www.google.com/search?q=polyfills" target="_blank"><strong>polyfills</strong></a> ou ignorer les contraintes du <a href="https://www.google.com/search?q=mobile" target="_blank"><strong>mobile</strong></a>.  
Le résultat peut fonctionner uniquement sur des systèmes <a href="https://www.google.com/search?q=modernes" target="_blank"><strong>modernes</strong></a>.  
Cela crée un écart entre <a href="https://www.google.com/search?q=d%C3%A9veloppement" target="_blank"><strong>développement</strong></a> et <a href="https://www.google.com/search?q=usage+final" target="_blank"><strong>usage final</strong></a>.

## **_6. <a href="https://www.google.com/search?q=Mauvaise+gestion+des+d%C3%A9pendances" target="_blank">Mauvaise gestion des dépendances</a>_**
L’IA peut ajouter des <a href="https://www.google.com/search?q=biblioth%C3%A8ques" target="_blank"><strong>bibliothèques</strong></a> obsolètes ou à risque.  
Elle peut multiplier les <a href="https://www.google.com/search?q=packages+npm" target="_blank"><strong>packages</strong></a>.  
Cela augmente les <a href="https://www.google.com/search?q=temps+de+build" target="_blank"><strong>temps de build</strong></a>.  
Un audit manuel des <a href="https://www.google.com/search?q=d%C3%A9pendances" target="_blank"><strong>dépendances</strong></a> devient indispensable.

## **_7. <a href="https://www.google.com/search?q=G%C3%A9n%C3%A9ration+d%27UI+incoh%C3%A9rente" target="_blank">Génération d’UI incohérente</a>_**
Les composants peuvent ignorer le <a href="https://www.google.com/search?q=design+system" target="_blank"><strong>design system</strong></a>.  
Les attributs <a href="https://www.google.com/search?q=ARIA" target="_blank"><strong>ARIA</strong></a> peuvent manquer.  
Le CSS peut devenir <a href="https://www.google.com/search?q=trop+sp%C3%A9cifique" target="_blank"><strong>trop spécifique</strong></a>.  
L’interface devient alors <a href="https://www.google.com/search?q=h%C3%A9t%C3%A9rog%C3%A8ne" target="_blank"><strong>hétérogène</strong></a>.

## **_8. <a href="https://www.google.com/search?q=Expositions+c%C3%B4t%C3%A9+front" target="_blank">Expositions involontaires côté front</a>_**
L’IA peut inclure des <a href="https://www.google.com/search?q=cl%C3%A9s+API" target="_blank"><strong>clés API</strong></a> ou données <a href="https://www.google.com/search?q=sensibles" target="_blank"><strong>sensibles</strong></a>.  
Elles apparaissent dans le <a href="https://www.google.com/search?q=bundle+final" target="_blank"><strong>bundle final</strong></a>.  
Une mauvaise configuration <a href="https://www.google.com/search?q=CORS" target="_blank"><strong>CORS</strong></a> ou des <a href="https://www.google.com/search?q=tokens+persistants" target="_blank"><strong>tokens persistants</strong></a> amplifie la fuite.  
Cela mène à des <a href="https://www.google.com/search?q=fuites+de+donn%C3%A9es" target="_blank"><strong>fuites de données</strong></a>.

## **_9. <a href="https://www.google.com/search?q=Tests+insuffisants+ou+erron%C3%A9s" target="_blank">Tests insuffisants ou erronés</a>_**
Les tests couvrent seulement des <a href="https://www.google.com/search?q=cas+heureux" target="_blank"><strong>cas heureux</strong></a>.  
Les <a href="https://www.google.com/search?q=mocks" target="_blank"><strong>mocks</strong></a> peuvent être incorrects.  
Sans tests de <a href="https://www.google.com/search?q=r%C3%A9gression" target="_blank"><strong>régression</strong></a>, la maintenance devient risquée.  
La <a href="https://www.google.com/search?q=qualit%C3%A9+r%C3%A9elle" target="_blank"><strong>qualité réelle</strong></a> reste inconnue.

## **_10. <a href="https://www.google.com/search?q=Documentation+trompeuse" target="_blank">Documentation trompeuse</a>_**
La doc peut sembler <a href="https://www.google.com/search?q=claire+en+apparence" target="_blank"><strong>claire en apparence</strong></a> mais être incorrecte.  
Cela complique l’<a href="https://www.google.com/search?q=audit+code" target="_blank"><strong>audit</strong></a>.  
Elle peut être trop <a href="https://www.google.com/search?q=g%C3%A9n%C3%A9rique" target="_blank"><strong>générique</strong></a>.  
Cela crée des <a href="https://www.google.com/search?q=malentendus" target="_blank"><strong>malentendus</strong></a>.
