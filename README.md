# **_Risques liés à l'utilisation d'une IA pour coder (version très détaillée et exhaustive)_**

Ce document rassemble l’ensemble des risques connus, directs et indirects, liés à l’usage d’une [**intelligence artificielle générative**](https://www.google.com/search?q=intelligence+artificielle+g%C3%A9n%C3%A9rative) pour la production de code.  
Il couvre les aspects techniques, humains, organisationnels, juridiques et sécuritaires.

**Sources :**  
- [OpenAI Safety Best Practices](https://platform.openai.com/docs/guides/safety)  
- [Wikipedia – Generative AI](https://en.wikipedia.org/wiki/Generative_artificial_intelligence)

---

## 1. Risques techniques

### 1.1 Bugs subtils et erreurs logiques
L’IA peut générer du code :  
- qui semble correct mais ne respecte pas parfaitement les [**spécifications fonctionnelles**](https://www.google.com/search?q=sp%C3%A9cifications+fonctionnelles),  
- qui omet des cas limites (données [**null**](https://www.google.com/search?q=null), dépassements, données [**corrompues**](https://www.google.com/search?q=donn%C3%A9es+corrompues)),  
- qui contient des [**erreurs logiques**](https://www.google.com/search?q=erreurs+logiques) difficiles à détecter,  
- qui réutilise des [**approches obsolètes**](https://www.google.com/search?q=approches+obsol%C3%A8tes),  
- qui produit des comportements [**imprévus en production**](https://www.google.com/search?q=impr%C3%A9visibles+en+production).  

**Pourquoi ?** L’IA n’exécute pas le code, elle anticipe statistiquement ce qui “semble correct”.  

**Sources :**  
- [AI-Generated Code Risks – ACM](https://dl.acm.org/doi/10.1145/3446871)  
- [Stack Overflow Developer Survey 2023](https://survey.stackoverflow.co/2023/)

---

### 1.2 Code non fonctionnel ou incomplet
Le code produit peut :  
- ne pas [**compiler**](https://www.google.com/search?q=compiler),  
- dépendre de [**bibliothèques incompatibles**](https://www.google.com/search?q=biblioth%C3%A8ques+incompatibles),  
- être insuffisamment [**testé**](https://www.google.com/search?q=test%C3%A9),  
- reposer sur des [**suppositions incorrectes**](https://www.google.com/search?q=suppositions+incorrectes).  

**Sources :**  
- [GitHub – Copilot Security Risks](https://docs.github.com/en/copilot/security-and-privacy)  
- [IEEE Software – AI in Development](https://ieeexplore.ieee.org/document/9523772)

---

### 1.3 Utilisation de mauvaises pratiques
L’IA peut produire :  
- des [**structures inefficaces**](https://www.google.com/search?q=structures+inefficaces),  
- des [**duplications de code**](https://www.google.com/search?q=duplications+de+code),  
- des [**patterns anti-architecture**](https://www.google.com/search?q=patterns+anti-architecture) (god objects, couplage excessif),  
- des solutions [**non idiomatiques**](https://www.google.com/search?q=non+idiomatiques).  

**Sources :**  
- [Refactoring Guru – Code Smells](https://refactoring.guru/smells)  
- [Martin Fowler – Software Architecture](https://martinfowler.com/)

---

### 1.4 Code non optimisé
L'IA peut générer du code qui :  
- consomme plus de [**mémoire**](https://www.google.com/search?q=m%C3%A9moire),  
- effectue des [**opérations inutiles**](https://www.google.com/search?q=op%C3%A9rations+inutiles),  
- adopte une [**complexité algorithmique excessive**](https://www.google.com/search?q=complexit%C3%A9+algorithmique+excessive),  
- ne profite pas des [**optimisations natives du langage ou framework**](https://www.google.com/search?q=optimisations+langage+framework).  

**Sources :**  
- [Big-O Complexity](https://en.wikipedia.org/wiki/Big_O_notation)  
- [High Performance JavaScript](https://www.oreilly.com/library/view/high-performance-javascript/9780596802798/)

---

### 1.5 Génération de dépendances incompatibles
Le code généré peut :  
- installer des versions [**instables**](https://www.google.com/search?q=instables),  
- mélanger des versions [**incompatibles**](https://www.google.com/search?q=incompatibles),  
- utiliser des [**bibliothèques non maintenues**](https://www.google.com/search?q=biblioth%C3%A8ques+non+maintenues),  
- faire appel à des [**API dépréciées**](https://www.google.com/search?q=API+d%C3%A9pr%C3%A9ci%C3%A9es).  

**Sources :**  
- [NPM Security Practices](https://docs.npmjs.com/cli/v9/configuring-npm/package-json#dependencies)  
- [OWASP Dependency Check](https://owasp.org/www-project-dependency-check/)

---

### 1.6 Difficulté à maintenir le code généré
Sans [**commentaires pertinents**](https://www.google.com/search?q=commentaires+pertinents), il devient difficile de :  
- comprendre l’intention originale,  
- [**déboguer**](https://www.google.com/search?q=d%C3%A9boguer),  
- mettre à jour,  
- modifier sans casser l’existant.  

**Sources :**  
- [Clean Code – Robert C. Martin](https://www.oreilly.com/library/view/clean-code-a/9780136083238/)  
- [IEEE Software – AI Maintainability](https://ieeexplore.ieee.org/document/9322333)

---

## 2. Risques liés à la sécurité

### 2.1 Vulnérabilités classiques non gérées
Le code généré peut laisser passer :  
- [**injections SQL**](https://owasp.org/www-community/attacks/SQL_Injection),  
- [**failles XSS**](https://owasp.org/www-community/attacks/xss/),  
- [**attaques CSRF**](https://owasp.org/www-community/attacks/csrf),  
- contournement d’authentification,  
- absence de [**validation des entrées**](https://owasp.org/www-project-top-ten/).

**Sources :**  
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)  
- [Security Risks of AI-generated Code](https://dl.acm.org/doi/10.1145/3454122)

---

### 2.2 Mécanismes cryptographiques incorrects
L’IA peut :  
- implémenter sa propre [**cryptographie**](https://www.google.com/search?q=cryptographie),  
- utiliser des fonctions [**obsolètes**](https://www.google.com/search?q=obsol%C3%A8tes+MD5+SHA1+RC4),  
- générer des [**clés faibles**](https://www.google.com/search?q=cl%C3%A9s+faibles),  
- mal gérer les [**secrets**](https://www.google.com/search?q=secrets).  

**Sources :**  
- [OWASP Cryptographic Storage](https://owasp.org/www-project-top-ten/2017/A3_2017-Sensitive_Data_Exposure.html)  
- [NIST Cryptography Guidelines](https://csrc.nist.gov/projects/cryptographic-standards-and-guidelines)

---

### 2.3 Manque de gestion d’erreurs sécurisée
L’IA peut produire :  
- des messages d’erreur exposant des informations sensibles,  
- des [**exceptions non gérées**](https://www.google.com/search?q=exceptions+non+g%C3%A9r%C3%A9es),  
- des logs contenant des [**données confidentielles**](https://www.google.com/search?q=donn%C3%A9es+confidentielles).  

**Sources :**  
- [OWASP Logging Security](https://owasp.org/www-project-top-ten/2017/A6_2017-Security_Misconfiguration.html)  
- [IEEE – Error Handling in AI Systems](https://ieeexplore.ieee.org/document/9390012)

---

## 3. Risques humains

### 3.1 Dépendance excessive
Une utilisation massive de l’IA peut entraîner :  
- un recul des [**compétences de base**](https://www.google.com/search?q=comp%C3%A9tences+de+base),  
- une incapacité à coder sans assistance,  
- une perte de compréhension approfondie du code.

**Sources :**  
- [ACM Digital Library – Human Factors in AI](https://dl.acm.org/doi/10.1145/3313831)  
- [Stack Overflow Developer Survey 2023](https://survey.stackoverflow.co/2023/)

### 3.2 Illusion de compétence
Le développeur peut croire :  
- comprendre le code généré,  
- maîtriser une [**technologie**](https://www.google.com/search?q=technologie),  
- avoir produit un code fiable,  
alors que l’essentiel provient de l’IA.

**Sources :**  
- [Dunning-Kruger Effect in Programming](https://www.sciencedirect.com/science/article/pii/S0742051X21001436)

### 3.3 Manque de revues de code sérieuses
Des équipes peuvent valider du code :  
- sans relecture approfondie,  
- sous pression de rapidité,  
- en supposant que “l’IA a raison”.  

Cela augmente massivement la [**dette technique**](https://www.google.com/search?q=dette+technique).

**Sources :**  
- [Martin Fowler – Technical Debt](https://martinfowler.com/bliki/TechnicalDebt.html)

---

## 4. Risques organisationnels

### 4.1 Perte de cohérence dans l’architecture
En utilisant l'IA pour produire différents modules :  
- les [**conventions de code**](https://www.google.com/search?q=conventions+de+code) varient,  
- les [**patterns**](https://www.google.com/search?q=patterns) deviennent incohérents,  
- la [**structure globale**](https://www.google.com/search?q=structure+globale) perd sa logique.

**Sources :**  
- [IEEE Software – Software Architecture](https://ieeexplore.ieee.org/document/9032331)

### 4.2 Dégradation du workflow de développement
L’IA peut :  
- contourner les processus standard,  
- générer du code sans respecter les [**guidelines internes**](https://www.google.com/search?q=guidelines+internes),  
- ignorer les conventions de commits, pipelines CI et tests.

**Sources :**  
- [Agile Alliance – Dev Workflow](https://www.agilealliance.org/glossary/devops/)

### 4.3 Faible reproductibilité
Le même prompt peut produire :  
- une version différente du code,  
- une solution incompatible,  
- une alternative non vérifiable.

**Sources :**  
- [ACM Transactions on Software Engineering – Reproducibility](https://dl.acm.org/doi/10.1145/3411764)

---

## 5. Risques juridiques

### 5.1 Propriété intellectuelle
Le code généré peut :  
- ressembler à du code sous licence restrictive,  
- inclure des extraits protégés,  
- enfreindre des obligations légales ou contractuelles.

**Sources :**  
- [GitHub Copilot Licensing FAQ](https://docs.github.com/en/copilot/getting-started-with-github-copilot/about-github-copilot#licensing)

### 5.2 Incompatibilité de licences
L’IA peut proposer des dépendances sous :  
- GPL, AGPL, LGPL,  
- licences manipulant les conditions d'utilisation.  

Certaines licences imposent des obligations incompatibles avec des projets commerciaux.

**Sources :**  
- [Open Source Initiative – License Types](https://opensource.org/licenses)

### 5.3 Confidentialité et protection des données
Selon l’outil, le code peut :  
- être envoyé sur des serveurs externes,  
- contenir des [**données sensibles**](https://www.google.com/search?q=donn%C3%A9es+sensibles),  
- intégrer par erreur des identifiants ou [**secrets**](https://www.google.com/search?q=secrets).

**Sources :**  
- [GDPR Compliance Guide](https://gdpr.eu/)  
- [OpenAI Data Usage Policy](https://openai.com/policies/data-usage)

---

## 6. Risques stratégiques

### 6.1 Perte de maîtrise du produit
Si trop de code est généré automatiquement :  
- le cœur du produit devient difficile à expliquer,  
- la compréhension technique se perd,  
- la maintenance dépend fortement de l’outil.

**Sources :**  
- [IEEE – Strategic Risks of AI](https://ieeexplore.ieee.org/document/9321122)

### 6.2 Risque de dépendance à un fournisseur
En fonction de l’IA utilisée :  
- évolutions imprévisibles du modèle,  
- coûts croissants,  
- limitations futures,  
- changements de politique d'utilisation.

**Sources :**  
- [Vendor Lock-in Risks – ACM](https://dl.acm.org/doi/10.1145/3460172)

---

## 7. Risques pédagogiques (chez les débutants)

### 7.1 Apprentissage superficiel
L'utilisateur peut :  
- ne pas comprendre les bases du langage,  
- ignorer les [**structures de données**](https://www.google.com/search?q=structures+de+donn%C3%A9es),  
- ne pas savoir déboguer seul.

**Sources :**  
- [IEEE Transactions on Education](https://ieeexplore.ieee.org/document/9381001)

### 7.2 Mauvaise compréhension des erreurs
Les débutants ne peuvent pas toujours :  
- expliquer pourquoi le code ne marche pas,  
- corriger les bugs introduits,  
- comprendre l'approche théorique.

**Sources :**  
- [ACM Education Reports](https://dl.acm.org/doi/10.1145/3429789)

### 7.3 Mauvaises habitudes codifiées
Exemples :  
- copier-coller sans réflexion,  
- absence de tests,  
- dépendance aux prompts au lieu de la logique.

**Sources :**  
- [IEEE Software – Coding Practices](https://ieeexplore.ieee.org/document/9322211)

---

## 8. Risques liés à la gestion des prompts

### 8.1 Prompts mal formulés
Un prompt ambigu peut générer :  
- du code dangereux,  
- une mauvaise architecture,  
- des idées incohérentes avec le projet.

**Sources :**  
- [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompting)

### 8.2 Fuite de contexte
S'il faut donner beaucoup d'informations à l’IA, il existe un risque de :  
- divulgation,  
- surcharge contextuelle,  
- perte de contrôle sur ce qui a été envoyé.

**Sources :**  
- [AI Privacy Risks – IEEE](https://ieeexplore.ieee.org/document/9387763)

### 8.3 Hallucinations techniques
L’IA peut inventer :  
- des fonctions qui n’existent pas,  
- des arguments inexistants,  
- des modules imaginaires,  
- des solutions théoriques mais infaisables.

**Sources :**  
- [OpenAI – AI Hallucinations](https://platform.openai.com/docs/guides/gpt-best-practices)

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

**Sources générales :**  
- [OpenAI Safety Best Practices](https://platform.openai.com/docs/guides/safety)  
- [ACM Digital Library – AI Risks](https://dl.acm.org/)  
- [IEEE Software – AI in Software Development](https://ieeexplore.ieee.org/)
