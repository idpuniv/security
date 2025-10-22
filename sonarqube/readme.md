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

