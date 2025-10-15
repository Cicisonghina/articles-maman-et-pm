# Du Chaos Engineering à la parentalité : Quand mes enfants deviennent mes Chaos Monkeys

## Ce matin, 10h23, aire de pansage

Tout était orchestré. Matinée catastrophique à la maison ? On évacue. Direction Vazy, ma jument. Trajet : tout le monde s'endort. Arrivée : la gérante surveille les dormeurs pendant que je vais au pré. Mon grand se réveille pile au bon moment. On récupère le matériel ensemble. Le petit se réveille en douceur. Je le pose au sol, loin des sabots. Tout le monde joue tranquillement.

**Et là.**

Victor le golden retriever, adorable bébé pataud de la gérante, débarque à toute vitesse pour nous dire bonjour.

Il essaie de jouer avec la brosse que mon grand tient. La brosse gicle dans l'eau stagnante. Mon fils perd l'équilibre, tombe. Le golden, enthousiaste, poursuit sur sa lancée pour lécher mon petit, le fait tomber à la renverse. Puis grimpe dans la voiture de prêt — tout plein de boue qu'il est — pour vérifier s'il n'y aurait pas un troisième enfant avec lequel jouer.

Tout le monde pleure. Ma jument est sur le qui-vive. Victor est très fier de lui.

Moi ? **Je documente mentalement.**

Blast radius : 4 composants affectés simultanément. Cascade complète. Temps de récupération : 15 minutes. Root cause : enthousiasme canin non contrôlé. Mitigation future : prévoir zone d'isolation chien.

Chez ManoMano, j'injectais volontairement des pannes dans les systèmes pour tester leur résilience. Maintenant, je n'ai plus besoin d'injecter quoi que ce soit. **Mes enfants s'en chargent.**

Et chaque incident me forge.

---

## Chaos Engineering 101 : Casser les choses pour devenir plus fort

Le Chaos Engineering, c'est l'art de volontairement introduire des pannes dans un système pour vérifier s'il peut les encaisser. Chez ManoMano, je coupais des serveurs en production, je simulais des latences réseau, je provoquais des crashes de base de données. Pas par sadisme. **Pour identifier les failles avant qu'elles ne deviennent critiques en pleine nuit.**

L'objectif : forger des systèmes antifragiles.

Faire deux enfants à moins de 2 ans d'écart, c'est exactement la même discipline. Pas par sadisme. **Pour identifier mes propres failles avant qu'elles ne deviennent des effondrements critiques en pleine nuit.**

Sauf que :
- Les pannes ne sont pas simulées, elles sont constantes
- Le système tourne 24/7 sans possibilité de maintenance planifiée
- Les composants (les enfants) évoluent en permanence, changeant les conditions de test
- **Et personne ne m'a donné le manuel d'utilisation**

La différence ? Chez ManoMano, je **choisissais** mes chaos experiments.

Ici, le chaos me choisit.

**Et j'apprends à le maîtriser.**

---

## Mes Chaos Monkeys personnels : Le fuzzing familial en action

Vous connaissez les Chaos Monkeys ? Des outils inventés par Netflix qui tuent volontairement des serveurs en production pour forcer les équipes à construire des systèmes résilients.

Chez moi, j'ai deux Chaos Monkeys. Sauf qu'ils ne tuent pas des serveurs, ils renversent du thé, corrompent le linge propre, et hackent l'interphone.

**Et contrairement aux vrais Chaos Monkeys, je ne peux pas les désactiver.**

**Scénario 1 : Injection d'erreur par bonne intention**

Mon grand adore "aider" à plier le linge. Il prend le dernier t-shirt de la pile propre et soigneusement pliée, le déplie, et le met dans l'armoire. Ou mieux : il vide la machine à laver propre directement dans le bac à linge sale.

C'est de l'**injection d'erreur pure**. Le système "linge propre → armoire" se retrouve corrompu. 

Mais voilà ce que j'apprends : **les meilleures intentions peuvent produire les pires corruptions de données.** En Product Management, c'est pareil. Une feature bien intentionnée mal implémentée peut détruire l'expérience utilisateur.

Je m'entraîne à détecter ces patterns. À prévoir. À mettre en place des circuit breakers.

**Scénario 2 : Corruption de données non intentionnelle**

Je change mon petit. J'entends un bruit métallique dans la cuisine. Je demande à mon grand ce qu'il fait. L'activité est trop passionnante pour qu'il réponde. Quand je sors de la salle de bain avec bébé dans les bras, je découvre qu'il a voulu sentir tous mes thés. Résultat : sachets partout par terre, mélange de parfums, chaos intégral.

**Le système "thé rangé par type" est devenu "thé en vrac sur le carrelage".**

Root cause analysis : curiosité + accès non restreint aux ressources critiques.

Leçon forgée : **Les permissions matters.** En tant que future Product Manager, je sais que la meilleure architecture ne sert à rien si les contrôles d'accès sont mal définis.

**Scénario 3 : Le fuzzing d'interface**

Mon grand a un talent inné avec l'électronique. Il appuie sur tous les boutons de l'interphone et arrive à le paramétrer en mode silencieux. Résultat : quand le livreur de couches passe, on ne l'entend pas. Il s'en va sans déposer le colis. Et évidemment, c'est le jour où les couches se terminent.

**C'est du fuzzing d'interface.** Il teste toutes les combinaisons de boutons possibles jusqu'à trouver une qui change le comportement du système.

Et moi ? **J'apprends à designer des interfaces qui résistent au fuzzing.**

Chaque incident me forme. Chaque panne m'affûte. Chaque chaos monkey domestique forge ma capacité à anticiper l'inattendu.

**[IMAGE : This is Fine meme - chien dans pièce en feu]**
*Moi, documentant mentalement les patterns de résilience pendant que mes Chaos Monkeys testent les limites du système.*

---

## Blast radius familial : Maîtriser la propagation des incidents

La cascade du golden retriever, c'est un cas d'école de blast radius incontrôlé.

**Incident initial** : Chien enthousiaste arrive trop vite.

**Propagation niveau 1** : Brosse gicle → enfant tombe → stress monte.

**Propagation niveau 2** : Chien continue → deuxième enfant tombe → pleurs généralisés.

**Propagation niveau 3** : Chien grimpe dans voiture interdite → boue partout → jument stressée.

**Impact final** : Système familial en mode dégradé. Tous les composants affectés simultanément. Temps de récupération : 15 minutes de câlins + nettoyage voiture.

C'est exactement ce qui se passe quand un microservice tombe et que toutes les dépendances en aval commencent à échouer. 

**La différence ? Maintenant, je sais anticiper ces cascades.**

Un autre exemple : l'interphone en mode silencieux.

**Incident initial** : Réglage accidentel par toddler curieux.

**Propagation niveau 1** : Livreur ne peut pas prévenir → pas de livraison.

**Propagation niveau 2** : Stock de couches atteint zéro.

**Propagation niveau 3** : Impossibilité de sortir acheter des couches (deux enfants + pas de couches = équation impossible).

**Impact final** : Escalade d'urgence. Appel mari. Détour par pharmacie en rentrant du travail.

Le blast radius d'un simple bouton d'interphone : toute l'organisation familiale.

**Ce que je forge :** La capacité à cartographier mentalement les dépendances critiques. À identifier les single points of failure. À prévoir les effets domino avant qu'ils ne se déclenchent.

En Product Management, c'est cette vision systémique qui différencie un PM junior d'un PM senior. **Je m'entraîne tous les jours.**

---

## Failure scenarios prévisibles : Anticiper pour mieux contrôler

Certaines pannes, je les vois venir. Parfois, je n'ai pas les ressources pour les prévenir. Mais **je les ai toujours documentées mentalement.**

**La couche en surcharge**

Chaque matin, je me lève fatiguée. Mon grand a des couches énormes. Je sais que si je ne le change pas immédiatement, ça va déborder. Mais parfois, il refuse catégoriquement. Il court partout. Et je dois choisir : me battre maintenant et risquer une crise de nerfs généralisée, ou accepter le risque de débordement.

C'est comme savoir qu'un serveur est à 95% de RAM et qu'il va crasher dans 10 minutes, mais que redémarrer maintenant couperait le service aux utilisateurs connectés.

**Je temporise. J'évalue. Je décide.**

Parfois, ça tient. Parfois, non. Mais ce n'est jamais un accident. **C'est un arbitrage conscient.**

**La routine matinale optimisée**

Pour éviter les failure scenarios du matin, j'ai mis en place une routine : lever le petit d'abord, le changer, l'installer avec un morceau de pain. Pendant qu'il est occupé, je vais chercher mon grand. Je le laisse sans pantalon (graceful degradation : si la couche déborde, pas besoin de changer le pantalon).

Ça marche. Sauf quand le petit ne veut plus de pain. Ou quand le grand refuse d'être changé. Ou quand les deux se réveillent en même temps.

**Les failure scenarios prévisibles ne sont pas toujours évitables.**

Mais je les ai cartographiés. Je connais mes plans B, C, et D. **Et c'est ça qui forge ma résilience.**

En Product Management, c'est pareil. Un bon PM anticipe les risques, prépare les mitigations, et sait prendre des décisions sous contrainte.

**Je m'entraîne à ça. Chaque matin.**

---

## Circuit breakers parentaux : Savoir couper avant l'effondrement

Un circuit breaker, c'est un mécanisme qui coupe automatiquement le flux quand le système est en surcharge. **Ça évite la dégradation complète.**

En famille, j'active manuellement ce circuit breaker. Et j'ai appris à reconnaître les signaux avant le point de non-retour.

**L'autre matin, tout le monde était énervé.** Le petit chouinait sans raison. Le grand était surexcité et n'écoutait rien. Le chien aboyait. Mon mari était avec son casque devant l'ordinateur pendant qu'une bombe atomique explosait dans la pièce d'à côté.

J'ai pensé appeler ma mère à la rescousse. Pas disponible.

**Alors j'ai activé le circuit breaker familial.**

J'ai attaché tout le monde à la poussette, descendu à la voiture, et décidé de partir voir Vazy. Changement de contexte radical. Nouveau système, nouvelles conditions.

**Et ça a fonctionné. Tout le monde s'est endormi dans les 5 minutes.**

Le circuit breaker, ce n'est pas de l'abandon. **C'est de la prévention d'incident critique.**

Parfois, c'est un appel à une amie : "Tu es dispo pour une balade au parc ?" Parfois, c'est une pizza commandée au lieu de cuisiner. Parfois, c'est juste s'asseoir sur le balcon avec le bébé qui pleure et attendre que l'énergie revienne.

**Ce que je forge :** La capacité à reconnaître les signaux faibles. À couper avant que le système ne parte en production outage. À préserver les ressources critiques.

En Product Management, savoir dire "stop" au bon moment peut sauver un produit. **Je maîtrise cette compétence.**

---

## Resilience patterns : Les stratégies qui tiennent le système debout

Après des mois d'incidents de production familiale, j'ai forgé mes propres resilience patterns. **Des automatismes qui maintiennent le système en vie.**

**Le pain occupationnel** : Installer le petit avec un morceau de pain pendant que je gère le grand. C'est comme un cache : ça occupe le CPU (l'enfant) pendant que je traite d'autres requêtes.

**Le mode sans pantalon** : Laisser le grand en couche le matin pour éviter de devoir changer le pantalon en cas de débordement. C'est de la graceful degradation : on accepte un mode dégradé (pas habillé) pour éviter un échec complet (pantalon sale + bataille pour en remettre un propre).

**Le double stock** : Toujours avoir un sac de rechange dans la poussette. Toujours avoir des couches de secours dans la voiture. C'est de la redondance. Si un composant échoue, le backup prend le relais.

Ces patterns ne sont pas glamours. **Mais ce sont eux qui font que le système familial continue de tourner même quand tout part en vrille.**

Et en Product Management ? **Les resilience patterns, c'est exactement ça.** Retry logic. Fallback mechanisms. Redundancy. Circuit breakers.

Je ne les ai pas appris dans un cours. **Je les ai forgés dans le feu de l'action.**

---

## Post-mortem sans blame : Apprendre de ce qui a dérapé

Les visites chez les grands-parents sont notre post-mortem récurrent.

On débriefe systématiquement après chaque visite. Pas pour chercher un coupable. **Pour comprendre ce qui a dérapé et comment l'éviter la prochaine fois.**

**Leçon 1** : Même si on demande à déjeuner vers midi, rien n'est jamais prêt avant 13h30. Solution : amener petit pot + lait pour faire manger les enfants dès les premiers signes de faim.

**Leçon 2** : Retarder le déjeuner retarde la sieste. Solution : s'éclipser avant la fin du repas si nécessaire. Besoins des enfants > politesse.

**Leçon 3** : Si tension sous-jacente chez les grands-parents, nos enfants (éponges émotionnelles) captent tout et déraillent. Solution : partir à la première occasion. Bien-être des enfants d'abord.

**C'est un post-mortem qui s'améliore. On itère. On ajuste. On apprend.**

Comme après un incident en prod : on identifie la root cause, on met en place des préventions, on améliore le monitoring. Pas de blame, juste des learnings.

**Et c'est exactement la culture que je veux instaurer en tant que Product Manager.**

Une équipe qui apprend de ses échecs sans chercher de coupables est une équipe qui devient antifragile. **Je forge cette mentalité tous les jours.**

---

## Antifragility parentale : Devenir plus fort grâce au chaos

L'antifragilité, c'est quand un système ne se contente pas de résister au stress, mais **devient plus fort à cause de lui.**

Mon grand essaie de cracker le code de la porte d'entrée. Il appuie sur tous les boutons. Résultat : il sonne chez les voisins. Et ça se transforme en apéro improvisé.

**Une panne qui devient une feature. Un incident qui crée du lien social.**

Ou encore : la cascade du golden retriever. Sur le moment, c'était le chaos total. Mais après ? On a ri. On a nettoyé ensemble. Mon grand a appris à être plus prudent avec les chiens excités. Et moi, j'ai compris que même mes sorties "refuge" pouvaient partir en vrille, et que c'était okay.

**Chaque micro-catastrophe familiale me rend un peu plus résiliente. Un peu plus capable de gérer l'imprévu. Un peu plus antifragile.**

Parce que le chaos n'affaiblit pas le système. **Il le renforce. À condition de ne pas le subir passivement, mais d'en tirer des apprentissages.**

En Product Management, c'est pareil. Les meilleurs produits ne sont pas ceux qui n'ont jamais eu de bugs. **Ce sont ceux qui ont appris de chaque incident pour devenir plus robustes.**

Je forge cette antifragilité. **Chaque jour. Chaque incident. Chaque chaos monkey domestique.**

---

## Ce que ça forge en moi comme Product Manager

Chez ManoMano, j'injectais du chaos pour tester la résilience des systèmes. Maintenant, je vis dans le chaos **pour forger ma propre résilience.**

Un bon produit, ce n'est pas un produit qui ne tombe jamais en panne. **C'est un produit qui sait encaisser les pannes et continuer de fonctionner.**

En tant que Product Manager, je maîtrise maintenant :
- **Identifier les points de rupture** avant qu'ils ne deviennent critiques
- **Mettre en place des circuit breakers** pour éviter les dégradations complètes
- **Concevoir des resilience patterns** qui maintiennent le service même en mode dégradé
- **Faire des post-mortems constructifs** sans chercher de coupables
- **Construire des systèmes antifragiles** qui s'améliorent sous la pression

Tous les jours, je gère un système distribué complexe avec des composants imprévisibles, des pannes constantes, et zéro possibilité de rollback.

**Si je peux maîtriser ça, je peux gérer n'importe quel produit.**

Ces compétences ne sont pas théoriques. **Je les ai forgées dans le feu.**

Et je suis prête à les déployer.

---

**Et vous, c'est quoi votre pire cascade d'incidents familiaux ?**

Partagez vos blast radius en commentaire. Parce que les meilleures leçons de résilience viennent toujours du terrain.

---

## À propos de moi

Je suis Cecilia, ex-Chaos Engineer chez ManoMano, ex-ingénieure Cloud chez Ubisoft, ex-entrepreneure en saddle-fitting équin, et **Product Manager en devenir**. Du Chaos Engineering volontaire au chaos parental involontaire, j'ai appris que la résilience se construit dans l'adversité.

**Je suis disponible immédiatement (ou dès qu'une place en crèche se libère) pour de nouvelles opportunités Product Manager.**

Si vous voulez voir comment je traduis ces compétences en méthodologie produit concrète, **[mon portfolio est par ici](https://tar-hawk-fa8.notion.site/Portfolio-Product-Owner-Cecilia-DI-MAULO-27bd1b694d528029a1e9c2258667a3bf)**.

Mon thé est froid, mais mes systèmes sont résilients. ☕💪