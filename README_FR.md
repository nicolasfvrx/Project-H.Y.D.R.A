# H.Y.D.R.A.

### High-Yield Distributed Rack Assembly
*(Infrastructure de Refroidissement Centralisée pour Rack 19")*

**H.Y.D.R.A.** est un projet d'infrastructure spécialisé dans la conception d'un **système de refroidissement liquide centralisé** pour les environnements en rack 19 pouces multi-nœuds.

Au lieu de refroidir chaque machine de manière isolée, H.Y.D.R.A. consolide la gestion thermique dans un "Cœur" unique et haute performance (un châssis 4U dédié) qui dessert plusieurs "Têtes" indépendantes (PC, serveurs ou NAS) au sein du même rack.

---

## 🌌 Le Concept

Le projet repose sur la philosophie de la **consolidation thermique**. En déplaçant l'échange de chaleur à l'extérieur des boîtiers individuels vers une boucle centralisée, nous obtenons :

* **Déplacement du bruit :** Toutes les nuisances sonores mécaniques (ventilateurs et pompes) sont concentrées dans une zone optimisée ou déportées.
* **Efficacité thermique :** L'utilisation de dissipateurs externes massifs offre une capacité d'absorption de chaleur qu'un boîtier standard ne peut égaler.
* **Modularité du système :** Les nœuds peuvent être ajoutés ou retirés de la grille via des interfaces de déconnexion rapide (Quick Disconnects) sans interrompre le fonctionnement global du système.

## 🏗️ Architecture

Le système H.Y.D.R.A. est divisé en trois couches principales :

### 1. Le Cœur (Châssis de Refroidissement)
Une unité dédiée montée en rack qui abrite le réservoir central, un réseau redondant de pompes industrielles et la logique de contrôle primaire. C'est le moteur du système, garantissant une pression et un débit constants sur toute la grille.

### 2. La Grille de Distribution (Manifold)
Un système de collecteurs hydrauliques à haute pression qui divise le flux principal en plusieurs lignes parallèles. Chaque ligne est équilibrée pour s'assurer qu'une station de travail GPU performante et un nœud de stockage basse consommation reçoivent précisément le débit nécessaire.

### 3. La Couche de Monitoring (Télémétrie)
Un système complet de capteurs qui surveille la santé de la boucle. En utilisant des sondes industrielles (débit, pression différentielle, conductivité), le système fournit des données en temps réel exportées vers un environnement Linux pour des analyses de performance avancées (Grafana) et des protocoles de sécurité automatisés.

## 🚀 Caractéristiques Clés

* **Redondance N+1 :** Plusieurs pompes travaillant en harmonie pour garantir qu'une défaillance unique ne compromette pas le refroidissement de tout le rack.
* **Dissipation Centralisée :** La chaleur est rejetée par des échangeurs thermiques externes massifs, maintenant l'environnement du rack stable et frais.
* **Équilibrage de flux intelligent :** Gestion dynamique des fluides pour maintenir une pression optimale quel que soit le nombre de nœuds actifs.
* **Monitoring Ouvert :** Conçu pour être indépendant de l'OS, avec des données accessibles pour des tableaux de bord personnalisés et des alertes à distance.

---

> *"Coupez un nœud, les autres resteront au frais."*
