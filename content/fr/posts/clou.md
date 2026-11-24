---
title: Comment configurer Cloudflare CDN (Guide 2027)
slug: clou
date: 2026-11-24
draft: false
---
Comment configurer Cloudflare CDN (Guide 2027)

Cloudflare CDN est une solution populaire permettant d’améliorer les performances d’un site web, de réduire les temps de chargement et d’ajouter une couche de sécurité supplémentaire. Grâce au réseau mondial de Cloudflare, les propriétaires de sites web peuvent mettre en cache les contenus statiques, protéger leurs serveurs et optimiser l’accès des visiteurs depuis différentes régions.

Que vous gériez un blog WordPress, un site web professionnel, une boutique en ligne ou un site hébergé sur un VPS, la configuration de Cloudflare CDN peut contribuer à améliorer les performances de votre site.

Dans ce guide, vous découvrirez comment configurer Cloudflare CDN en 2027, connecter votre nom de domaine, configurer les enregistrements DNS, activer le proxy, ajuster les paramètres de mise en cache et résoudre les problèmes les plus courants.

Si vous utilisez également des outils de paiement en ligne pour accéder à des services internationaux, vous pouvez découvrir CoinePay, une solution proposant des options de paiement en ligne.

👉 **CoinePay 官方入口：**  
[https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

Si vous utilisez également le réseau TRON pour effectuer des transferts d’USDT, vous pouvez découvrir le service de location d’énergie TRON proposé par TRXAPI, qui peut contribuer à réduire la consommation de ressources TRX pour certaines transactions compatibles.

👉 **TRXAPI 官方入口：**  
[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## **Qu’est-ce que Cloudflare CDN ?**

Cloudflare CDN est un réseau de diffusion de contenu qui permet de distribuer les ressources d’un site web à travers un réseau mondial de serveurs. Au lieu que chaque visiteur se connecte directement au serveur d’origine, Cloudflare peut fournir les contenus mis en cache depuis un emplacement plus proche du visiteur.

Cloudflare propose également d’autres services, notamment la gestion DNS, la protection contre les attaques DDoS, le filtrage du trafic, la prise en charge de SSL/TLS et différentes options de mise en cache.

Les principaux avantages de Cloudflare CDN sont les suivants :

- Amélioration de la vitesse de chargement du site web pour les visiteurs situés dans différentes régions.
- Réduction de la consommation de bande passante du serveur d’origine.
- Protection supplémentaire contre certains trafics malveillants et attaques DDoS.
- Prise en charge du chiffrement SSL/TLS.
- Gestion flexible des DNS.
- Fonctions de mise en cache et d’optimisation du site web.

Cloudflare propose des offres gratuites et payantes. De nombreuses fonctionnalités CDN de base peuvent être configurées avec l’offre Free.

## **Ce qu’il faut préparer avant de configurer Cloudflare CDN**

Avant de connecter votre site web à Cloudflare, assurez-vous de disposer des éléments suivants :

- Un nom de domaine enregistré.
- Un site web ou un serveur d’hébergement déjà opérationnel.
- Un accès au panneau de gestion de votre registraire de domaine.
- Un accès aux enregistrements DNS de votre domaine.
- L’adresse IP de votre serveur d’hébergement, si nécessaire.

Si votre domaine est déjà associé à un site web, vérifiez la configuration DNS existante avant d’effectuer des modifications. Des enregistrements DNS incorrects peuvent rendre votre site web, votre messagerie ou d’autres services indisponibles.

## **Étape 1 : Créer un compte Cloudflare**

Tout d’abord, rendez-vous sur le site officiel de Cloudflare :

[https://www.cloudflare.com/](https://www.cloudflare.com/)

Créez un compte à l’aide de votre adresse e-mail et d’un mot de passe.

Une fois inscrit, connectez-vous au tableau de bord Cloudflare. Vous pourrez ensuite ajouter votre domaine et configurer les paramètres DNS, de sécurité, de mise en cache et d’autres fonctionnalités.

## **Étape 2 : Ajouter votre domaine à Cloudflare**

Après vous être connecté :

1. Ouvrez le tableau de bord Cloudflare.
2. Sélectionnez l’option permettant d’ajouter ou d’intégrer un domaine.
3. Saisissez votre nom de domaine, par exemple [example.com](http://example.com).
4. Passez à l’étape suivante.
5. Sélectionnez une offre.

Pour la plupart des sites personnels, des blogs et des petits sites web, l’offre Free constitue un bon point de départ.

Cloudflare tentera de détecter automatiquement vos enregistrements DNS existants et de les importer dans son interface de gestion DNS.

## **Étape 3 : Vérifier les enregistrements DNS**

Avant d’activer Cloudflare, vérifiez attentivement vos enregistrements DNS.

Les principaux types d’enregistrements DNS sont les suivants :

- Enregistrement A : associe un domaine ou un sous-domaine à une adresse IPv4.
- Enregistrement AAAA : associe un domaine ou un sous-domaine à une adresse IPv6.
- Enregistrement CNAME : redirige un domaine ou un sous-domaine vers un autre nom d’hôte.
- Enregistrement MX : définit les serveurs de messagerie de votre domaine.
- Enregistrement TXT : utilisé pour la vérification, SPF, DKIM, DMARC et d’autres configurations.

Assurez-vous que les enregistrements principaux de votre site web sont corrects.

Par exemple :

Enregistrement A

Nom : @

Contenu : adresse IP de votre serveur

Enregistrement CNAME

Nom : www

Contenu : votre domaine principal ou le nom d’hôte fourni par votre hébergeur.

Les enregistrements exacts dépendent de la configuration de votre hébergement web.

Si vous utilisez une messagerie associée à votre domaine, veillez à conserver correctement les enregistrements MX, TXT et les autres enregistrements liés aux e-mails. Le proxy Cloudflare ne prend pas en charge le trafic de messagerie classique. Les enregistrements de messagerie doivent généralement rester en mode DNS Only.

## **Étape 4 : Activer le proxy Cloudflare**

L’une des étapes les plus importantes de la configuration de Cloudflare CDN consiste à activer son service proxy.

Dans la section de gestion DNS, vous trouverez une option permettant de définir l’état du proxy pour les enregistrements compatibles.

Proxied — Nuage orange

Lorsque le nuage orange est activé, le trafic associé aux enregistrements compatibles passe par Cloudflare. Cela permet d’utiliser les fonctions CDN, les services proxy et les fonctionnalités de sécurité correspondantes.

DNS Only — Nuage gris

Lorsque le nuage gris est activé, Cloudflare assure uniquement la résolution DNS. Le trafic ne passe pas par son réseau proxy.

Pour les principaux enregistrements de votre site web, comme l’enregistrement A du domaine et l’enregistrement A ou CNAME de www, activez Proxied si votre configuration le permet.

N’activez pas automatiquement le proxy pour tous les enregistrements DNS. Certains services, notamment la messagerie électronique et certains enregistrements de vérification ou services tiers, doivent rester en mode DNS Only.

## **Étape 5 : Modifier les serveurs de noms de votre domaine**

Après avoir vérifié vos enregistrements DNS, Cloudflare vous fournira deux serveurs de noms (nameservers).

Vous devez remplacer les serveurs de noms actuels de votre domaine par ceux attribués par Cloudflare.

La procédure est généralement la suivante :

1. Connectez-vous au compte de votre registraire de domaine.
2. Ouvrez la page de gestion de votre domaine.
3. Recherchez les paramètres des serveurs de noms.
4. Remplacez les serveurs de noms existants par les deux serveurs fournis par Cloudflare.
5. Enregistrez les modifications.

La propagation des changements de serveurs de noms peut prendre un certain temps.

Pendant cette période, la résolution DNS peut varier selon le réseau et le cache DNS. Évitez d’effectuer des modifications DNS inutiles pendant l’activation.

Si DNSSEC est activé pour votre domaine, vérifiez sa configuration avant de changer les serveurs de noms. Une configuration DNSSEC incorrecte peut empêcher la résolution de votre domaine.

## **Étape 6 : Configurer SSL/TLS**

SSL/TLS est essentiel pour sécuriser les connexions à votre site web et éviter les avertissements de sécurité dans les navigateurs.

Dans le tableau de bord Cloudflare :

1. Sélectionnez votre domaine.
2. Ouvrez la section SSL/TLS.
3. Vérifiez le mode de chiffrement.
4. Sélectionnez le mode correspondant à la configuration SSL de votre serveur d’origine.

Cloudflare propose généralement les modes SSL/TLS suivants :

Flexible

Le mode Flexible chiffre la connexion entre les visiteurs et Cloudflare, mais la connexion entre Cloudflare et votre serveur d’origine n’est pas chiffrée.

Ce mode peut être utilisé lorsque le serveur d’origine ne dispose pas de certificat SSL. Toutefois, il n’est généralement pas recommandé comme configuration à long terme.

Full

Le mode Full chiffre la connexion entre Cloudflare et votre serveur d’origine. Votre serveur doit prendre en charge HTTPS, mais le certificat n’a pas nécessairement besoin d’être délivré par une autorité de certification publique reconnue.

Full (Strict)

Le mode Full (Strict) chiffre la connexion et vérifie le certificat du serveur d’origine. Celui-ci doit disposer d’un certificat valide répondant aux exigences de Cloudflare.

Pour la plupart des sites web disposant déjà d’une configuration HTTPS correcte, le mode Full (Strict) est recommandé.

Avant de l’activer, assurez-vous que votre serveur d’origine possède un certificat SSL valide.

## **Étape 7 : Configurer le cache Cloudflare**

Le cache Cloudflare permet de stocker certaines ressources de votre site web sur son réseau. Ces ressources peuvent ainsi être distribuées aux visiteurs sans devoir être récupérées à chaque fois depuis le serveur d’origine.

Pour configurer le cache :

1. Ouvrez votre domaine dans le tableau de bord Cloudflare.
2. Accédez aux paramètres de mise en cache.
3. Consultez les options disponibles.
4. Ajustez le comportement du cache selon les besoins de votre site web.

Les ressources statiques pouvant généralement être mises en cache comprennent :

- Les images.
- Les fichiers CSS.
- Les fichiers JavaScript.
- Les polices de caractères.
- Les pages HTML statiques, lorsque cela est approprié.

Les contenus dynamiques, les pages de connexion, les paniers d’achat, les tableaux de bord et les contenus personnalisés nécessitent une configuration plus prudente.

Pour les sites WordPress, évitez de mettre en cache sans distinction les pages contenant des informations de connexion, des données personnelles, des informations de panier ou des fonctions d’administration.

Vous pouvez utiliser les Cache Rules de Cloudflare pour définir les URL à mettre en cache et contrôler leur comportement.

## **Étape 8 : Configurer les Cache Rules**

Les Cache Rules permettent de contrôler le comportement du cache pour des URL ou des conditions spécifiques.

Par exemple, vous pouvez :

- Mettre les fichiers statiques en cache pendant une période plus longue.
- Exclure les pages d’administration du cache.
- Éviter la mise en cache des pages de connexion.
- Appliquer différents paramètres de cache à certains sous-domaines.
- Contrôler la mise en cache de certains types de contenu.

Si vous utilisez WordPress, pensez à exclure les chemins suivants du cache lorsque cela est nécessaire :

- /wp-admin/
- /wp-login.php

Selon la configuration de votre site, vous devrez peut-être également exclure les pages dynamiques, les pages de paiement ou les contenus personnalisés.

Testez toujours votre site web après avoir modifié les Cache Rules.

## **Étape 9 : Vider le cache Cloudflare**

Lorsque vous mettez à jour votre site web, mais que les visiteurs continuent de voir l’ancien contenu, le problème peut provenir du cache.

Vous pouvez vider le cache depuis Cloudflare.

1. Ouvrez le tableau de bord Cloudflare.
2. Sélectionnez votre domaine.
3. Accédez à la section de mise en cache.
4. Recherchez l’option de purge du cache.
5. Choisissez la méthode de nettoyage appropriée.

Cloudflare propose plusieurs options pour supprimer les contenus mis en cache. Selon vos besoins, vous pouvez vider le cache de certaines URL ou supprimer un ensemble plus large de contenus.

Pour les mises à jour courantes d’un site web, il est généralement préférable de vider uniquement le cache des URL concernées plutôt que de supprimer l’intégralité du cache.

## **Étape 10 : Tester Cloudflare CDN**

Après avoir configuré Cloudflare, vérifiez que votre site web fonctionne correctement.

Contrôlez les éléments suivants :

- Votre site web s’ouvre normalement.
- HTTPS fonctionne sans avertissement du navigateur.
- Les enregistrements DNS sont correctement résolus.
- Les versions avec www et sans www fonctionnent comme prévu.
- Les services de messagerie continuent de fonctionner.
- Les ressources statiques sont mises en cache lorsque cela est nécessaire.

Vous pouvez également examiner les en-têtes HTTP des réponses.

Par exemple, l’en-tête suivant peut apparaître :

cf-cache-status

Les valeurs les plus courantes sont :

- HIT : la ressource demandée a été fournie depuis le cache.
- MISS : la ressource n’était pas présente dans le cache et a été récupérée depuis le serveur d’origine.
- BYPASS : le cache a été contourné.
- DYNAMIC : la ressource n’est pas considérée comme éligible à la mise en cache classique.
- EXPIRED : la ressource mise en cache a expiré.

Toutes les requêtes ne doivent pas nécessairement renvoyer HIT. Les pages dynamiques et les ressources non mises en cache peuvent légitimement renvoyer d’autres statuts.

Vous pouvez également utiliser des outils de test de performances comme PageSpeed Insights, GTmetrix ou WebPageTest pour évaluer la vitesse de chargement et les performances de votre site web.

## **Problèmes courants avec Cloudflare CDN**

### **Erreur Cloudflare 521**

L’erreur 521 indique généralement que Cloudflare ne parvient pas à établir une connexion avec le serveur d’origine parce que celui-ci refuse la connexion.

Solutions possibles :

- Vérifiez que votre serveur fonctionne.
- Assurez-vous que le pare-feu autorise le trafic provenant de Cloudflare.
- Vérifiez le service web de votre serveur d’origine.
- Examinez les règles du pare-feu et des logiciels de sécurité.

### **Erreur Cloudflare 522**

L’erreur 522 indique un délai d’attente dépassé lors de la connexion entre Cloudflare et le serveur d’origine.

Les causes possibles comprennent :

- Une surcharge du serveur d’origine.
- Des règles de pare-feu qui bloquent Cloudflare.
- Des problèmes de connectivité réseau.
- Des délais de réponse trop longs du serveur.

Vérifiez votre serveur d’hébergement et votre configuration réseau.

### **Erreurs de certificat SSL**

Des erreurs SSL peuvent survenir lorsque la configuration SSL/TLS de Cloudflare ne correspond pas à celle du certificat du serveur d’origine.

Vérifiez les points suivants :

- Le certificat SSL du serveur d’origine est valide.
- Le mode SSL/TLS sélectionné est approprié.
- HTTPS est correctement configuré sur le serveur d’origine.
- Aucune règle de redirection incompatible n’est présente.

### **Le contenu du site web ne se met pas à jour**

Si votre site web affiche toujours d’anciens contenus :

- Videz le cache Cloudflare correspondant.
- Effacez le cache de votre navigateur.
- Vérifiez les Cache Rules.
- Vérifiez si le plugin de mise en cache de votre site web est à l’origine du problème.

## **Cloudflare CDN est-il gratuit ?**

Cloudflare propose une offre Free qui comprend différentes fonctionnalités DNS, proxy, sécurité et mise en cache.

Pour de nombreux sites personnels, blogs et petits sites professionnels, l’offre Free est suffisante pour commencer.

Les offres payantes proposent des fonctionnalités et des services supplémentaires, selon l’offre et la disponibilité actuelle des produits.

Le choix de l’offre dépend du trafic de votre site web, de vos besoins en matière de sécurité et de performances, ainsi que de votre budget.

## **Liste de vérification pour la configuration de Cloudflare CDN**

Avant de terminer la configuration, vérifiez les points suivants :

- Votre domaine a été ajouté à Cloudflare.
- Les enregistrements DNS ont été vérifiés.
- Les principaux enregistrements du site web sont correctement configurés.
- Le proxy est activé pour les enregistrements web compatibles.
- Les serveurs de noms ont été mis à jour.
- SSL/TLS est correctement configuré.
- Les paramètres de mise en cache ont été vérifiés.
- Les pages dynamiques ne sont pas mises en cache de manière incorrecte.
- Votre site web se charge correctement en HTTPS.
- Les enregistrements DNS de votre messagerie sont toujours corrects.
- Les performances du site web ont été testées.

## **Conclusion**

Configurer Cloudflare CDN est une solution pratique pour améliorer la distribution des contenus de votre site web, gérer les DNS et ajouter une couche de protection supplémentaire.

La procédure de base consiste à ajouter votre domaine à Cloudflare, vérifier les enregistrements DNS, activer le proxy, mettre à jour les serveurs de noms, configurer SSL/TLS et ajuster les règles de mise en cache.

Même si Cloudflare propose de nombreuses fonctionnalités avancées, les débutants peuvent commencer par une configuration de base et optimiser progressivement leur site web selon leurs besoins.

En configurant correctement les DNS, le proxy, SSL/TLS et le cache, vous pouvez mettre en place une infrastructure web plus efficace et améliorer l’expérience des visiteurs dans différentes régions du monde.

Ressources officielles de Cloudflare :

Configuration d’un domaine Cloudflare :  
[https://developers.cloudflare.com/fundamentals/manage-domains/add-site/](https://developers.cloudflare.com/fundamentals/manage-domains/add-site/)

État du proxy Cloudflare :  
[https://developers.cloudflare.com/dns/proxy-status/](https://developers.cloudflare.com/dns/proxy-status/)

Cache Rules de Cloudflare :  
[https://developers.cloudflare.com/cache/how-to/cache-rules/](https://developers.cloudflare.com/cache/how-to/cache-rules/)

Purge du cache Cloudflare :  
[https://developers.cloudflare.com/cache/how-to/purge-cache/](https://developers.cloudflare.com/cache/how-to/purge-cache/)