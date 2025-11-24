# Risques d'utiliser une IA pour coder

## 1. Vulnérabilités de sécurité

### Taux élevé de failles de sécurité

Dans 45% des cas testés, les modèles de langage (LLM) ont introduit des vulnérabilités classées dans le Top 10 de l'OWASP, selon une étude de Veracode. Java présente le plus grand risque avec un taux d'échec de sécurité supérieur à 70%, tandis que Python, C# et JavaScript affichent des taux d'échec entre 38% et 45%.

**Source:** [EC News - Le code généré par l'IA présente des risques pour la sécurité](https://www.ecinews.fr/fr/le-code-genere-par-lia-presente-des-risques-pour-la-securite/)

### Types de vulnérabilités fréquentes

Les LLM échouent à sécuriser le code contre les scripts intersites (CWE-80) dans 86% des cas et contre l'injection de logs (CWE-117) dans 88% des cas. Les injections SQL et attaques similaires deviennent plus faciles avec les vulnérabilités du code généré par l'IA.

**Sources:** 
- [EC News](https://www.ecinews.fr/fr/le-code-genere-par-lia-presente-des-risques-pour-la-securite/)
- [Kaspersky - Risques liés à la sécurité du vibe coding](https://www.kaspersky.fr/blog/vibe-coding-2025-risks/23307/)

### Faux sentiment de sécurité

Une étude de Stanford révèle que dans 4 tâches sur 5, les participants assistés par l'IA ont écrit du code moins sécurisé que ceux sans IA, représentant une augmentation de 80%. Ce phénomène s'explique par un excès de confiance dans le système, amenant les développeurs à négliger la vérification du code.

**Source:** [Louis-François Bouchard - Les Risques de Coder avec l'IA Générative](https://www.louisbouchard.ca/blog-ia/risques-coder-ia)

## 2. Risques liés à la chaîne d'approvisionnement

### Composants non vérifiés

L'utilisation de bibliothèques, outils et modèles pré-entraînés non vérifiés peut introduire des vulnérabilités ou des portes dérobées (backdoors). Une vigilance particulière doit être portée aux composants n'ayant pas fait l'objet d'une évaluation de sécurité approfondie.

**Sources:**
- [CNIL - Garantir la sécurité du développement d'un système d'IA](https://www.cnil.fr/fr/ia-garantir-la-securite-du-developpement)
- [ANSSI - Recommandations de sécurité pour un système d'IA générative](https://cyber.gouv.fr/sites/default/files/document/Recommandations_de_sécurité_pour_un_système_d_IA_générative.pdf)

### Vulnérabilités des plateformes

La vulnérabilité CurXecute (CVE-2025-54135) a permis aux pirates d'ordonner à Cursor d'exécuter des commandes arbitraires sur la machine du développeur. Les plateformes de génération de code peuvent elles-mêmes présenter des failles exploitables.

**Source:** [Kaspersky](https://www.kaspersky.fr/blog/vibe-coding-2025-risks/23307/)

## 3. Fuite de données sensibles

### Exposition de données confidentielles

La fuite de données sensibles de l'entité doit être une menace à prendre en compte, quel que soit le cas d'usage du système d'IA générative. Les développeurs peuvent involontairement partager du code propriétaire ou des informations confidentielles avec les services d'IA.

**Source:** [ANSSI](https://cyber.gouv.fr/sites/default/files/document/Recommandations_de_sécurité_pour_un_système_d_IA_générative.pdf)

### Risques des services mutualisés

L'ANSSI et le BSI soulignent les risques liés aux services mutualisés accessibles depuis Internet, où les données envoyées aux assistants de programmation peuvent être exposées.

**Source:** [ANSSI - Assistants de programmation basés sur l'IA](https://cyber.gouv.fr/actualites/lanssi-et-le-bsi-publient-leurs-recommandations-de-securite-concernant-les-assistants-de)

## 4. Propriété intellectuelle et droits d'auteur

### Absence de protection juridique

Une œuvre générée sans intervention humaine significative ne peut pas bénéficier de la protection par le droit d'auteur. En France, seule une personne physique peut être considérée comme auteur.

**Source:** [Alexia.fr - Intelligence artificielle et droit d'auteur](https://www.alexia.fr/fiche/12455/intelligence-artificielle-et-droit-d-auteur-ou-en-sommes-nous-en-2025.htm)

### Risques de contrefaçon

L'exploitation des données générées par l'IA est soumise aux droits d'auteur des auteurs des données d'entraînement. Les entreprises utilisant du code généré par IA peuvent involontairement violer des droits de propriété intellectuelle.

**Source:** [Village Justice - IA générative et propriété intellectuelle](https://www.village-justice.com/articles/generative-propriete-intellectuelle-les-defis-juridiques-les-perspectives,49889.html)

### Impact sur les acquisitions

Dans le cadre d'acquisitions, la présence de code généré par l'IA est scrutée avec des impacts potentiels sur la sécurité de la propriété intellectuelle et la viabilité commerciale.

**Source:** [Louis-François Bouchard](https://www.louisbouchard.ca/blog-ia/risques-coder-ia)

## 5. Dépendance et perte de compétences

### Atrophie des compétences

Le développement d'une dépendance excessive à l'IA entraîne une diminution de la capacité d'un développeur à coder de manière indépendante et à innover de manière créative.

**Source:** [Louis-François Bouchard](https://www.louisbouchard.ca/blog-ia/risques-coder-ia)

### Problèmes de maintenance

Sans compréhension approfondie du code généré, les développeurs peuvent rencontrer des difficultés lors du débogage ou de la maintenance du code à long terme.

## 6. Recommandations de l'ANSSI

L'ANSSI et le BSI recommandent d'aborder ces outils avec prudence malgré leurs avantages certains, car ils induisent de nouveaux risques de sécurité à différents stades du développement.

**Source:** [ANSSI](https://cyber.gouv.fr/actualites/lanssi-et-le-bsi-publient-leurs-recommandations-de-securite-concernant-les-assistants-de)

## 7. Mesures de prévention

Le niveau de risque peut être réduit par une combinaison de mesures :
- Révision automatique du code avec des outils SAST
- Intégration d'exigences de sécurité dans les invites système
- Revues de code par des spécialistes
- Formation des développeurs

**Source:** [Kaspersky](https://www.kaspersky.fr/blog/vibe-coding-2025-risks/23307/)

---

## Synthèse des sources principales

1. **EC News** - [Le code généré par l'IA présente des risques pour la sécurité](https://www.ecinews.fr/fr/le-code-genere-par-lia-presente-des-risques-pour-la-securite/)
2. **Kaspersky** - [Risques liés à la sécurité du vibe coding](https://www.kaspersky.fr/blog/vibe-coding-2025-risks/23307/)
3. **Louis-François Bouchard** - [Les Risques de Coder avec l'IA Générative](https://www.louisbouchard.ca/blog-ia/risques-coder-ia)
4. **CNIL** - [Garantir la sécurité du développement d'un système d'IA](https://www.cnil.fr/fr/ia-garantir-la-securite-du-developpement)
5. **ANSSI** - [Recommandations de sécurité pour un système d'IA générative](https://cyber.gouv.fr/sites/default/files/document/Recommandations_de_sécurité_pour_un_système_d_IA_générative.pdf)
6. **ANSSI** - [Assistants de programmation basés sur l'IA](https://cyber.gouv.fr/actualites/lanssi-et-le-bsi-publient-leurs-recommandations-de-securite-concernant-les-assistants-de)
7. **Alexia.fr** - [Intelligence artificielle et droit d'auteur](https://www.alexia.fr/fiche/12455/intelligence-artificielle-et-droit-d-auteur-ou-en-sommes-nous-en-2025.htm)
8. **Village Justice** - [IA générative et propriété intellectuelle](https://www.village-justice.com/articles/generative-propriete-intellectuelle-les-defis-juridiques-les-perspectives,49889.html)
