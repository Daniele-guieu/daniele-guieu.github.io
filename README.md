# daniele-guieu.fr — Site vitrine

Site statique HTML/CSS/JS de **Danièle Guieu**, naturopathe animale à Cluses (Haute-Savoie).  
Hébergé sur **GitHub Pages** avec domaine custom OVH : `www.daniele-guieu.fr`

---

## Structure du projet

```
/
├── index.html            # Page d'accueil
├── soins.html            # Soins naturels proposés
├── tarifs.html           # Tarifs des consultations
├── parcours.html         # Parcours et formations
├── rendez-vous.html      # Prise de rendez-vous
├── contact.html          # Contact
├── mentions-legales.html # Mentions légales
├── confidentialite.html  # Politique de confidentialité
├── cgv.html              # Conditions générales de vente
├── sitemap.xml           # Sitemap pour Google
├── robots.txt            # Instructions aux crawlers
└── CNAME                 # Domaine custom GitHub Pages
```

---

## Hébergement

| Élément | Valeur |
|---|---|
| Hébergeur | GitHub Pages |
| Domaine | OVH — `daniele-guieu.fr` |
| HTTPS | Let's Encrypt (automatique via GitHub) |
| Branche de déploiement | `main` |

Le site est déployé automatiquement à chaque `git push` sur la branche `main`.  
Aucun build, aucune dépendance, aucun framework.

---

## DNS — Configuration OVH

Enregistrements à maintenir dans la zone DNS OVH :

| Type | Nom | Valeur |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | `nom-utilisateur.github.io.` |

---

## SEO

Chaque page contient :
- `<title>` et `<meta description>` uniques
- Balise `canonical` pointant vers l'URL réelle
- Open Graph et Twitter Card
- Données structurées JSON-LD (Schema.org — LocalBusiness)
- Géolocalisation (`geo.region`, `geo.position`)

Le sitemap est déclaré dans Google Search Console.  
URL : `https://www.daniele-guieu.fr/sitemap.xml`

---

## Modifier le site

Toutes les pages sont en HTML pur. Pour modifier une page :

1. Édite le fichier `.html` concerné
2. Si tu modifies du contenu (texte, tarifs, horaires) :
   - Mets à jour la `<meta description>` si nécessaire
   - Mets à jour le JSON-LD si les horaires ou tarifs changent
   - Mets à jour la date `<lastmod>` dans `sitemap.xml`
3. Commit et push sur `main` — le site est mis à jour en moins d'une minute

---

## Fichiers à ne jamais supprimer

- `CNAME` — suppression = perte du domaine custom
- `sitemap.xml` — suppression = déréférencement progressif
- `robots.txt` — suppression = comportement indéfini des crawlers

---

## Contact technique

Site réalisé et maintenu par : `[ton nom ou pseudo]`  
Toute question sur le code : `[ton email]`
