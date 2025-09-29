# Product Owner de deux tornades humaines : mes 5 métriques pour piloter le chaos

## Comment mes compétences en gestion de produit ont survécu à l'épreuve du feu : la parentalité.

### À 6h30, mon premier incident critique de la journée

Le réveil de mon mari sonne. Dans le noir de notre chambre, je retiens mon souffle. La première métrique de la journée vient de s'activer : **le temps que met mon mari à éteindre son réveil**. Ça ne se mesure pas toujours en secondes. Parfois même pas en minutes, mais en dizaines de minutes.

Et pendant ce temps ? Je suis un Prometheus en mode alerte, tous mes capteurs en éveil. Vont-ils l'entendre ? Est-ce que je vais réussir à grappiller encore 30 minutes de tranquillité (voire de sommeil après une nuit plus qu'agitée) ?

Puis, le premier cri. Très souvent à l'instant même où mon mari franchit le seuil de la maison. Mon **temps de réponse** doit être inférieur à 3 millisecondes si je veux espérer ne pas avoir un double réveil. L'objectif : extraire le plus matinal de la chambre, le changer, le câliner, préparer le petit-déjeuner. Quand son frère sera aussi debout, ce sera plus compliqué de donner l'attention que chacun nécessite à son réveil et du coup... pleurs.

*Fail critique.*

Bienvenue dans mon dashboard Grafana mental. Celui que je consulte 24h/24, 7j/7, depuis que je suis mère.

---

### Mon architecture de monitoring familial

En Product Management, on mesure tout. Le taux de conversion, le churn, l'engagement utilisateur, le temps de réponse. On ne pilote bien que ce qu'on mesure, dit-on.

Devenir mère, c'est découvrir qu'on devient aussi une infrastructure de monitoring ambulante. Un Prometheus qui ne se met jamais en veille, avec des capteurs hypersensibles et un Alertmanager aux seuils de warning particulièrement... sensibles.

Voici mes cinq (principales) métriques de survie quotidienne.

---

### Métrique #1 : Mean Time Between Wakeups (MTBW)

**Valeur cible :** 10 heures  
**Meilleure performance actuelle :** 2 heures  
**SLA respecté :** Jamais

Cette métrique mesure la durée moyenne entre deux réveils nocturnes. Dans un monde idéal, mes "utilisateurs finaux" ne m'enverraient aucune requête entre 21h et 7h. Dans la réalité, mon système reçoit des alertes toutes les deux heures. Parfois plus.

*"Maman, j'ai soif."* *"Maman, j'ai fait un cauchemar."* *"Maman, où tu es ?"*

Ce que cette métrique m'apprend en tant que PO : **la disponibilité totale a un coût insoutenable**. Je dois donc faire des arbitrages conscients. Je choisis de dégrader temporairement un service non-essentiel (mon sommeil) pour garantir la performance sur un KPI critique : la satisfaction et la sécurité de mes utilisateurs.

---

### Métrique #2 : Niveau de criticité de la couche

**Échelle :** Vert → Orange → Rouge → Code brun  
**Temps de résolution critique :** < 2 minutes

Ah, la gestion des incidents. Quand est-ce qu'elle va déborder ? A-t-on encore le temps de finir cette tâche ou bien faut-il interrompre immédiatement pour éviter le désastre ?

C'est une métrique qui requiert une évaluation constante et une prise de décision rapide basée sur des signaux faibles : l'odeur, le comportement de l'enfant, le temps écoulé depuis le dernier change.

En Product Management, on parle de "dette technique". Ici, c'est de la dette... organique. Plus on attend, plus la résolution devient complexe et coûteuse. Un débordement de couche, c'est un incident P0 qui mobilise toutes les ressources.

Ce que cette métrique m'apprend en tant que PO : **anticiper un problème coûte infiniment moins cher que de gérer une crise**. Le monitoring proactif et la maintenance préventive ne sauvent pas que des bodys : ils sauvent des ressources.

---

### Métrique #3 : Seuil critique de décibels

**Alerte haute :** Douleur ? Danger ? Fatigue extrême ?  
**Alerte basse :** Silence = Bêtise en cours

Cette métrique est fascinante car elle nécessite une interprétation bidirectionnelle. Trop de bruit déclenche une alerte. Mais *pas assez de bruit* aussi.

Quand le volume sonore dépasse 85 décibels, j'enclenche le mode intervention d'urgence. Quelqu'un a mal, peur, ou est en surcharge émotionnelle.

Mais quand le silence règne trop longtemps dans la pièce d'à côté ? Alerte aussi. Un enfant silencieux est un enfant qui teste les limites de la physique avec le tube de crème solaire et le canapé en tissu.

Ce que cette métrique m'apprend en tant que PO : **les anomalies ne sont pas toujours dans le bruit**. L'absence de signal est une donnée critique. Un produit sans feedback utilisateur (ni positif, ni négatif) est un produit dont on ignore le véritable état de santé.

---

### Métrique #4 : Time to Fall Asleep (TTFA)

**Objectif :** < 15 minutes  
**Réalité moyenne :** 65 minutes  
**[Degraded mode] :** 2 heures (avec rebonds multiples)

Cette métrique mesure le temps nécessaire pour réussir enfin à lâcher un enfant endormi dans son lit sans qu'il se réveille instantanément. C'est un processus délicat qui demande une synchronisation parfaite, une exécution technique irréprochable et une gestion du risque à chaque craquement de parquet.

Certains soirs, après trois tentatives échouées, je reste assise au sol dans le noir, un enfant endormi dans les bras, à me demander si je vais passer la nuit dans cette position.

Ce que cette métrique m'apprend en tant que PO : **le *last mile* est souvent le plus critique**. Un produit parfaitement fonctionnel en staging (l'enfant endormi) peut échouer au déploiement. Ma stratégie inclut donc des déploiements progressifs, des plans de rollback rapides (le reprendre dans les bras) et surtout, une analyse post-mortem pour itérer et améliorer le processus à chaque tentative.

---

### Métrique #5 : Temps de réponse de maman

**SLA contractuel :** Immédiat  
**Temps de réponse réel :** Ça dépend de l'heure, du nombre de thés ingérés, et de la dette de sommeil.

*"Maman !"*

Mon temps de réponse conditionne tout : éviter le double réveil, désamorcer une dispute avant l'escalade, intercepter une chute, réconforter avant que les larmes ne deviennent inconsolables.

C'est une course contre la montre permanente. Et contrairement à un système informatique, je ne peux pas scaler horizontalement en ajoutant des instances. Je suis une ressource unique, non réplicable. Mais j'essaie chaque jour de scaler un peu plus verticalement.

Ce que cette métrique m'apprend en tant que PO : **la meilleure réactivité est celle qui devient de la proactivité**. Plus on maîtrise son produit et ses utilisateurs, plus on peut anticiper leurs besoins et livrer de la valeur avant même qu'ils n'aient à la demander.

---

### Ma stack technique : Prometheus, Thanos et sixième sens

Alors oui, je plaisante sur les métriques. Mais pas tant que ça.

Être mère, c'est développer une stack de monitoring surpuissante. Mon **Prometheus** interne est ce sixième sens qui se déclenche avant la crise. Mon **Thanos** est cette mémoire à long terme qui identifie les patterns pour la prochaine visite chez le pédiatre. Mon **Alertmanager** est ce système qui détecte les signaux faibles pour transformer une crise potentielle en simple incident.

En Product Management, c'est la même chose. Cette stack, c'est la capacité à croiser la **donnée quantitative** (les métriques d'usage) avec les **insights qualitatifs** (le feedback utilisateur) pour anticiper le prochain besoin avant même que l'utilisateur ne le formule.

---

### Du chaos familial à la stratégie produit

Au final, ces métriques sont la preuve qu'**être parent, c'est être le Product Owner d'un produit en constante évolution, avec des utilisateurs exigeants et sans documentation.**

Les compétences sont les mêmes :
- **Prioriser** sous une pression extrême
- **Décoder** le vrai besoin derrière la demande
- **Anticiper** les risques avant qu'ils ne deviennent des crises
- **Itérer** rapidement, car ce qui marchait hier est déjà obsolète
- Accepter que le **"done"** est toujours meilleur que le **"perfect"**

Mon thé est froid et mon dashboard est plein de warnings. Mais le système est stable et les utilisateurs sont satisfaits.

**Prêt à voir comment j'applique cette résilience et cette vision produit à un environnement digital ?**

J'affine actuellement ma stratégie pour mon prochain défi professionnel, avec une disponibilité à partir de janvier 2025.

**Découvrez mes études de cas et projets sur mon portfolio :** [Portfolio Product Owner - Cecilia DI MAULO](https://tar-hawk-fa8.notion.site/Portfolio-Product-Owner-Cecilia-DI-MAULO-27bd1b694d528029a1e9c2258667a3bf)

**Contactez-moi sur LinkedIn pour en discuter.**

---
*Cecilia DI MAULO - Mère de deux tornades humaines, ancienne entrepreneuse, future Product Owner. Je transforme le chaos familial en insights produit, et les nuits blanches en storytelling tech.*