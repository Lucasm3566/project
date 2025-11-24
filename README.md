# **_Risques liés à l'utilisation d'une IA pour coder (version très détaillée et exhaustive)_**

Ce document rassemble l’ensemble des risques connus, directs et indirects, liés à l’usage d’une <a href="https://www.google.com/search?q=intelligence+artificielle+g%C3%A9n%C3%A9rative" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">intelligence artificielle générative</a> pour la production de code.  
Il couvre les aspects techniques, humains, organisationnels, juridiques et sécuritaires.

---

## 1. Risques techniques

### 1.1 Bugs subtils et erreurs logiques
L’IA peut générer du code :  
- qui semble correct mais ne respecte pas parfaitement les <a href="https://www.google.com/search?q=sp%C3%A9cifications+fonctionnelles" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">spécifications fonctionnelles</a>,  
- qui omet des cas limites (données <a href="https://www.google.com/search?q=null" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">null</a>, dépassements, données <a href="https://www.google.com/search?q=donn%C3%A9es+corrompues" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">corrompues</a>),  
- qui contient des <a href="https://www.google.com/search?q=erreurs+logiques" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">erreurs logiques</a> difficiles à détecter,  
- qui réutilise des <a href="https://www.google.com/search?q=approches+obsol%C3%A8tes" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">approches obsolètes</a>,  
- qui produit des comportements <a href="https://www.google.com/search?q=impr%C3%A9visibles+en+production" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">imprévus en production</a>.

**Pourquoi ?**  
L’IA n’exécute pas le code, elle anticipe statistiquement ce qui “semble correct”.

---

### 1.2 Code non fonctionnel ou incomplet
Le code produit peut :  
- ne pas <a href="https://www.google.com/search?q=compiler" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">compiler</a>,  
- dépendre de <a href="https://www.google.com/search?q=biblioth%C3%A8ques+incompatibles" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">bibliothèques incompatibles</a>,  
- être insuffisamment <a href="https://www.google.com/search?q=test%C3%A9" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">testé</a>,  
- reposer sur des <a href="https://www.google.com/search?q=suppositions+incorrectes" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">suppositions incorrectes</a>.

---

### 1.3 Utilisation de mauvaises pratiques
L’IA peut produire :  
- des <a href="https://www.google.com/search?q=structures+inefficaces" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">structures inefficaces</a>,  
- des <a href="https://www.google.com/search?q=duplications+de+code" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">duplications de code</a>,  
- des <a href="https://www.google.com/search?q=patterns+anti-architecture" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">patterns anti-architecture</a> (god objects, couplage excessif),  
- des solutions <a href="https://www.google.com/search?q=non+idiomatiques" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">non idiomatiques</a>.

---

### 1.4 Code non optimisé
L'IA peut générer du code qui :  
- consomme plus de <a href="https://www.google.com/search?q=m%C3%A9moire" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">mémoire</a>,  
- effectue des <a href="https://www.google.com/search?q=op%C3%A9rations+inutiles" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">opérations inutiles</a>,  
- adopte une <a href="https://www.google.com/search?q=complexit%C3%A9+algorithmique+excessive" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">complexité algorithmique excessive</a>,  
- ne profite pas des <a href="https://www.google.com/search?q=optimisations+langage+framework" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">optimisations natives du langage ou framework</a>.

---

### 1.5 Génération de dépendances incompatibles
Le code généré peut :  
- installer des versions <a href="https://www.google.com/search?q=instables" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">instables</a>,  
- mélanger des versions <a href="https://www.google.com/search?q=incompatibles" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">incompatibles</a>,  
- utiliser des <a href="https://www.google.com/search?q=biblioth%C3%A8ques+non+maintenues" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">bibliothèques non maintenues</a>,  
- faire appel à des <a href="https://www.google.com/search?q=API+d%C3%A9pr%C3%A9ci%C3%A9es" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">API dépréciées</a>.

---

### 1.6 Difficulté à maintenir le code généré
Sans <a href="https://www.google.com/search?q=commentaires+pertinents" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">commentaires pertinents</a>, il devient difficile de :  
- comprendre l’intention originale,  
- <a href="https://www.google.com/search?q=d%C3%A9boguer" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">déboguer</a>,  
- mettre à jour,  
- modifier sans casser l’existant.

---

## 2. Risques liés à la sécurité

### 2.1 Vulnérabilités classiques non gérées
Le code généré peut laisser passer :  
- <a href="https://www.google.com/search?q=injections+SQL" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">injections SQL</a>,  
- <a href="https://www.google.com/search?q=XSS" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">failles XSS</a>,  
- <a href="https://www.google.com/search?q=CSRF" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">attaques CSRF</a>,  
- contournement d’authentification,  
- absence de <a href="https://www.google.com/search?q=validation+des+entr%C3%A9es" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">validation des entrées</a>.

---

### 2.2 Mécanismes cryptographiques incorrects
L’IA peut :  
- implémenter sa propre <a href="https://www.google.com/search?q=cryptographie" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">cryptographie</a>,  
- utiliser des fonctions <a href="https://www.google.com/search?q=obsol%C3%A8tes+MD5+SHA1+RC4" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">obsolètes</a>,  
- générer des <a href="https://www.google.com/search?q=cl%C3%A9s+faibles" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">clés faibles</a>,  
- mal gérer les <a href="https://www.google.com/search?q=secrets" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">secrets</a>.

---

### 2.3 Manque de gestion d’erreurs sécurisée
L’IA peut produire :  
- des messages d’erreur exposant des informations sensibles,  
- des <a href="https://www.google.com/search?q=exceptions+non+g%C3%A9r%C3%A9es" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">exceptions non gérées</a>,  
- des logs contenant des <a href="https://www.google.com/search?q=donn%C3%A9es+confidentielles" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">données confidentielles</a>.

---

## 3. Risques humains

### 3.1 Dépendance excessive
Une utilisation massive de l’IA peut entraîner :  
- un recul des <a href="https://www.google.com/search?q=comp%C3%A9tences+de+base" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">compétences de base</a>,  
- une incapacité à coder sans assistance,  
- une perte de compréhension approfondie du code.

### 3.2 Illusion de compétence
Le développeur peut croire :  
- comprendre le code généré,  
- maîtriser une <a href="https://www.google.com/search?q=technologie" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">technologie</a>,  
- avoir produit un code fiable,  
alors que l’essentiel provient de l’IA.

### 3.3 Manque de revues de code sérieuses
Des équipes peuvent valider du code :  
- sans relecture approfondie,  
- sous pression de rapidité,  
- en supposant que “l’IA a raison”.  

Cela augmente massivement la <a href="https://www.google.com/search?q=dette+technique" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">dette technique</a>.

---

## 4. Risques organisationnels

### 4.1 Perte de cohérence dans l’architecture
En utilisant l'IA pour produire différents modules :  
- les <a href="https://www.google.com/search?q=conventions+de+code" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">conventions de code</a> varient,  
- les <a href="https://www.google.com/search?q=patterns" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">patterns</a> deviennent incohérents,  
- la <a href="https://www.google.com/search?q=structure+globale" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">structure globale</a> perd sa logique.

### 4.2 Dégradation du workflow de développement
L’IA peut :  
- contourner les processus standard,  
- générer du code sans respecter les <a href="https://www.google.com/search?q=guidelines+internes" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">guidelines internes</a>,  
- ignorer les conventions de commits, pipelines CI et tests.

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

### 5.2 Incompatibilité de licences
L’IA peut proposer des dépendances sous :  
- GPL, AGPL, LGPL,  
- licences manipulant les conditions d'utilisation.  

Certaines licences imposent des obligations incompatibles avec des projets commerciaux.

### 5.3 Confidentialité et protection des données
Selon l’outil, le code peut :  
- être envoyé sur des serveurs externes,  
- contenir des <a href="https://www.google.com/search?q=donn%C3%A9es+sensibles" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">données sensibles</a>,  
- intégrer par erreur des identifiants ou <a href="https://www.google.com/search?q=secrets" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">secrets</a>.

---

## 6. Risques stratégiques

### 6.1 Perte de maîtrise du produit
Si trop de code est généré automatiquement :  
- le cœur du produit devient difficile à expliquer,  
- la compréhension technique se perd,  
- la maintenance dépend fortement de l’outil.

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
- ignorer les <a href="https://www.google.com/search?q=structures+de+donn%C3%A9es" target="_blank" style="color:red; font-weight:bold; text-decoration:none;">structures de données</a>,  
- ne pas savoir déboguer seul.

### 7.2 Mauvaise compréhension des erreurs
Les débutants ne peuvent pas toujours :  
- expliquer pourquoi le code ne marche pas,  
- corriger les bugs introduits,  
- comprendre l'approche théorique.

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

### 8.2 Fuite de contexte
S'il faut donner beaucoup d'informations à l’IA, il existe un risque de :  
- divulgation,  
- surcharge contextuelle,  
- perte de contrôle sur ce qui a été envoyé.

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
