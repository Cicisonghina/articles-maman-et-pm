# Du Chaos Engineering à la parentalité : Quand mes enfants injectent les pannes à ma place

## Ce matin, 10h23, aire de pansage

Tout était parfaitement orchestré. Après une matinée catastrophique à la maison, j'avais pris mon courage à deux mains et emmené mes deux garçons voir Vazy, ma jument. Trajet : tout le monde s'endort. Arrivée : la gérante est là pour surveiller les dormeurs pendant que je vais chercher ma jument au pré. Mon grand se réveille pile au bon moment. On va chercher le matériel ensemble. Le petit se réveille en douceur. Je le pose au sol, loin des sabots. Tout le monde joue tranquillement.

Et là.

Victor le golden retriever, adorable bébé pataud de la gérante, arrive à toute vitesse pour nous dire bonjour.

Il essaie de jouer avec la brosse que mon grand tient. La brosse gicle dans l'eau stagnante. Mon fils perd l'équilibre, tombe. Le golden, enthousiaste, poursuit sur sa lancée pour lécher mon petit, le fait tomber à la renverse. Puis grimpe dans la voiture de prêt — tout plein de boue qu'il est — pour vérifier s'il n'y aurait pas un troisième enfant avec lequel jouer.

Tout le monde pleure. Ma jument est sur le qui-vive. Victor est très fier de lui.

Moi ? Je ne sais pas si je dois rire ou m'arracher les cheveux.

Chez ManoMano, j'injectais volontairement des pannes dans les systèmes pour tester leur résilience. Maintenant, je n'ai plus besoin d'injecter quoi que ce soit. Mes enfants s'en chargent.

---

## Chaos Engineering 101 : Quand casser les choses devient une compétence

Le Chaos Engineering, c'est l'art de volontairement introduire des pannes dans un système pour vérifier s'il peut les encaisser. Chez ManoMano, je coupais des serveurs en production, je simulais des latences réseau, je provoquais des crashes de base de données. Pas par sadisme. Pour m'assurer que quand la vraie catastrophe arrive, le système tient bon.

L'objectif : identifier les points faibles avant qu'ils ne deviennent des incidents critiques en pleine nuit.

Une famille avec deux enfants en bas âge, c'est exactement la même chose. Sauf que :
- Les pannes ne sont pas simulées, elles sont constantes
- Le système tourne 24/7 sans possibilité de maintenance planifiée
- Les composants (les enfants) évoluent en permanence, changeant les conditions de test
- Et SURTOUT personne ne t'a donné le manuel d'utilisation

Bienvenue dans mon laboratoire de Chaos Engineering involontaire.

---

## Mes Chaos Monkeys personnels : Quand les enfants font du fuzzing familial

Vous connaissez la comptine ? *"3 little monkeys jumping on the bed, one fell off and bumped his head..."* En Chaos Engineering, on a des Chaos Monkeys aussi. Des outils inventés par Netflix qui tuent volontairement des serveurs en production pour forcer les équipes à construire des systèmes résilients.

Chez moi, j'ai deux Chaos Monkeys. Sauf qu'ils ne tuent pas des serveurs, ils renversent du thé, corrompent le linge propre, et hackent l'interphone. Et contrairement à la comptine, ils ne tombent jamais du lit. Eux, c'est tout le reste qui tombe.

**Scénario 1 : L'aide bien intentionnée**

Mon grand adore "aider" à plier le linge. Touchant, non ? Sauf qu'il prend le dernier t-shirt de la pile propre et soigneusement pliée, le déplie, et le met dans l'armoire. Ou mieux : il vide la machine à laver propre directement dans le bac à linge sale.

C'est de l'injection d'erreur pure. Le système "linge propre → armoire" se retrouve corrompu. Et le pire ? Ça part d'une bonne intention. Comme un développeur junior qui déploie un fix non testé en prod.

**Scénario 2 : Le renversement de thé**

Je change mon petit. J'entends un bruit de boîte métallique qui tombe dans la cuisine. Je demande à mon grand ce qu'il fait. L'activité est trop passionnante pour qu'il réponde. Quand je sors de la salle de bain avec bébé dans les bras, je découvre qu'il a voulu sentir tous mes thés. Résultat : sachets partout par terre, mélange de parfums, chaos intégral.

Corruption de données non intentionnelle. Le système "thé rangé par type" est devenu "thé en vrac sur le carrelage". Et moi, je dois nettoyer pendant que le bébé commence à ramper vers le désastre.

**Scénario 3 : Le hacker en herbe**

Mon grand a un talent inné avec l'électronique. Il appuie sur tous les boutons de l'interphone et arrive à le paramétrer en mode silencieux. Résultat : quand le livreur de couches passe, on ne l'entend pas. Il s'en va sans déposer le colis. Et évidemment, c'est le jour où les couches se terminent.

C'est du fuzzing d'interface. Il teste toutes les combinaisons de boutons possibles jusqu'à trouver une qui change le comportement du système. Sauf que contrairement au cheat code "rosebud" des Sims que j'utilisais petite pour avoir de l'argent infini, là, il n'y a pas de rollback possible.

---

## Blast radius familial : Quand une panne se propage en cascade

La cascade du golden retriever, c'est un cas d'école de blast radius incontrôlé.

**Incident initial** : Chien enthousiaste arrive trop vite.

**Propagation niveau 1** : Brosse gicle → enfant tombe → stress monte.

**Propagation niveau 2** : Chien continue → deuxième enfant tombe → pleurs généralisés.

**Propagation niveau 3** : Chien grimpe dans voiture interdite → boue partout → jument stressée.

**Impact final** : Système familial en mode dégradé. Tous les composants affectés simultanément. Temps de récupération : 15 minutes de câlins + nettoyage voiture.

C'est exactement ce qui se passe quand un microservice tombe et que toutes les dépendances en aval commencent à échouer. Sauf que là, je n'ai pas de dashboard Grafana pour monitorer les métriques de pleurs par minute.

Un autre exemple : l'interphone en mode silencieux.

**Incident initial** : Réglage accidentel par toddler curieux.

**Propagation niveau 1** : Livreur ne peut pas prévenir → pas de livraison.

**Propagation niveau 2** : Stock de couches atteint zéro.

**Propagation niveau 3** : Impossibilité de sortir acheter des couches (deux enfants + pas de couches = equation impossible).

**Impact final** : Escalade d'urgence. Appel mari. Détour par pharmacie en rentrant du travail.

Le blast radius d'un simple bouton d'interphone : toute l'organisation familiale.

---

## Failure scenarios prévisibles : Les pannes qu'on voit venir (mais qu'on ne peut pas toujours éviter)

Certaines pannes, on les connaît. On les voit arriver. Mais parfois, on n'a tout simplement pas les ressources pour les prévenir.

**La couche en surcharge**

Chaque matin, je me lève fatiguée. Mon grand a des couches énormes. Je sais que si je ne le change pas immédiatement, ça va déborder. Mais parfois, il refuse catégoriquement. Il court partout. Et je dois choisir : me battre maintenant et risquer une crise de nerfs généralisée, ou accepter le risque de débordement.

C'est comme savoir qu'un serveur est à 95% de RAM et qu'il va crasher dans 10 minutes, mais que redémarrer maintenant couperait le service aux utilisateurs connectés. Tu temporises. Tu espères. Et parfois, ça tient. Parfois, non.

**La routine matinale optimisée**

Pour éviter les failure scenarios du matin, j'ai mis en place une routine : lever le petit d'abord, le changer, l'installer avec un morceau de pain. Pendant qu'il est occupé, je vais chercher mon grand. Je le laisse sans pantalon (graceful degradation : si la couche déborde, pas besoin de changer le pantalon). 

Ça marche. Sauf quand le petit ne veut plus de pain. Ou quand le grand refuse d'être changé. Ou quand les deux se réveillent en même temps. Les failure scenarios prévisibles ne sont pas toujours évitables. Ils sont juste... prévisibles.

---

## Circuit breakers parentaux : Savoir quand couper le système

Un circuit breaker, c'est un mécanisme qui coupe automatiquement le flux quand le système est en surcharge. Ça évite la dégradation complète.

En famille, c'est pareil. Il y a des moments où tu dois activer le circuit breaker manuellement.

**L'autre matin, tout le monde était énervé.** Le petit chouinait sans raison. Le grand était surexcité et n'écoutait rien. Le chien aboyait. Mon mari était avec son casque devant l'ordinateur pendant qu'une bombe atomique explosait dans la pièce d'à côté.

J'ai pensé appeler ma mère à la rescousse. Pas disponible.

Alors j'ai activé le circuit breaker familial : j'ai attaché tout le monde à la poussette, descendu à la voiture, et décidé de partir voir Vazy. Changement de contexte radical. Nouveau système, nouvelles conditions. Et ça a fonctionné. Tout le monde s'est endormi dans les 5 minutes.

Le circuit breaker, c'est savoir dire : "Ce système est en train de partir en vrille. On coupe. On change d'environnement. On recommence."

Parfois, c'est un appel à une amie : "Tu es dispo pour une balade au parc ?" Parfois, c'est une pizza commandée au lieu de cuisiner. Parfois, c'est juste s'asseoir sur le balcon avec le bébé qui pleure et attendre que l'énergie revienne.

Le circuit breaker parental, ce n'est pas de l'abandon. C'est de la prévention d'incident critique.

---

## Resilience patterns : Les stratégies qui tiennent le système debout

Certains patterns de résilience deviennent des automatismes.

**Le pain occupationnel** : Installer le petit avec un morceau de pain pendant que je gère le grand. C'est comme un cache : ça occupe le CPU (l'enfant) pendant que je traite d'autres requêtes.

**Le mode sans pantalon** : Laisser le grand en couche le matin pour éviter de devoir changer le pantalon en cas de débordement. C'est de la graceful degradation : on accepte un mode dégradé (pas habillé) pour éviter un échec complet (pantalon sale + bataille pour en remettre un propre).

**Le double stock** : Toujours avoir un sac de rechange dans la poussette. Toujours avoir des couches de secours dans la voiture. C'est de la redondance. Si un composant échoue, le backup prend le relais.

Ces patterns ne sont pas glamour. Mais ce sont eux qui font que le système familial continue de tourner même quand tout part en vrille.

---

## Post-mortem sans blame : Apprendre de ce qui a dérapé

Les visites chez les grands-parents sont notre post-mortem récurrent.

On débriefe systématiquement après chaque visite. Pas pour chercher un coupable. Pour comprendre ce qui a dérapé et comment l'éviter la prochaine fois.

**Leçon 1** : Même si on demande à déjeuner vers midi, rien n'est jamais prêt avant 13h30. Solution : amener petit pot + lait pour faire manger les enfants dès les premiers signes de faim.

**Leçon 2** : Retarder le déjeuner retarde la sieste. Solution : s'éclipser avant la fin du repas si nécessaire. Besoins des enfants > politesse.

**Leçon 3** : Si tension sous-jacente chez les grands-parents, nos enfants (éponges émotionnelles) captent tout et déraillent. Solution : partir à la première occasion. Bien-être des enfants d'abord.

C'est un post-mortem qui n'est pas encore parfait. On itère. On ajuste. Mais on ne se reproche rien. On apprend.

Comme après un incident en prod : on identifie la root cause, on met en place des préventions, on améliore le monitoring. Pas de blame, juste des learnings.

---

## Antifragility parentale : Devenir plus fort grâce au chaos

L'antifragilité, c'est quand un système ne se contente pas de résister au stress, mais devient plus fort à cause de lui.

Mon grand essaie de cracker le code de la porte d'entrée. Il appuie sur tous les boutons. Résultat : il sonne chez les voisins. Et ça se transforme en apéro improvisé.

Une panne qui devient une feature. Un incident qui crée du lien social.

Ou encore : la cascade du golden retriever. Sur le moment, c'était le chaos total. Mais après ? On a ri. On a nettoyé ensemble. Mon grand a appris à être plus prudent avec les chiens excités. Et moi, j'ai compris que même mes sorties "refuge" pouvaient partir en vrille, et que c'était okay.

Chaque micro-catastrophe familiale me rend un peu plus résiliente. Un peu plus capable de gérer l'imprévu. Un peu plus antifragile.

Parce que le chaos n'affaiblit pas le système. Il le renforce. À condition de ne pas le subir passivement, mais d'en tirer des apprentissages.

---

## Ce que ça m'apprend comme Product Owner

Chez ManoMano, j'injectais du chaos pour tester la résilience des systèmes. Maintenant, je vis dans le chaos pour apprendre à construire des systèmes résilients.

Un bon produit, ce n'est pas un produit qui ne tombe jamais en panne. C'est un produit qui sait encaisser les pannes et continuer de fonctionner.

En tant que future Product Owner, je saurai :
- Identifier les points de rupture avant qu'ils ne deviennent critiques
- Mettre en place des circuit breakers pour éviter les dégradations complètes
- Concevoir des resilience patterns qui maintiennent le service même en mode dégradé
- Faire des post-mortems constructifs sans chercher de coupables
- Construire des systèmes antifragiles qui s'améliorent sous la pression

Parce que tous les jours, je gère un système distribué complexe avec des composants imprévisibles, des pannes constantes, et zéro possibilité de rollback.

Et si je peux gérer ça, je peux gérer n'importe quel produit.

---

**Et vous, c'est quoi votre pire cascade d'incidents familiaux ?**

Partagez vos blast radius en commentaire. Parce que les meilleures leçons de résilience viennent toujours du terrain.

---

## À propos de moi

Je suis Cecilia, ex-Chaos Engineer chez ManoMano, ex-ingénieure Cloud chez Ubisoft, ex-entrepreneure en saddle-fitting équin, et future Product Owner. Du Chaos Engineering volontaire au chaos parental involontaire, j'ai appris que la résilience se construit dans l'adversité.

**Je serai disponible pour de nouvelles opportunités Product Owner dès novembre/décembre 2025.**

Si vous voulez voir comment je traduis ces compétences en méthodologie produit concrète, **[mon portfolio est par ici](https://tar-hawk-fa8.notion.site/Portfolio-Product-Owner-Cecilia-DI-MAULO-27bd1b694d528029a1e9c2258667a3bf)**.

Mon thé est froid, mais mes systèmes sont résilients. ☕💪