# VIDEO FORGE

VIDEO FORGE est un studio web local pour transformer une idee video en storyboard IA complet avec images, narration et apercu audio.

## Fonctionnalites

- Scenario IA a partir d'un concept, d'une duree et d'un format.
- Plans manuels ou generation automatique des shots.
- Upload de 5 images de reference pour garder une coherence visuelle.
- Generation d'images via `POST /v1/images/generations`.
- Narration auto, manuelle ou desactivee.
- 6 voix disponibles avec controle de vitesse.
- Generation audio via `POST /v1/audio/sound-effects`.
- Pipeline visible en 5 etapes: scenario, images, script, audio, assemblage.
- Filmstrip interactif pour previsualiser les plans generes.

## API interne

L'application est deja configuree en interne.

- Base URL: `https://build.lewisnote.com/v1`
- Auth: `Authorization: Bearer sk-afri-963f137fcaa6447c9417075883b83fda`
- Aucune cle API a saisir dans l'interface.

## Structure

- `index.html` : structure de la page
- `style.css` : tout le style
- `app.js` : logique, appels API et interactions

## Utilisation

1. Ouvrir `index.html` dans le navigateur.
2. Renseigner le concept video.
3. Choisir duree, format et style.
4. Ajouter des plans manuels ou laisser l'IA les generer.
5. Ajouter des images de reference si besoin.
6. Choisir la narration et la voix.
7. Cliquer sur `GENERER LE PROJET IA`.

## Notes

- Cette version produit un storyboard interactif, pas un export MP4 final.
- Les images de reference sont envoyees a la generation d'image quand elles sont presentes.
- Le footer conserve la signature `C-Y ASS` et l'inspiration Story Forge.
