# Du Chaos Engineering à la parentalité : Quand mes enfants forgent ma résilience

## Chez ManoMano, j'injectais des pannes dans les systèmes pour tester leur résilience. Maintenant, je n'ai plus besoin d'injecter quoi que ce soit. Mes enfants s'en chargent.

### Ce matin, 10h23, aire de pansage

Tout était parfaitement orchestré. Après une matinée catastrophique, j'avais pris mon courage à deux mains et emmené mes deux garçons voir Vazy, ma jument. Le plan se déroulait sans accroc.

Et là. L'imprévu.

Victor le golden retriever arrive à toute vitesse. Il essaie de jouer avec la brosse, la fait gicler dans l'eau. Mon fils tombe. Le chien, enthousiaste, fait tomber mon petit à la renverse, puis grimpe dans la voiture, plein de boue.

Tout le monde pleure. Ma jument est sur le qui-vive. Victor est très fier de lui.

Moi ? Je ne sais pas si je dois rire ou m'arracher les cheveux. Mais une chose est sûre : bienvenue dans mon laboratoire de Chaos Engineering involontaire.

---

## Chaos Engineering 101 : Quand casser les choses devient une compétence

Le Chaos Engineering, c'est l'art d'introduire des pannes dans un système pour vérifier s'il peut les encaisser. L'objectif : identifier les points faibles avant qu'ils ne deviennent des incidents critiques en pleine nuit, comme je l'ai décrit dans mes [**Nuits InfernalOps**](https://medium.com/@cecidimaulo/nuits-infernalops-quand-mon-b%C3%A9b%C3%A9-devient-ladmin-sys-de-mes-cauchemars-2a4a3223ba42).

Une famille avec deux enfants, c'est pareil. Sauf que les pannes ne sont pas simulées, elles sont constantes, et le système tourne 24/7. C'est mon arène.

---

## Mes Chaos Monkeys personnels : Le Fuzzing familial

Chez Netflix, des "Chaos Monkeys" tuent des serveurs pour forcer les équipes à construire des systèmes résilients. Chez moi, j'ai deux Chaos Monkeys. Ils ne tuent pas des serveurs, ils renversent du thé, corrompent le linge propre, et hackent l'interphone.

**Scénario 1 : L'aide bien intentionnée**
Mon grand adore "aider". Il vide la machine à laver propre directement dans le bac à linge sale. C'est de l'injection d'erreur pure.

**Scénario 2 : Le renversement de thé**
Il veut sentir tous mes thés. Résultat : chaos intégral. Et moi, je dois nettoyer pendant que le bébé rampe vers le désastre, une démonstration parfaite de [**Resource Management parental**](https://medium.com/@cecidimaulo/ressource-management-parental-0e3eb066855d) sous contrainte.

**Scénario 3 : Le hacker en herbe**
Mon grand paramètre l'interphone en mode silencieux. Résultat : le livreur de couches passe, on ne l'entend pas. Il n'y a pas de rollback possible.

---

## Blast Radius familial : La cascade d'incidents

La cascade du golden retriever est un cas d'école de *blast radius* incontrôlé. Un incident initial qui se propage et met tout le système en mode dégradé.

C'est ce qui se passe quand un microservice tombe et que toutes les dépendances échouent. Sauf que là, je n'ai pas de dashboard Grafana, juste les [**cinq métriques de survie**](https://medium.com/@cecidimaulo/product-owner-de-deux-tornades-humaines-fe6629a2de49) que je traque en permanence dans ma tête.

---

## Circuit Breakers parentaux : Savoir quand couper le système

Un circuit breaker coupe le flux quand le système est en surcharge. L'autre matin, tout le monde était énervé. J'ai activé le circuit breaker familial : direction la jument. Changement de contexte radical. Ça a fonctionné.

Ce n'est pas de l'abandon. C'est une manœuvre stratégique pour prévenir l'incident critique.

---

## Resilience Patterns : Les stratégies qui tiennent le système debout

Certains patterns de résilience deviennent des automatismes qui maintiennent le système en fonctionnement même quand tout part en vrille.

* **Le pain occupationnel :** Un cache pour occuper le CPU (l'enfant) pendant que je traite d'autres requêtes.
* **Le mode sans pantalon :** De la *graceful degradation*. On accepte un mode dégradé pour éviter un échec complet.
* **Le double stock :** De la redondance. Si un composant échoue, le backup prend le relais.

Ces patterns ne sont pas glamour. Ce sont les fondations d'un système résilient.

---

## Post-mortem sans blâme : Transformer l'échec en apprentissage

Les visites chez les grands-parents sont notre post-mortem récurrent. On débriefe systématiquement. Pas pour chercher un coupable. Pour identifier la *root cause* et améliorer le monitoring. Pas de blâme, juste des *learnings*.

---

## Antifragilité parentale : Devenir plus fort GRÂCE au chaos

L'antifragilité, c'est quand un système devient plus fort à cause du stress. Chaque micro-catastrophe familiale me rend plus résiliente. Parce que le chaos n'affaiblit pas le système : il le forge.

---

## Ce que ça m'apprend en tant que Product Manager

Je ne subis plus le chaos pour apprendre à construire des systèmes résilients. **Je le maîtrise.**

Un bon produit n'est pas un produit qui ne tombe jamais en panne. C'est un produit qui sait encaisser les pannes et continuer de fonctionner. En tant que future Product Manager, je ne vais pas juste "gérer" des produits. Je vais construire des forteresses.

Parce que tous les jours, je pilote un système complexe avec des pannes constantes et zéro possibilité de rollback.

**Ce n'est pas une simulation. C'est la forge. Et c'est la preuve que je sais construire des produits qui ne s'effondrent pas sous la pression.**

---

*Et vous, c'est quoi votre pire cascade d'incidents familiaux ? Partagez vos blast radius en commentaire. Les meilleures leçons de résilience viennent toujours du terrain.*

---

**À propos de moi**

*Je suis Cecilia, ex-Chaos Engineer, ex-entrepreneure, et Product Manager. Du Chaos Engineering volontaire au chaos parental involontaire, j'ai appris que la résilience se construit dans l'adversité.*

**Je suis disponible dès maintenant pour de nouveaux défis en Product Management.**

*Si vous voulez voir comment je traduis ces compétences en méthodologie produit concrète, [**mon portfolio est par ici**](https://tar-hawk-fa8.notion.site/Portfolio-Product-Owner-Cecilia-DI-MAULO-27bd1b694d528029a1e9c2258667a3bf).*

*Mon thé est froid, mais mes systèmes sont résilients. 🍵⚔️*