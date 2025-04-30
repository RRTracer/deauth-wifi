# 🔒 Script Deauth Wi-Fi – Usage Pédagogique Uniquement

⚠️ **Ce script Bash a été conçu uniquement à des fins pédagogiques dans un environnement légalement contrôlé.**  
Il ne doit **en aucun cas** être utilisé à des fins malveillantes ou illégales.

## 🎓 Objectif

Ce dépôt contient un **script Bash automatisant une attaque de désauthentification Wi-Fi** à l'aide de la suite **Aircrack-ng**.  
Il a été développé pour **apprendre et démontrer** les vulnérabilités des réseaux sans fil (802.11), dans le but de renforcer la sécurité des infrastructures.

## ⚖️ Cadre légal

> ❗ **Attention : utiliser ce script en dehors d’un environnement de test avec autorisation explicite est illégal.**  
> Lancer une attaque de deauth sur un réseau tiers constitue une infraction aux lois en vigueur dans la majorité des pays (ex. : [article 323-1 du Code pénal en France](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006417233)).

Ce script doit **exclusivement** être utilisé :

- sur **votre propre réseau**, ou  
- dans un **environnement de laboratoire**, ou  
- avec **l’accord écrit du propriétaire du réseau**.

## 🧰 Prérequis

- Une interface Wi-Fi compatible **mode monitor**
- La suite **[Aircrack-ng](https://www.aircrack-ng.org/)**
- Droits **root**

## ⚙️ Utilisation

```bash
sudo ./deauth.sh <interface> <bssid> <channel>
```

**Exemple :**

```bash
sudo ./deauth.sh wlan0mon 00:11:22:33:44:55 6
```

Ce script activera le mode monitor (si pas déjà fait), se placera sur le bon canal, et enverra en boucle des paquets de désauthentification à l'aide de `aireplay-ng`.

## 📄 Licence

Ce projet est publié sous licence **[MIT](https://opensource.org/licenses/MIT)**.  
Tu es libre de l'utiliser, modifier ou redistribuer tant que tu respectes les termes de la licence et que tu m'identifie.
