
outils 



# ApacheBench (simple)
10 personnes envoient 1000 requêtes AU TOTAL, en même temps
ab -n 1000 -c 10 http://localhost/counter  

# Siege (plus avancé)
10 personnes bombardent le site pendant 30 secondes, sans compter combien de coups
siege -c 10 -t 30s http://localhost/counter

# k6 (moderne, scriptable)
10 personnes naviguent pendant 30 secondes conforment au senario decrit dans scripts.js
k6 run --vus 10 --duration 30s script.js
