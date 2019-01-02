# Answers

Nom : de Solms
Prénom : Jean
NB : 1

# 1.
A quoi sert l'A/B testing ?
Il permet de tester une version d'une app/service/code sur une partie des utilisateurs selon un critère choisi.

Comment appliquer de l'A/B testing grâce à Istio ?
Istio nous permet de créer des routes permettant de rediriger une partie des utilisateurs sur une nouvelle version.

# 2.
Comment simuler un problème de timeout avec Istio ?
On peut utiliser une "fault injection".

Comment le résoudre ?
En optimisant le code ou en modifiant le "timeout"

# 3.
Qu'est-ce que le canary release ?
Le canary release permet de conduire seulement une partie des utilisateurs sur une nouvelle version mis en production.

En quoi est-ce utile ?
Elle permet de s'assurer que la version est stable et qu'elle satisfait les besoins utilisateurs

Comment l'implémenter dans Istio ?

route:
destination: host: website subset: version-2 weight: 5
destination: host: website subset: version-1 weight: 95

# 4.

# 5.
Qu'est-ce qu'un Circuit Breaker ?
Un circuit Breaker consiste à rediriger le flux en cas de malfonctionnement d'un service.

Comment l'implémenter dans un contexte Kubernetes ?
Les configuration de Kubernetes nous permettent d'instaurer des règles necessaires au Circuit Breaker

# 6.
Pourquoi avoir besoin de mirrorer le traffic vers un autre composant ?
Cela nous permet de modifier la version en prod sans trop de risques.
# 7.
Pourquoi bloquer le traffic vers un service ?
On bloque le trafic vers un service lorsque ce dernier est trop lent à répondre ou qu'il contient un erreur.
Ceci évite l'accumulation du temps de réponse et donc le ralentissement d'autres services.

Comment l'implémenter simplement avec Istio ?
Rate limit permet de l’implémenter facilement avec Istio

# 8.
Quel est la problématique de tracing distribué ?
La problématique de tracing distribué est de comprendre le comportement d'une application en détail

Quel est la spécification du tracing distribué et son implémentation dans Istio ?
Istio met à disposition un dashboard récapitulant toutes les requettes sur un service

# 9.
Comment s'appelle l'outil de récupération des métrics ?
Prometheus

# 10.

# 11.
Comment s'appelle l'outil de visualisation des métrics ?
Grafana

# 12.
A quoi sert un servicegraph ?
Un servicegraph permet de visualiser dans un graph l'ensemble du trafic de données correspondant à un service

Quel serait l'utilité dans le quotidien d'un ops ?
Ceci peut lui permettre d'identifier les points faibles de son service, quels sont les bouts de code à optimiser pour rendre son app plus efficace
