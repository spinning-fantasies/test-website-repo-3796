---
title: Comment générer un QR Code ?
---
## Le contexte

Aujourd'hui on m'a demandé si c'était facile de "créer un QRCode qui oriente vers une page web". Ça m'a ramené 10 ans en arrière à l'époque où je travaillais avec [Baptiste Jamin](https://jam.in), [Erwan Maro](https://fr.linkedin.com/in/erwan-maro-2454321b9), [Nicolas Ha](https://nicolas-ha.com), et [Quentin de Quelen](https://fr.linkedin.com/in/quentin-de-quelen-4241a865) sur une solution d'authentification sans contact, **Scan2Auth**.

Je me suis largement éloigné du développement logiciel depuis ce temps-là, mais j'ai gardé l'habitude d'utiliser des produits [Libres et Open Source](https://fr.wikipedia.org/wiki/Free/Libre_Open_Source_Software) pour mes besoins divers.

## La solution

J'ai donc rapidement effectué une recherche sur [Microsoft GitHub](soldair/node-qrcode), la plateforme d'hébergement de projets Open Source la plus populaire du moment, pour trouver un outil qui me permettrait de générer facilement un QRCode. Je suis tombé sur [soldair/node-qrcode](https://github.com/soldair/node-qrcode), le projet ayant le plus de _stars_ sur GitHub et mis à jour il y a seulement quelques semaines, signe que le projet est toujours maintenu.

SOn utilisation est très simple. Pour l'installer, il suffit d'ouvrir son émulateur de terminal préféré et tapper :

```
npm install -g qrcode
```

À partir de maintenant, on peut utiliser ``qrcode`` depuis la ligne de commandes.

Pour générer un QRCode ``mon-qr-code.png`` de 500 pixels avec 1 pixel de bordure et qui redirige vers ``www.monsite.bzh``, il suffit d'écrire :

```
qrcode -o mon-qr-code.png -w 500 -q 1 "www.monsite.bzh"
```

Et voilà ! On peut maintenant générer des QRCodes pour permettre l'accès à un site web.