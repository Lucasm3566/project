# Risques liés à l'utilisation d'une IA pour coder (version très détaillée et exhaustive)

Ce document rassemble l’ensemble des risques connus, directs et indirects, liés à l’usage d’une intelligence artificielle générative pour la production de code.  
Il couvre les aspects techniques, humains, organisationnels, juridiques et sécuritaires.

---

## 1. Risques techniques

### 1.1 Bugs subtils et erreurs logiques
L’IA peut générer du code :
- qui semble correct mais ne respecte pas parfaitement les spécifications,
- qui omet des cas limites (données nulles, dépassements, données corrompues),
- qui contient des erreurs difficiles à repérer dans les premières lignes de tests,
- qui réutilise des approches obsolètes ou incorrectes,
- qui produit des comportements imprévisibles en production.

**Pourquoi ?**  
L’IA n’exécute pas le code, elle anticipe statistiquement ce qui “semble correct”.

---

### 1.2 Code non fonctionnel ou incomplet
Le code produit peut :
- ne pas compiler,
- dépendre de bibliothèques non compatibles,
- être insuffisamment testé,
- reposer sur des suppositions incorrectes liées au contexte du projet.

L’IA n’a pas accès à la même vision que l’environnement réel (fichiers, architecture, erreurs compilateur).

---

### 1.3 Utilisation de mauvaises pratiques
L’IA peut produire :
- des structures inefficaces,
- des duplications de code,
- des patterns anti architecture (god objects, couplage excessif),
- des solutions non idiomatiques selon le langage.

---

### 1.4 Code non optimisé
L'IA peut générer du code qui :
- utilise plus de mémoire que nécessaire,
- effectue des opérations inutiles,
- choisit une complexité algorithmique trop élevée,
- ne profite pas des optimisations propres au langage ou au framework.

---

### 1.5 Génération de dépendances incompatibles
Le code généré peut :
- installer des versions instables,
- mélanger des versions majeures incompatibles,
- utiliser des bibliothèques non maintenues,
- faire appel à des API dépréciées.

Ce problème est fréquent dans Python, JavaScript, Java, Go et Rust.

---

### 1.6 Difficulté à maintenir le code généré
Sans commentaire pertinent ou logique claire, il devient difficile de :
- comprendre l’intention originale,
- déboguer,
- mettre à jour,
- modifier sans casser l’existant.

---

## 2. Risques liés à la sécurité

### 2.1 Vulnérabilités classiques non gérées
Le code généré peut laisser passer :
- injections SQL,
- failles XSS,
- attaques CSRF,
- contournement d’authentification,
- absence de validation des entrées.

---

### 2.2 Mécanismes cryptographiques incorrects
L’IA peut :
- implémenter sa propre cryptographie (extrêmement dangereux),
- utiliser des fonctions obsolètes (MD5, SHA1, RC4),
- générer des clés trop faibles,
- mal gérer les secrets ou la rotation des clés.

---

### 2.3 Manque de gestion d’erreurs sécurisée
L’IA peut produire :
- des messages d’erreur exposant des informations sensibles,
- des exceptions non gérées crashant le système,
- des logs contenant des données confidentielles.

---

### 2.4 Appels réseau non sécurisés
Exemples :
- utilisation de HTTP au lieu de HTTPS,
- absence de vérification de certificats,
- exposition involontaire d’endpoints internes,
- mauvaise gestion de timeouts et de retries.

---

### 2.5 Intégration de code malveillant involontaire
Bien que non intentionnel, un modèle peut générer :
- des dépendances contenant du malware,
- des commandes pouvant exécuter des scripts dangereux,
- des configurations facilitant la compromission du système.

---

## 3. Risques humains

### 3.1 Dépendance excessive
Une utilisation massive de l’IA peut entraîner :
- un recul des compétences de base,
- une incapacité à coder sans assistance,
- une perte de compréhension en profondeur.

---

### 3.2 Illusion de compétence
Le développeur peut croire :
- comprendre le code généré,
- maîtriser une technologie,
- avoir produit un code fiable,

alors que l’essentiel provient de l’IA.

---

### 3.3 Manque de revues de code sérieuses
Des équipes peuvent valider du code :
- sans relecture approfondie,
- sous pression de rapidité,
- en supposant que “l’IA a raison”.

Cela augmente massivement la dette technique.

---

## 4. Risques organisationnels

### 4.1 Perte de cohérence dans l’architecture
En utilisant l'IA pour produire différents modules :
- les conventions de code varient,
- les patterns deviennent incohérents,
- la structure globale perd sa logique.

---

### 4.2 Dégradation du workflow de développement
L’IA peut :
- contourner les processus standard,
- générer du code sans respecter les guidelines internes,
- ignorer les conventions de commits, les pipelines CI, les tests.

---

### 4.3 Faible reproductibilité
Le même prompt peut produire :
- une version différente du code,
- une solution incompatible,
- une alternative non vérifiable.

---

## 5. Risques juridiques

### 5.1 Propriété intellectuelle
Le code généré peut :
- ressembler à du code sous licence restrictive,
- inclure des extraits protégés,
- enfreindre des obligations légales ou contractuelles.

---

### 5.2 Incompatibilité de licences
L’IA peut proposer des dépendances sous :
- GPL,
- AGPL,
- LGPL,
- licences manipulant les conditions d'utilisation.

Certaines licences imposent des obligations industrielles incompatibles avec des projets commerciaux.

---

### 5.3 Confidentialité et protection des données
Selon l’outil, le code peut :
- être envoyé sur des serveurs externes,
- contenir des données sensibles,
- intégrer par erreur des identifiants ou secrets.

---

## 6. Risques stratégiques

### 6.1 Perte de maîtrise du produit
Si trop de code est généré automatiquement :
- le cœur du produit devient difficile à expliquer,
- la compréhension technique se perd,
- la maintenance dépend fortement de l’outil.

---

### 6.2 Risque de dépendance à un fournisseur
En fonction de l’IA utilisée :
- évolutions imprévisibles du modèle,
- coûts croissants,
- limitations futures,
- changements de politique d'utilisation.

---

## 7. Risques pédagogiques (chez les débutants)

### 7.1 Apprentissage superficiel
L'utilisateur peut :
- ne pas comprendre les bases du langage,
- ignorer les structures de données,
- ne pas savoir déboguer seul.

---

### 7.2 Mauvaise compréhension des erreurs
Les débutants ne peuvent pas toujours :
- expliquer pourquoi le code ne marche pas,
- corriger les bugs introduits,
- comprendre l'approche théorique.

---

### 7.3 Mauvaises habitudes codifiées
Exemples :
- copier-coller sans réflexion,
- absence de tests,
- dépendance aux prompts au lieu de la logique.

---

## 8. Risques liés à la gestion des prompts

### 8.1 Prompts mal formulés
Un prompt ambigu peut générer :
- du code dangereux,
- une mauvaise architecture,
- des idées incohérentes avec le projet.

---

### 8.2 Fuite de contexte
S'il faut donner beaucoup d'informations à l’IA, il existe un risque de :
- divulgation,
- surcharge contextuelle,
- perte de contrôle sur ce qui a été envoyé.

---

### 8.3 Hallucinations techniques
L’IA peut inventer :
- des fonctions qui n’existent pas,
- des arguments inexistants,
- des modules imaginaires,
- des solutions théoriques mais infaisables.

---

# Conclusion

Utiliser une IA pour coder est extrêmement puissant, mais comporte des risques lourds s'il n'y a pas :

- contrôle humain systématique,
- tests rigoureux,
- audit de sécurité,
- vérification de compatibilité,
- cohérence architecturale,
- ligne directrice claire,
- maturité dans l’usage des prompts.

L’IA doit être un accélérateur, pas un remplaçant du jugement humain.
