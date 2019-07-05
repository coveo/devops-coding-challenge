# Coveo DevOps Challenge

## Le défi

Ton défi, si tu l’acceptes, est de développer un outil permettant d’analyser la taille des ressources de stockage S3 d’un compte Amazon Web Services (AWS).

Afin de tester ton outil, tu peux te créer un compte gratuit sur [Amazon](http://aws.amazon.com/fr/free/) (si tu n’en as pas déjà un).

## Spécifications

L’outil doit se présenter sous forme d’une commande shell qui permet d’obtenir des informations sur l’ensemble des ressources [S3](https://aws.amazon.com/documentation/s3/) d’un compte Amazon.

- Ton outil doit fonctionner sous Linux, OSX et Windows.
- Il doit être simple à installer et à utiliser.
- Idéalement, ton outil ne devrait pas nécessiter l'installation de libraries et / ou outils externes pour être fonctionnel.
- Le temps est de l'argent, nous ne pouvons pas attendre des heures pour obtenir des résultats. Ta solution devrait nous retourner des réponses en quelques secondes (ou en quelques minutes si tu tiens à tester notre patience :-).

### Temps alloué

Ceux qui ont réussi avec succès ce challenge et qui sont maintenant d'heureux membres de l'équipe Coveo y ont investi entre 4 et 10 heures.

Chez Coveo, on aime bien le principe KISS.

### L’outil doit permettre d’obtenir les informations suivantes:

Pour chaque bucket:
  - Nom
  - Date de création
  - Nombre de fichiers
  - Taille totale des fichiers
  - Date de mise-à-jour de l'objet le plus récent
  - Et le plus important de tous, **combien ça coûte...**

### Les options suivantes doivent être supportées:

- Affichage
  - Possibilité de sortir les résultats en octets, kilooctets, Mégaoctets, etc.
  - Pouvoir grouper les buckets par [régions](https://docs.aws.amazon.com/fr_fr/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)
  
- Filtres
  - Par nom de bucket
  - Par [type de stockage](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html) (Standard, IA, RR). Tu peux fournir des stats sur les objets dans le bucket (la quantité par type de stockage) et / ou ajouter un filtre sur le type de stockage (les informations sur le bucket réflètent alors seulement les objets qui ont le type sélectionné)

### Idées de fonctionnalités supplémentaires (optionnel)

Il serait bien de pouvoir:
- Filtrer les fichiers considérés dans le calcul à l’aide d’un préfixe, un glob et / ou une expression régulière (ex: s3://mybucket/Folder/SubFolder/log*).
- Filtrer ou organiser les résultats selon le [type d'encryption](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingEncryption.html)
- Obtenir des informations supplémentaires sur les buckets (Life cycle, cross-region replication, etc.)
- Tenir compte des [versions précédentes](https://docs.aws.amazon.com/AmazonS3/latest/UG/enable-bucket-versioning.html) des fichiers (nombre + taille).

Des statistiques pour afficher le pourcentage de l’espace total occupé par un bucket ou toute autre bonne idée que tu pourrais avoir sont également les bienvenues.

### Plus d'informations

- Tu es libre d’utiliser le langage et le [SDK](https://aws.amazon.com/tools/) de ton choix, mais souviens-toi que l'installation ne doit pas dépendre d'outils externes ;
- Nous allons tester le fruit de ton travail sur notre environnement qui, soit dit en passant, **contient des millions de fichiers**. La performance globale de la solution proposée est donc à considérer. La plupart des projets que nous recevons prendrait des semaines à rouler dans notre environnement. Peux-tu faire mieux? ;
- Ton code doit être disponible à partir de GitHub ou n'importe quel gestionnaire de code source publique. **Tu ne dois pas faire de "fork" de notre challenge ou de n'importe quel autre projet**.

## Conseils

- **Tente de créer ta solution comme si c'était du vrai code de production**. Montre nous comment tu crées du code propre et maintenable qui fait des choses incroyables. Construit quelque chose à laquelle nous serions heureux de contribuer. Ceci n'est pas un concours de programmation où les "hack" malpropres remportent la victoire.
- N'hésite pas à ajouter des fonctionnalités! Nous sommes curieux de voir ce à quoi tu peux penser. Nous nous attendrons à la même chose si tu travailles avec nous.
- La documentation et la maintenabilité est un plus.
- N'oublie pas les tests unitaires.
- On ne cherche pas à savoir si vous pouvez uniquement suivre des instructions (sinon tous les résultats seraient pareils). On veut savoir qu'est-ce que **tu** contribues lorsque tu travailles sur un projet. C'est quoi ton secret. Plus de fonctionnalités? Meilleure solution? Idées originales?
