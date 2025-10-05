# La Stack Technique familiale : Quand choisir ses outils devient une compétence de Product Owner

## Ce matin, 8h47, contemplation stratégique

Un mois avant la naissance de mon deuxième fils, je me tiens devant la baignoire. Dedans : une pile de linge humide qui attend désespérément d'être étendu. Derrière moi : la machine à laver qui tourne déjà pour le prochain cycle. À mes pieds : le panier à linge qui déborde encore.

Mon mari me rejoint. On se regarde. On regarde la baignoire. On regarde le panier.

"On a un problème de throughput", je lâche.

Mon mari me regarde. "Tu viens vraiment de parler de notre linge comme d'un pipeline CI/CD ?"

"Oui. Et on est en production outage."

Deux semaines plus tard, on a un lave-linge séchant vendu habituellement à McDonald's. Le vendeur nous a assuré que si l'odeur de friture partait, les odeurs de digestion infantile ne feraient pas le poids.

Bienvenue dans ma stack technique familiale.

---

## Build vs Buy : le framework que personne ne vous apprend à l'école

En tant que future Product Owner, je vais passer mes journées à prendre ce type de décisions : est-ce qu'on développe en interne, ou est-ce qu'on achète une solution existante ?

En tant que mère de deux garçons, je prends déjà ce type de décisions. Plusieurs fois par jour. Avec des budgets serrés, des ressources limitées, et des conséquences immédiates.

La différence ? Personne ne me demande de faire un business case en trois slides. Mais le raisonnement est exactement le même.

**Buy**, c'est quand tu investis dans une solution existante pour résoudre un problème. **Build**, c'est quand tu construis ta propre solution parce qu'aucune n'existe ou ne répond exactement à ton besoin.

Et entre les deux ? C'est là que ça devient intéressant.

---

## Infrastructure critique : quand le lave-linge devient ton CI/CD pipeline

Notre premier fils était un champion du débordement. Je ne sais toujours pas comment il fait, mais ses couches défient les lois de la physique. Les bodys tournent vite. Très vite.

Nos options :
- **Acheter plus de bodys** : pas compatible avec nos valeurs (les enfants grandissent trop vite)
- **Améliorer le process lavage-séchage** : investissement initial plus élevé, mais ROI rapide

On a fait le calcul. Temps gagné par jour : ~2h (lavage + séchage combinés vs lavage + attente + étendage + attente). Sur un an : ~730h. Coût machine : ~1200€. 

ROI évident.

Mais surtout : **availability critique**. Avec deux enfants, je ne peux pas me permettre de downtime linge. C'est comme un système de production : si le pipeline tombe, tout s'arrête.

Notre lave-linge McDonald's, c'est mon infrastructure cloud. Capacité élevée, programmable à distance (app mobile), silencieux (déploiements nocturnes possibles), économe en énergie. Les specs sont solides. Et pour l'instant, elle tient vraiment bien le rythme.

**Ce que ça m'apprend comme PO :**

Investir dans l'infrastructure, ce n'est pas sexy. Ça ne se voit pas. Mais c'est ce qui permet de scaler. Un bon produit repose sur des fondations solides. Et parfois, la meilleure feature, c'est celle qui fait tourner le système sans qu'on y pense.

---

## Scaling hardware : l'évolution des poussettes comme capacity planning

**V1 - La poussette héritée** : Cadeau des cousins. Roues fines, bloquées dès qu'il y a de la boue. Problème : je passe 90% de mon temps en forêt. Solution inadaptée au use case.

**Décision Buy V2** : Poussette tout-terrain, grosses roues. Game changer. Coût : ~300€. Impact : accès complet à mes terrains de jeux préférés. ROI immédiat.

**V3 - Le problème du scaling** : Deuxième bébé arrive. Solution initiale : écharpe de portage. Bébé né à 5kg, courbe exponentielle. Mon dos : en compote. Hypothèse : "Mon grand va bientôt m'écouter et marcher à côté de moi."

Spoiler : non.

Résultat : impossibilité de sortir avec les deux. Je reste enfermée. Inacceptable pour quelqu'un qui vit dehors.

**Décision Buy V3** : Poussette double d'occasion. Timing : **6 mois trop tard**. Pourquoi ? Parce que j'ai sous-estimé le problème. Parce que j'ai cru pouvoir "optimiser autrement". Parce que j'ai oublié la règle de base du capacity planning : anticiper la charge future, pas juste gérer la charge actuelle.

**Ce que ça m'apprend comme PO :**

Technical debt, c'est aussi ça. C'est comme jouer des oiseaux sans regarder leurs synergies dans Wingspan : tu poses des cartes maintenant, mais ton moteur ne s'enclenche jamais vraiment. Reporter un investissement nécessaire parce qu'on croit qu'on va s'en sortir autrement. Résultat : 6 mois de douleurs de dos, de sorties ratées, de frustration. Le coût réel du "j'attendrai encore un peu" est toujours plus élevé qu'on le pense.

Anticiper les besoins futurs, ce n'est pas du luxe. C'est du pragmatisme.

---

## Mentalité "Build" : quand aucune solution n'existe sur le marché

Pendant mon aventure entrepreneuriale en saddle-fitting, j'ai côtoyé des professionnels dont les besoins n'ont jamais été adressés par la tech. Des gens qui travaillent avec des outils analogiques parce que personne n'a pensé à eux.

Trois idées de produits qui me trottent dans la tête :

**Produit 1 - App mesures cheval :**
On prend les mesures du cheval avec une ligne articulée. On reporte sur papier. On cherche quelle arcade de selle correspond. On teste. Processus long, imprécis, frustrant.

Mon idée : app mobile qui analyse une photo de la ligne articulée et suggère les arcades compatibles par marque. Gain de temps massif. Réduction erreurs. Stockage données clients facilité.

**Produit 2 - Scan 3D évolution cheval :**
Les professionnels de santé équine veulent suivre l'évolution musculaire, détecter des gonflements, comparer dans le temps. Aujourd'hui : observation visuelle, palpation, photos approximatives.

Mon idée : scan 3D via smartphone, comparaison automatique, mise en évidence zones qui ont évolué. Complexité technique élevée, mais besoin réel.

**Produit 3 - Carhorsel :**
Le vrai pain point des saddle-fitters ? La prise de rendez-vous et l'organisation des tournées. Optimiser les trajets, gérer les disponibilités, éviter les trous dans l'agenda.

Solution construite : plateforme de mise en relation + optimisation logistique. Parce qu'aucun outil existant ne résolvait ce problème spécifique.

**Ce que ça m'apprend comme PO :**

La meilleure opportunité produit, c'est celle que personne n'a encore adressée. Mais identifier un problème ne suffit pas. Il faut valider que le besoin est réel, que les utilisateurs sont prêts à payer (en argent ou en temps), et que tu as les ressources pour construire.

Build, c'est un engagement long terme. Contrairement à Buy, tu ne peux pas juste changer de fournisseur si ça ne marche pas.

---

## Buy vs Build : le framework de décision

Quand acheter une solution existante ?
- Le problème est commun (beaucoup de gens ont le même besoin)
- Des solutions éprouvées existent déjà
- Le coût d'acquisition est inférieur au coût de développement
- Ce n'est pas ton cœur de métier

Quand construire ta propre solution ?
- Le besoin est unique ou très spécifique
- Aucune solution existante ne répond vraiment au problème
- C'est un avantage compétitif potentiel
- Tu as les ressources et la passion pour le faire

**Exemple familial :**
- Poussettes : **Buy**. Problème commun, marché mature, solutions éprouvées.
- Carhorsel : **Build**. Besoin spécifique, marché de niche, opportunité différenciante.

La vraie compétence, ce n'est pas de savoir coder ou bricoler. C'est de savoir **quand** il vaut mieux acheter et **quand** il vaut mieux construire.

---

## Maintenance & Total Cost of Ownership

Acheter une solution, ce n'est jamais "acheter et oublier".

Mon lave-linge nécessite de l'entretien. Ma poussette double a des pneus à vérifier. Mes outils numériques ont des abonnements.

Construire, c'est encore pire. Carhorsel, c'est du code à maintenir, des bugs à corriger, des features à ajouter, des utilisateurs à supporter.

**Total Cost of Ownership**, c'est ça : le coût initial + tous les coûts récurrents sur la durée de vie du produit.

Un lave-linge à 1200€ qui tombe en panne tous les 6 mois coûte finalement plus cher qu'un modèle à 1800€ ultra-fiable.

Un produit gratuit avec 10h de configuration et 2h de maintenance par mois coûte plus cher qu'un produit payant clé en main.

**Ce que ça m'apprend comme PO :**

Quand tu évalues une solution (Buy ou Build), ne regarde jamais juste le coût d'acquisition. Regarde le coût total sur 3 ans. Combien de temps de maintenance ? Quelle évolutivité ? Quel risque d'obsolescence ?

Les décisions les moins chères à court terme sont souvent les plus coûteuses à long terme.

---

## Ce que ma stack technique familiale m'apprend

Chaque jour, je prends des décisions d'investissement sous contrainte. Budget limité. Temps limité. Énergie limitée.

Je dois choisir : est-ce que j'achète cette solution ou est-ce que je la construis moi-même ? Est-ce que j'investis maintenant ou plus tard ? Est-ce que je privilégie la rapidité ou la qualité ?

Ces décisions, je ne les prends pas dans un PowerPoint. Je les prends dans le chaos d'un appartement avec deux enfants qui hurlent et un chien qui aboie.

Et paradoxalement, c'est exactement ce qui me prépare à devenir Product Owner.

Parce que gérer un produit, ce n'est jamais dans des conditions idéales. C'est sous pression. Avec des ressources limitées. En essayant de maximiser l'impact tout en minimisant le coût.

Ma stack technique familiale, c'est mon terrain d'entraînement. Chaque lave-linge acheté, chaque poussette testée, chaque produit imaginé, c'est une décision produit en miniature.

Et maintenant, je sais que je peux prendre ces décisions. Parce que je les prends déjà. Tous les jours.

---

**Et vous, quel investissement matériel vous a fait gagner le plus de temps au quotidien ?**

Partagez vos game changers en commentaire. Parce que les meilleures stack techniques, elles viennent souvent des expériences terrain.

---

## À propos de moi

Je suis Cecilia, ex-Chaos Engineer chez ManoMano, ex-ingénieure Cloud chez Ubisoft, ex-entrepreneure en saddle-fitting équin, et future Product Owner. De l'infrastructure cloud aux décisions d'investissement familial, j'ai appris que tout est question de ROI, de priorités, et de savoir quand acheter vs quand construire.

**Je serai disponible pour de nouvelles opportunités Product Owner dès novembre/décembre 2025.**

Si vous voulez voir comment je traduis ces compétences en méthodologie produit concrète, **[mon portfolio est par ici](https://tar-hawk-fa8.notion.site/Portfolio-Product-Owner-Cecilia-DI-MAULO-27bd1b694d528029a1e9c2258667a3bf)**.

Mon thé est froid, mais mes décisions d'investissement sont calculées. ☕️💰