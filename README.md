## Risques liés à l'utilisation d'une IA pour coder

### 1. Bugs subtils et erreurs difficiles à détecter
Même si le code généré semble propre et fonctionnel, il peut contenir :
- des erreurs logiques difficiles à repérer sans tests approfondis,
- des cas frontières non gérés (valeurs extrêmes, null, erreurs réseau, etc.),
- des comportements imprévus liés à une mauvaise compréhension du contexte technique.

Comme l'IA n'exécute pas réellement le programme, elle peut proposer un code correct en apparence mais incorrect en pratique. Le risque principal est de faire confiance à un code qui n'a pas été entièrement vérifié.



### 2. Introduction involontaire de vulnérabilités de sécurité
L'IA peut proposer du code :
- qui ne valide pas correctement les entrées utilisateurs,
- qui laisse passer des injections SQL, XSS ou des vulnérabilités de type RCE,
- qui utilise des bibliothèques obsolètes ou des pratiques à risque,
- qui oublie des mesures de sécurité (authentification, permissions, sanitation des données).

La sécurité demande une expertise spécifique que l'IA ne peut garantir. Utiliser son code tel quel sans audit peut exposer un système à des attaques.



### 3. Dépendance excessive à l’outil
Une utilisation trop systématique peut conduire à :
- une diminution de la compréhension fondamentale des concepts,
- une perte de compétence en résolution de problèmes,
- une baisse de la capacité à produire du code sans assistance,
- une difficulté accrue à maintenir ou à déboguer du code généré par l'IA.

Avec le temps, un développeur peut devenir moins autonome, ce qui est risqué dans des environnements professionnels exigeants.



### 4. Problèmes liés aux licences et à la propriété intellectuelle
Même si l’IA ne « copie » pas directement du code existant, il peut arriver qu’elle génère :
- du code très proche d’exemples existants sous licence restrictive (GPL, AGPL, etc.),
- des fragments issus de données d'entraînement qui ne sont pas compatibles avec l’usage prévu,
- des implémentations inspirées de projets protégés.

L’intégration de ce code dans un produit commercial peut poser des problèmes juridiques, surtout dans des contextes sensibles.



### 5. Code peu optimal ou mal structuré
Le code généré par l’IA peut être :
- fonctionnel mais non performant,
- dépourvu d’optimisations classiques (mémoire, complexité algorithmique, parallélisation),
- structuré de manière incohérente ou peu maintenable,
- redondant ou trop verbeux.

Sans connaissances solides, le développeur peut ne pas voir que la solution produite est sous-optimale.



### 6. Absence de compréhension du contexte métier
L’IA ne connaît pas :
- les contraintes spécifiques à un projet,
- les règles internes de l’entreprise,
- les impératifs organisationnels (logging, normes, politiques de sécurité),
- les dépendances techniques ou les choix d'architecture.

Elle génère du code générique qui peut être inadapté, voire incompatible avec l’environnement existant.



### 7. Incohérences dans l'architecture et le style du code
En utilisant de l’IA pour générer diverses parties d’un projet, on peut obtenir :
- des styles de code différents d’un fichier à l’autre,
- des patterns ou des architectures contradictoires,
- des conventions non respectées (nommages, organisation, tests),
- une perte progressive de cohérence dans le projet.

Cela augmente la dette technique et complique la maintenance.



### 8. Mauvaise gestion des dépendances et des versions
L’IA peut proposer :
- des bibliothèques incompatibles entre elles,
- des versions qui ne fonctionnent plus,
- des solutions basées sur des APIs dépréciées.

Sans vérification manuelle, cela peut mener à des conflits, des erreurs de compilation ou des comportements instables.



### 9. Risques liés à la confidentialité des données
Selon l’outil utilisé :
- des morceaux de code sensibles peuvent être envoyés à un service externe,
- des clés API, secrets ou données internes peuvent être accidentellement intégrées à une requête,
- l'outil peut conserver certaines informations selon sa politique.

Une mauvaise gestion de ces données peut exposer un projet à des risques de fuite.



## Comment limiter ces risques ?
- Considérer l’IA comme un assistant et non un auteur autonome.
- Toujours relire, tester et auditer le code généré.
- Fournir un contexte très clair (spécifications, contraintes, style).
- Utiliser des tests unitaires et d’intégration systématiques.
- Vérifier manuellement les aspects sécurité et licences.
- Maintenir une cohérence d’architecture via des documents de référence et des revues de code.

