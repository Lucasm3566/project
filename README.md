# **_Risques liés à l'utilisation d'une IA pour coder en développement web_**

## **_1. Vulnérabilités de sécurité_**
L’IA peut générer du code sans validations serveur robustes.  
Elle peut écrire des requêtes <a href="https://www.google.com/search?q=SQL" target="_blank"><strong>SQL</strong></a> ou <a href="https://www.google.com/search?q=ORM" target="_blank"><strong>ORM</strong></a> facilitant les <a href="https://www.google.com/search?q=injections" target="_blank"><strong>injections</strong></a>.  
Les protections <a href="https://www.google.com/search?q=XSS" target="_blank"><strong>XSS</strong></a>, <a href="https://www.google.com/search?q=CSRF" target="_blank"><strong>CSRF</strong></a> ou la gestion des sessions peuvent être incorrectes.  
Cela expose l’application à une exploitation.

## **_2. Mauvaise compréhension de l’architecture_**
L’IA ne comprend pas toujours le projet.  
Elle peut créer des fichiers inadéquats ou violer des conventions internes.  
Le code généré crée alors des <a href="https://www.google.com/search?q=incoh%C3%A9rences" target="_blank"><strong>incohérences</strong></a>.  
La <a href="https://www.google.com/search?q=dette+technique" target="_blank"><strong>dette technique</strong></a> augmente rapidement.

## **_3. Gestion incorrecte de l’asynchrone_**
L’IA peut mélanger <a href="https://www.google.com/search?q=callbacks" target="_blank"><strong>callbacks</strong></a>, <a href="https://www.google.com/search?q=promesses" target="_blank"><strong>promesses</strong></a> et <a href="https://www.google.com/search?q=async/await" target="_blank"><strong>async/await</strong></a>.  
Cela provoque des <a href="https://www.google.com/search?q=race+conditions" target="_blank"><strong>race conditions</strong></a> ou laisse des ressources ouvertes.  
Ces problèmes apparaissent surtout en charge réelle.

## **_4. Optimisation insuffisante_**
Le code peut produire des rendus inutiles.  
L’IA peut ignorer des mécanismes comme le cache, le memo ou la pagination.  
Certaines opérations sont exécutées en série.  
Les <a href="https://www.google.com/search?q=performances" target="_blank"><strong>performances</strong></a> diminuent.

## **_5. Incompatibilités navigateur_**
L’IA peut utiliser des <a href="https://www.google.com/search?q=APIs+r%C3%A9centes" target="_blank"><strong>APIs récentes</strong></a> sans fallback.  
Elle peut oublier les <a href="https://www.google.com/search?q=polyfills" target="_blank"><strong>polyfills</strong></a> ou ignorer les contraintes du mobile.  
Le résultat peut fonctionner uniquement sur des systèmes modernes.  
Cela crée un écart entre développement et usage final.

## **_6. Mauvaise gestion des dépendances_**
L’IA peut ajouter des <a href="https://www.google.com/search?q=biblioth%C3%A8ques" target="_blank"><strong>bibliothèques</strong></a> obsolètes ou à risque.  
Elle peut multiplier les packages.  
Cela augmente les temps de build.  
Un audit manuel des <a href="https://www.google.com/search?q=d%C3%A9pendances" target="_blank"><strong>dépendances</strong></a> devient indispensable.

## **_7. Génération d’UI incohérente_**
Les composants peuvent ignorer le <a href="https://www.google.com/search?q=design+system" target="_blank"><strong>design system</strong></a>.  
Les attributs <a href="https://www.google.com/search?q=ARIA" target="_blank"><strong>ARIA</strong></a> peuvent manquer.  
Le CSS peut devenir trop spécifique.  
L’interface devient alors <a href="https://www.google.com/search?q=h%C3%A9t%C3%A9rog%C3%A8ne" target="_blank"><strong>hétérogène</strong></a>.

## **_8. Expositions involontaires côté front_**
L’IA peut inclure des <a href="https://www.google.com/search?q=cl%C3%A9s+API" target="_blank"><strong>clés API</strong></a> ou données <a href="https://www.google.com/search?q=sensibles" target="_blank"><strong>sensibles</strong></a>.  
Elles apparaissent dans le bundle final.  
Une mauvaise configuration <a href="https://www.google.com/search?q=CORS" target="_blank"><strong>CORS</strong></a> ou des <a href="https://www.google.com/search?q=tokens+persistants" target="_blank"><strong>tokens persistants</strong></a> amplifie la fuite.  
Cela mène à des fuites de données.

## **_9. Tests insuffisants ou erronés_**
Les tests couvrent seulement des cas heureux.  
Les <a href="https://www.google.com/search?q=mocks" target="_blank"><strong>mocks</strong></a> peuvent être incorrects.  
Sans tests de <a href="https://www.google.com/search?q=r%C3%A9gression" target="_blank"><strong>régression</strong></a>, la maintenance devient risquée.  
La <a href="https://www.google.com/search?q=qualit%C3%A9+r%C3%A9elle" target="_blank"><strong>qualité réelle</strong></a> reste inconnue.

## **_10. Documentation trompeuse_**
La doc peut sembler claire en apparence mais être incorrecte.  
Cela complique l’<a href="https://www.google.com/search?q=audit+code" target="_blank"><strong>audit</strong></a>.  
Elle peut être trop générique.  
Cela crée des <a href="https://www.google.com/search?q=malentendus" target="_blank"><strong>malentendus</strong></a>.
