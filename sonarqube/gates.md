| Catégorie                         | Seuils que tu utilises     | Conforme au standard ? |
| --------------------------------- | -------------------------- | ---------------------- |
| Security = 0 vulnérabilités       | ✅ Oui                      |                        |
| Hotspots < 5                      | ✅ Oui (souple et réaliste) |                        |
| Bugs = 0 critiques / <10 majeures | ✅ Oui                      |                        |
| Maintainability ≤ 5 % / A-B       | ✅ Oui                      |                        |
| Coverage ≥ 60 %                   | ✅ Oui                      |                        |
| Duplication < 10 %                | ✅ Oui                      |                        |



| **Condition**                        | **Opérateur** | **Seuil** | **Action** |
| ------------------------------------ | ------------- | --------- | ---------- |
| **Reliability Rating**               | worse than    | A         | Fail       |
| **Security Rating**                  | worse than    | A         | Fail       |
| **Maintainability Rating**           | worse than    | A         | Fail       |
| **Coverage on New Code**             | less than     | 80%       | Fail       |
| **Duplicated Lines (%) on New Code** | greater than  | 3%        | Fail       |
| **Code Smells on New Code**          | greater than  | 0         | Fail       |
| **New Bugs**                         | greater than  | 0         | Fail       |
| **New Vulnerabilities**              | greater than  | 0         | Fail       |


# Lecture des expressions des gates 

| Métrique                     | Opérateur        | Valeur | Lecture                                                                 |
|-------------------------------|----------------|--------|------------------------------------------------------------------------|
| Issue                         | Is greater than | 0      | Ça échoue tant que le nombre de problèmes est supérieur à 0             |
| Security Hotspots Reviewed    | Is less than    | 100%   | Ça échoue tant que le nombre de problèmes revus est inférieur à 100%   |
| Coverage                      | Is less than    | 80%    | Ça échoue tant que la couverture est inférieure à 80%                  |
| Duplicated Lines (%)          | Is greater than | 3%     | Ça échoue tant que le nombre de lignes dupliquées est supérieur à 3%   |


Rating 
Comprendre les regles (les metrics et les sens des operations)
