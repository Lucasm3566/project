# Risques liés à l'utilisation d'une IA pour coder  
*(version affinée + liens sources)*

Ce document synthétise les risques techniques, humains, organisationnels, juridiques et sécuritaires associés à l’usage d’IA génératives pour produire du code. Il s’appuie sur des travaux standards de cybersécurité, recherches universitaires et analyses institutionnelles.

---

# 1. Risques techniques

## 1.1 Bugs subtils et erreurs logiques
Le code généré peut comporter :
- erreurs de logique non détectées,
- cas limites oubliés,
- comportements imprévisibles,
- utilisations d’API obsolètes.

**Sources :**  
- Microsoft Research – Large Language Models and Software Engineering (2023)  
  https://www.microsoft.com/en-us/research/publication/large-language-models-and-software-engineering/  
- NIST – Adversarial Machine Learning: A Taxonomy  
  https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2.pdf

---

## 1.2 Code non fonctionnel ou incomplet
- code non compilable,
- dépendances incorrectes,
- méconnaissance de l’environnement réel.

**Sources :**  
- GitHub Copilot Study (2022)  
  https://arxiv.org/abs/2107.03374  
- Google DeepMind – Limitations of LLM Code Generation  
  https://arxiv.org/abs/2312.02153

---

## 1.3 Mauvaises pratiques
- patterns anti-architecturaux,
- style incohérent ou non idiomatique.

**Source :**  
- JetBrains – State of Developer Ecosystem  
  https://www.jetbrains.com/lp/devecosystem-2023/

---

## 1.4 Code non optimisé
- solutions naïves,
- mauvaise complexité,
- absence d’optimisation.

**Source :**  
- Stanford HAI – Can LLMs Optimize Code?  
  https://arxiv.org/abs/2310.13008

---

## 1.5 Dépendances incompatibles
- versions obsolètes,
- bibliothèques vulnérables.

**Sources :**  
- OWASP Dependency-Check  
  https://owasp.org/www-project-dependency-check/  
- Sonatype – State of the Software Supply Chain  
  https://www.sonatype.com/resources/state-of-the-software-supply-chain

---

## 1.6 Difficulté de maintenance
Code difficile à comprendre ou justifier.

**Source :**  
- IEEE Software – Maintainability Risks of Generated Code  
  https://ieeexplore.ieee.org/document/9609657

---

# 2. Risques de sécurité

## 2.1 Vulnérabilités classiques
- XSS, SQLi, CSRF,
- absence de validation d’entrées.

**Sources :**  
- OWASP – LLM Top 10  
  https://owasp.org/www-project-top-10-for-large-language-model-applications/  
- MIT – Security Analysis of LLM-Generated Code  
  https://arxiv.org/abs/2401.00262

---

## 2.2 Cryptographie incorrecte
- MD5, SHA1, RC4,
- mauvaise gestion des clés.

**Sources :**  
- NIST SP 800-175  
  https://csrc.nist.gov/publications/detail/sp/800-175b/final  
- ENISA – AI Threat Landscape 2023/2024  
  https://www.enisa.europa.eu/publications/artificial-intelligence-threat-landscape

---

## 2.3 Gestion d’erreurs dangereuse
- messages d’erreur sensibles,
- logs de secrets,
- exceptions non gérées.

---

## 2.4 Appels réseau non sécurisés
- HTTP non chiffré,
- absence de vérification TLS.

**Source :**  
- OWASP API Security Top 10  
  https://owasp.org/API-Security/

---

## 2.5 Code malveillant involontaire
- dépendances infectées,
- scripts dangereux.

**Sources :**  
- Checkmarx – AI Code Supply Chain Risks  
  https://checkmarx.com/blog/ai-generated-code-supply-chain-security-risks/  
- Sonatype Malware Report  
  https://www.sonatype.com/state-of-the-software-supply-chain

---

# 3. Risques humains

## 3.1 Dépendance excessive  
## 3.2 Illusion de compétence  
## 3.3 Revue de code négligée  

**Source :**  
- ACM – Human Factors in LLM-Assisted Programming  
  https://dl.acm.org/doi/10.1145/3597503.3623368

---

# 4. Risques organisationnels

## 4.1 Incohérence architecturale  
## 4.2 Dégradation du workflow  
## 4.3 Faible reproductibilité  

---

# 5. Risques juridiques

## 5.1 Propriété intellectuelle

**Sources :**  
- Harvard Journal of Law & Technology – Generative AI & Copyright  
  https://jolt.law.harvard.edu/assets/articlePDFs/v37/37HarvJLTech331.pdf  
- EFF – Copyright Issues with AI-Generated Code  
  https://www.eff.org/deeplinks/2023/08/copyright-and-generative-ai

---

## 5.2 Licences incompatibles  
## 5.3 Confidentialité et protection des données

**Sources :**  
- CNIL – IA & Données personnelles (2024)  
  https://www.cnil.fr/fr/intelligence-artificielle  
- NIST – AI Risk Management Framework  
  https://www.nist.gov/itl/ai-risk-management-framework

---

# 6. Risques stratégiques

## 6.1 Perte de maîtrise du produit  
## 6.2 Dépendance au fournisseur  

---

# 7. Risques pédagogiques

## 7.1 Apprentissage superficiel  
## 7.2 Mauvaise compréhension des erreurs  
## 7.3 Mauvaises habitudes  

---

# 8. Risques liés aux prompts

## 8.1 Prompts mal formulés  
## 8.2 Fuite de contexte  
## 8.3 Hallucinations techniques  

---

# Conclusion

L’IA est un outil d’accélération, pas un remplaçant du jugement humain.  
La qualité et la sécurité dépendent de :
- revues de code systématiques,  
- tests unitaires et d’intégration,  
- audit de sécurité,  
- contrôle des dépendances,  
- respect d’une architecture cohérente,  
- prompts maîtrisés et documentés.
