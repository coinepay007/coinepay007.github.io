---
title: "Tutoriel Cloudflare : 10 fonctionnalités essentielles pour les débutants"
slug: cloud
date: 2026-11-03
draft: false
---
# Tutoriel Cloudflare : 10 fonctionnalités essentielles pour les débutants

## 1. Qu’est-ce que Cloudflare ?

Cloudflare est une plateforme de services Internet qui aide les propriétaires de sites web à améliorer la vitesse, la sécurité et la disponibilité de leurs sites.

Elle propose plusieurs outils importants :

- **Gestion DNS** : gérer les enregistrements DNS et diriger les visiteurs vers votre serveur.
- **CDN** : accélérer le chargement des sites grâce à un réseau mondial de serveurs.
- **SSL/TLS** : sécuriser les connexions entre les visiteurs et le site web.
- **Protection contre les attaques DDoS** : réduire les risques liés aux attaques par déni de service distribué.
- **WAF (Web Application Firewall)** : filtrer les requêtes malveillantes.
- **Mise en cache** : stocker temporairement les ressources du site pour accélérer leur chargement.
- **Analyses** : consulter les statistiques de trafic et de sécurité.
- **Workers** : exécuter du code directement sur le réseau Cloudflare.
- **Pages** : déployer des sites web statiques et des applications front-end.

Cloudflare propose des offres gratuites et payantes. Les débutants peuvent commencer avec l’offre gratuite pour découvrir les principales fonctionnalités.

## 2. Comment créer un compte Cloudflare et ajouter un site web ?

Avant d'utiliser les fonctionnalités de Cloudflare, vous devez créer un compte et ajouter votre nom de domaine.

### Étape 1 : Créer un compte Cloudflare

Accédez à la page officielle d'inscription :

[https://dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)

Saisissez votre adresse e-mail et créez un mot de passe pour ouvrir votre compte.

### Étape 2 : Ajouter votre site web

Après vous être connecté, sélectionnez l'option permettant d'ajouter un site ou un domaine.

Saisissez votre nom de domaine, par exemple :

`example.com`

Cloudflare analysera les enregistrements DNS existants et vous proposera une configuration.

### Étape 3 : Vérifier les enregistrements DNS

Vérifiez soigneusement les enregistrements DNS importés.

Les principaux types d'enregistrements sont :

- **A** : associe un nom de domaine à une adresse IPv4.
- **AAAA** : associe un nom de domaine à une adresse IPv6.
- **CNAME** : redirige un nom de domaine vers un autre nom de domaine.
- **MX** : définit les serveurs de messagerie.
- **TXT** : permet de stocker des informations textuelles, notamment pour certaines vérifications et configurations de messagerie.

Vérifiez particulièrement les enregistrements liés aux e-mails afin d'éviter toute interruption du service de messagerie.

### Étape 4 : Modifier les serveurs de noms

Cloudflare vous fournira deux serveurs de noms (nameservers).

Connectez-vous au site de votre registraire de domaine, puis remplacez les anciens serveurs de noms par ceux indiqués par Cloudflare.

La propagation peut prendre un certain temps. Une fois la configuration validée, Cloudflare commencera à gérer le trafic de votre domaine selon les paramètres définis.

## 3. Les 10 fonctionnalités essentielles de Cloudflare

### Fonctionnalité 1 : Gestion DNS

La gestion DNS est l'une des fonctions les plus importantes de Cloudflare.

Elle permet de gérer les enregistrements de votre domaine et de déterminer comment les visiteurs sont dirigés vers votre serveur.

Dans le tableau de bord Cloudflare, ouvrez la section **DNS** pour consulter et modifier les enregistrements.

Vous rencontrerez notamment deux modes de proxy :

- **Proxied (nuage orange)** : le trafic HTTP/HTTPS passe par le réseau Cloudflare. Cela permet d'utiliser les services de proxy, de CDN et de protection associés.
- **DNS Only (nuage gris)** : Cloudflare fournit uniquement la résolution DNS. Le trafic ne passe pas par son proxy.

Pour un site web classique, les enregistrements A et CNAME utilisés pour le site peuvent généralement être configurés en mode Proxied.

Attention : certains services, notamment les services de messagerie, nécessitent des configurations DNS spécifiques. Ne modifiez pas leurs paramètres sans vérifier leur fonctionnement.

### Fonctionnalité 2 : CDN et accélération du site web

Cloudflare dispose d'un réseau mondial de diffusion de contenu (CDN).

Lorsqu'un visiteur consulte votre site, certaines ressources peuvent être servies depuis un centre de données Cloudflare proche de sa position géographique.

Cela peut réduire la latence et améliorer la vitesse de chargement.

Les ressources qui bénéficient souvent de la mise en cache comprennent :

- Les images.
- Les fichiers CSS.
- Les fichiers JavaScript.
- Les polices de caractères.
- D'autres ressources statiques.

Pour activer le proxy Cloudflare, ouvrez la section DNS et vérifiez que les enregistrements web concernés affichent le nuage orange.

La mise en cache et les règles associées peuvent ensuite être configurées selon les besoins de votre site.

### Fonctionnalité 3 : SSL/TLS et chiffrement HTTPS

SSL/TLS permet de sécuriser les connexions entre les visiteurs et votre site web.

Un site correctement configuré en HTTPS protège les données échangées et inspire davantage confiance aux visiteurs.

Dans le tableau de bord Cloudflare, ouvrez :

**SSL/TLS → Overview**

Vous trouverez plusieurs modes de chiffrement :

- **Off** : aucun chiffrement entre Cloudflare et le visiteur.
- **Flexible** : connexion HTTPS entre le visiteur et Cloudflare, mais connexion HTTP entre Cloudflare et le serveur d'origine.
- **Full** : connexion chiffrée entre le visiteur, Cloudflare et le serveur d'origine, sans vérification stricte du certificat du serveur d'origine.
- **Full (strict)** : connexion chiffrée avec vérification du certificat du serveur d'origine.

Lorsque votre serveur d'origine dispose d'un certificat valide et correctement configuré, **Full (strict)** est généralement le mode recommandé.

Une mauvaise configuration SSL peut provoquer des erreurs telles que 525 ou 526. Vérifiez le certificat et la configuration du serveur d'origine si ces erreurs apparaissent.

### Fonctionnalité 4 : Mise en cache et Cache Rules

La mise en cache permet de stocker temporairement certaines ressources afin d'éviter de les récupérer à chaque visite sur le serveur d'origine.

Cela peut améliorer les performances et réduire la charge du serveur.

Dans Cloudflare, vous pouvez utiliser les paramètres de cache et les **Cache Rules** pour définir quelles ressources doivent être mises en cache et dans quelles conditions.

Si vous modifiez des fichiers ou des images mais que les visiteurs voient encore l'ancienne version, vous pouvez vider le cache.

Accédez à :

**Caching → Configuration → Purge Cache**

Vous pouvez ensuite choisir de vider le cache approprié.

Attention : évitez de mettre en cache sans précaution les pages de connexion, les paniers d'achat, les pages personnelles et les pages contenant des informations de paiement.

### Fonctionnalité 5 : Protection DDoS et sécurité du site

Les attaques DDoS cherchent à rendre un site indisponible en envoyant un volume important de requêtes.

Cloudflare fournit des mécanismes de protection destinés à détecter et à atténuer de nombreux types d'attaques DDoS.

Vous pouvez également consulter les événements de sécurité dans le tableau de bord pour comprendre les requêtes bloquées ou signalées.

Cette protection contribue à améliorer la disponibilité du site, mais elle ne garantit pas une protection absolue contre toutes les menaces.

Il reste important de sécuriser le serveur d'origine, les comptes administrateurs et les applications utilisées par votre site.

### Fonctionnalité 6 : WAF (Web Application Firewall)

Le WAF de Cloudflare permet de filtrer les requêtes HTTP susceptibles de présenter un risque pour votre application web.

Il peut aider à détecter ou à bloquer différents types de requêtes malveillantes, notamment celles associées à :

- L'injection SQL.
- Les attaques XSS (Cross-Site Scripting).
- Les requêtes suspectes.
- Certaines tentatives d'exploitation de vulnérabilités.

Cloudflare propose des règles gérées ainsi que des règles personnalisées.

Les **Managed Rules** permettent d'utiliser des ensembles de règles préparés, tandis que les **Custom Rules** vous donnent davantage de contrôle sur les conditions de filtrage.

Les paramètres doivent être adaptés à votre site. Des règles trop strictes peuvent bloquer des visiteurs légitimes ou perturber certaines fonctionnalités.

### Fonctionnalité 7 : Redirect Rules et redirections

Les Redirect Rules permettent de rediriger automatiquement les visiteurs d'une URL vers une autre.

Cette fonctionnalité est utile lorsque vous modifiez la structure de votre site, changez de domaine ou souhaitez uniformiser les URL.

Les deux types de redirection les plus courants sont :

- **301** : redirection permanente.
- **302** : redirection temporaire.

Par exemple, vous pouvez rediriger une ancienne page vers une nouvelle URL afin d'éviter les erreurs 404 et de faciliter la navigation.

Vérifiez toujours les conditions de redirection pour éviter les boucles ou les redirections incorrectes.

### Fonctionnalité 8 : Analytics et statistiques

Cloudflare Analytics permet de consulter différentes données relatives au trafic et à la sécurité de votre site.

Vous pouvez notamment examiner :

- Le nombre de requêtes.
- Le volume de données transférées.
- Les ressources servies depuis le cache.
- Les événements de sécurité.
- Certaines tendances du trafic.

Ces informations vous aident à comprendre comment votre site utilise le réseau Cloudflare et à identifier d'éventuels problèmes.

Attention : Cloudflare Analytics ne remplace pas nécessairement Google Analytics. Les deux services ne mesurent pas exactement les mêmes éléments et leurs statistiques peuvent être différentes.

### Fonctionnalité 9 : Cloudflare Workers

Cloudflare Workers permet d'exécuter du code sur le réseau Cloudflare, sans nécessairement gérer un serveur traditionnel.

Cette fonctionnalité peut être utilisée pour :

- Créer des API.
- Traiter des requêtes HTTP.
- Ajouter une logique personnalisée.
- Modifier des réponses.
- Développer des services distribués.

Les développeurs peuvent ainsi exécuter certaines fonctions à proximité des utilisateurs.

Les limites d'utilisation et les fonctionnalités disponibles dépendent de l'offre Cloudflare et de la configuration du service.

Documentation officielle :

[https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)

### Fonctionnalité 10 : Cloudflare Pages

Cloudflare Pages est une plateforme permettant de déployer des sites web statiques et des applications front-end.

Elle peut être connectée à un dépôt GitHub pour automatiser les déploiements.

Le processus général est le suivant :

1. Connectez votre compte GitHub.
2. Sélectionnez le dépôt du projet.
3. Configurez la commande de compilation (Build command), si nécessaire.
4. Indiquez le répertoire de sortie (Build output directory).
5. Lancez le déploiement.
6. Configurez un domaine personnalisé si nécessaire.

Cloudflare Pages est particulièrement adapté aux sites de documentation, aux blogs statiques et aux projets front-end.

Documentation officielle :

[https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

## 4. Paramètres Cloudflare recommandés pour les débutants

Si vous venez de connecter votre site à Cloudflare, il est préférable de commencer avec une configuration simple.

Voici les étapes recommandées :

1. Ajoutez votre domaine et vérifiez que les serveurs de noms sont correctement configurés.
2. Contrôlez les enregistrements DNS, notamment ceux liés au site et aux e-mails.
3. Configurez SSL/TLS en fonction du certificat installé sur votre serveur d'origine.
4. Activez le proxy Cloudflare pour les enregistrements web compatibles.
5. Configurez la mise en cache des ressources statiques.
6. Consultez les paramètres de sécurité et du WAF.
7. Surveillez les statistiques et les événements de sécurité.

Ne modifiez pas trop de paramètres simultanément. En cas de problème, il sera ainsi plus facile d'identifier la configuration responsable.

## 5. Problèmes Cloudflare fréquents et solutions

### Problème 1 : Le site ne fonctionne plus après la connexion à Cloudflare

Causes possibles :

- Les enregistrements DNS sont incorrects.
- Les serveurs de noms ne sont pas encore propagés.
- L'adresse IP du serveur d'origine est erronée.
- Le serveur d'origine refuse les connexions provenant de Cloudflare.

Solutions :

1. Vérifiez les enregistrements DNS.
2. Confirmez que l'adresse IP du serveur est correcte.
3. Vérifiez la configuration du pare-feu du serveur.
4. Contrôlez l'état de la connexion dans le tableau de bord Cloudflare.

### Problème 2 : Erreur 522

L'erreur 522 indique généralement que Cloudflare ne parvient pas à établir une connexion suffisamment rapidement avec le serveur d'origine.

Causes possibles :

- Le serveur est hors ligne ou surchargé.
- Le pare-feu bloque les connexions.
- Le serveur ne répond pas dans le délai attendu.
- La configuration réseau présente un problème.

Solutions :

- Vérifiez que le serveur d'origine fonctionne.
- Contrôlez les règles du pare-feu.
- Vérifiez que les adresses IP de Cloudflare ne sont pas bloquées.
- Contactez votre hébergeur si le problème persiste.

### Problème 3 : Erreur 525

L'erreur 525 indique un échec de la négociation SSL entre Cloudflare et le serveur d'origine.

Solutions :

- Vérifiez que le certificat SSL du serveur est correctement installé.
- Confirmez que le serveur prend en charge une configuration TLS compatible.
- Vérifiez les paramètres SSL/TLS de Cloudflare.
- Contactez votre hébergeur si nécessaire.

### Problème 4 : Les images ou les fichiers ne sont pas mis à jour

Ce problème est souvent lié au cache.

Solutions :

1. Ouvrez le tableau de bord Cloudflare.
2. Accédez à la section Caching.
3. Sélectionnez Purge Cache.
4. Videz le cache concerné.
5. Rechargez votre site et vérifiez le résultat.

### Problème 5 : L'offre gratuite est-elle suffisante ?

Pour un site personnel, un blog ou un petit site vitrine, l'offre gratuite de Cloudflare peut être suffisante pour commencer.

Elle donne accès à plusieurs fonctionnalités essentielles, notamment la gestion DNS, le proxy, le CDN et certaines protections de sécurité.

Les sites ayant des besoins plus avancés peuvent envisager une offre payante en fonction de leur trafic, de leurs exigences de sécurité et des fonctionnalités nécessaires.

## 6. Ressources officielles Cloudflare

Pour approfondir vos connaissances et consulter les instructions les plus récentes, utilisez les ressources officielles suivantes :

- Site officiel : [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Tableau de bord : [https://dash.cloudflare.com/](https://dash.cloudflare.com/)
- Documentation développeur : [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- Documentation DNS : [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- Documentation SSL/TLS : [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- Documentation WAF : [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Documentation Workers : [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Documentation Pages : [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

Il est conseillé de consulter la documentation officielle avant de modifier des paramètres importants de votre domaine ou de votre serveur.

## 7. Conclusion : Cloudflare est-il adapté aux débutants ?

Cloudflare propose de nombreux outils permettant d'améliorer les performances, la sécurité et la gestion d'un site web.

Les dix fonctionnalités présentées dans ce guide couvrent les principaux besoins des débutants :

1. Gestion DNS.
2. CDN et accélération du site.
3. SSL/TLS et HTTPS.
4. Mise en cache et Cache Rules.
5. Protection DDoS.
6. WAF.
7. Redirect Rules.
8. Analytics.
9. Workers.
10. Pages.

Il n'est pas nécessaire de maîtriser toutes ces fonctionnalités dès le début. Commencez par connecter votre domaine, vérifier les DNS, configurer HTTPS et activer les fonctions de base. Vous pourrez ensuite découvrir progressivement les outils plus avancés.

Pour les utilisateurs qui gèrent également des paiements en ligne ou des services numériques, il peut être utile de connaître des outils indépendants comme CoinePay et TRXAPI.

**CoinePay — plateforme de carte virtuelle**

Pour découvrir une solution de paiement par carte virtuelle destinée à certains paiements en ligne :

[https://www.coinepay.net/login?referrer=7PFFZMCH](https://www.coinepay.net/login?referrer=7PFFZMCH)

**TRXAPI — service de location d'énergie TRON**

Pour découvrir un service indépendant de location d'énergie TRON :

[https://www.trxapi.io/energy.html?lang=zh-TW](https://www.trxapi.io/energy.html?lang=zh-TW)

Code d'invitation TRXAPI : **57YQDGFU**

Remarque : CoinePay et TRXAPI sont des services tiers indépendants. Ils ne sont ni des produits Cloudflare ni des partenaires officiellement affiliés à Cloudflare.

## 8. Références

- Cloudflare : [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Documentation officielle : [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- DNS : [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- SSL/TLS : [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- WAF : [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Analytics : [https://developers.cloudflare.com/analytics/](https://developers.cloudflare.com/analytics/)
- Workers : [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Pages : [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

