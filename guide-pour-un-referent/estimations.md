---
description: >-
  Explications sur notre mode d'estimation. l'idée est de permettre à chacune
  des personnes de pouvoir se faire une idée approximative du délai de livraison
  d'un ticket.
---

# Estimations

### Taille d'un ticket

Nous travaillons en flux continue. Plus simple pour nous, cette approche nous semble aussi plus efficace. Nous poussons en production dès que c'est prêt.

Pour avoir une idée de ce qui nous attends, lorsque nous prenons connaissance d'un ticket \(ou lors de sa création\), nous faisons une estimation grossière sur le nombre de choses à réaliser et leur difficulté. Cela nous permet d'attribuer une taille de t-shirt à un ticket : S, M ou L.

Selon les situations, nous pouvons nous retrouver à rectifier cette taille de t-shirt durant la réalisation du ticket. L'idée étant d'avoir quelque chose qui reflète une réalité au moment du passage en production.

### Calcul du temps de réalisation d'un ticket

Notre tableau est assez basique : une colonne backlog, une colonne de ticket priorisé \(sélectionnés\), une colonne en cours et une colonne fini.

Le temps de réalisation est compté à partir du moment ou un ticket entre dans la colonne en cours, et prend fin au moment où le ticket est clos et placé dans la colonne finie.

Nous cherchons ici à déterminer la durée moyenne de réalisation d'un ticket S, M et L. Cela nous permettra ensuite de faire des estimations de délai de livraison sur des tickets encore dans le backlog.

Nous comptabilisons ensuite pour les tickets S en remontant sur les 10 ou 15 derniers, pour les M et les L nous les prenons tous en compte. Pour chaque ticket, nous calculons le nombre de jours \(jusqu'à la demi-journée\) entre l'entrée en développement jusqu'à la sortie. Nous essayons de considérer les jours fériées et les week-ends, ainsi que les nuits. Addition puis division par le nombre de tickets.

### Valeur à ce jour

Aujourd'hui, 11 mai 2021

| Poids | Temps |
| :--- | :--- |
| S | 1 journée |
| M | 7 jours |
| L | 14 jours |

{% file src="../.gitbook/assets/analyse-estimation-rdv-solidarites.ods" %}

