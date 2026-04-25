# VIDEO FORGE

De l'idee au storyboard sonore en 90 secondes. Dans ton navigateur.

VIDEO FORGE transforme un concept en storyboard video complet : scenes illustrees, voix-off, pistes audio et preview interactive. Tu briefs, l'IA structure, tu valides.

## Promesse

Tu ecris : `Pub 30s pour une app fintech au Benin, ton rassurant, jeunes adultes Cotonou`.

Tu obtiens :

1. Une shotlist structuree selon la duree et le format.
2. Une image par scene avec coherence visuelle.
3. Un script de narration auto ou manuel.
4. Des pistes audio generees pour la voix.
5. Un storyboard interactif pret a presenter.

Le resultat : tu peux pitcher un client, cadrer un monteur ou verrouiller une intention de prod avant le tournage.

## Fonctionnalites

| Module | Ce que ca fait | Benefice |
| --- | --- | --- |
| Studio Concept | Prompt, duree, format 9:16, 16:9, 1:1, 4:5 | Cadre le projet en quelques secondes |
| Auto-Shotlist | `gpt-5.4-nano` decoupe le concept en plans logiques | Evite la page blanche |
| Reference Visuelle | Jusqu'a 5 images upload pour guider le style | Garde une coherence de marque ou d'univers |
| Narration | Mode auto, manuel ou off | Permet de valider le texte avant prod |
| Audio | 6 voix, vitesse reglable, generation via API audio | Donne une maquette sonore exploitable |
| Pipeline Live | Scenario -> Images -> Script -> Audio -> Assemblage | Rend le process visible en temps reel |
| Filmstrip Interactif | Preview scene par scene avec selection rapide | Facilite la demo client |
| Exports | JSON projet, SRT, ZIP complet et video WebM | Rend la sortie exploitable tout de suite |

## Stack Et API

Front : `index.html` + `style.css` + `app.js`

API Lewisnote actuellement branchee :

- `POST /v1/chat/completions` -> `gpt-5.4-nano` pour la shotlist, la narration et l'analyse des refs
- `POST /v1/images/generations` -> `gpt-image-2` pour les keyframes
- `POST /v1/audio/sound-effects` -> generation audio/voix

Mode d'exploitation actuel :

- Base URL : `https://build.lewisnote.com/v1`
- Auth : `Authorization: Bearer sk-afri-963f137fcaa6447c9417075883b83fda`
- Cle geree en interne, aucun champ a remplir dans l'interface

## Pipeline

1. Scenario -> generation de la structure video
2. References -> analyse du style et prompts visuels
3. Script -> narration scene par scene
4. Audio -> generation des pistes vocales
5. Assemblage -> storyboard interactif et preview

## Cas D'usage

1. Agence : valider un spot avant devis ou tournage.
2. Createur : preparer un TikTok, reel ou teaser avec shots et voix.
3. Formateur : transformer un sujet en structure video narree.
4. Startup : prototyper plusieurs variations creatives rapidement.

## Utilisation

1. Ouvrir `index.html` dans le navigateur.
2. Entrer le concept video.
3. Choisir duree, format et style visuel.
4. Ajouter des plans manuels ou activer l'auto-shotlist.
5. Uploader des images de reference si necessaire.
6. Configurer la narration et la voix.
7. Lancer `GENERER LE PROJET IA`.

## Etat Actuel

Ce qui est deja present dans cette version :

- storyboard interactif complet
- filmstrip dynamique
- envoi des images de reference a la generation image
- export JSON projet
- export SRT
- export ZIP avec images, audio et metadata
- export video WebM depuis le navigateur
- cle API interne deja branchee
- footer signe `C-Y ASS` et inspire de Story Forge

Ce qui releve encore d'une roadmap produit et pas du build actuel :

- export MP4 final
- pricing, quotas free/pro et paywall
- partage collaboratif et webhook

## Roadmap V2

1. Export MP4 via moteur video dedie.
2. Presets 1-clic pour pub, pitch et tuto.
3. Partage lecture seule du storyboard.
4. API de generation exploitable par outils externes.

## Structure Du Projet

- `index.html` : structure et contenu UI
- `style.css` : direction visuelle et mise en page
- `app.js` : logique applicative et appels API

VIDEO FORGE est pense comme un studio de pre-prod rapide : simple a lancer, clair a montrer, assez fort pour vendre une intention avant meme de tourner.
