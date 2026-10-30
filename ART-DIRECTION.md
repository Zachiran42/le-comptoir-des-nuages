# Direction artistique et ressources

Une aventure chaleureuse pour adultes, inspirée du voyage et des cafés de quartier : noyer, cuivre, porcelaine, laiton, tissus pétrole, papier crème, lumière dorée. Typographie sérif pour les titres, interface lisible et animations discrètes. Les réglages système de réduction des animations sont respectés.

Les illustrations ont été générées avec **imagegen intégré**, sans appel API personnel, puis conservées dans le projet. Aucune image de jeu tiers utilisée. Les fichiers PNG finaux sont dans `docs/assets/`.

## Briefs des illustrations finales

**cafe.png** — Finished hand-painted 2D cafe interior background, landscape 3:2, no UI or lettering. Curved wooden airship hull, walnut floor, antique copper espresso machine and cup shelves on the left; panoramic windows showing luminous apricot clouds and floating islands; three separate teal armchairs and small tables on the right. Hanging plants, warm bulbs, brass pipes, painterly material textures. Empty seating, no people. Refined adult adventure-game style, readable objects at mobile scale.

**sky.png** — Finished landscape sky-archipelago illustration, no UI or words. Floating hillside port town on left with copper roofs, lighthouse, stone viaduct and tethered airships; floating garden islands and windmills on right; luminous open sky at center. Cream and peach clouds, gold light, teal shadows, fine gouache texture and detailed architecture.

**portraits.png** — Exactly six head-and-shoulders portraits in a rigid 3-column / 2-row atlas, identical deep petrol backdrop, no text, centered for circular crops. Refined warm hand-painted texture, consistent golden light. Characters: Alma, curly-haired aviator with orange scarf; Basile, elderly Black botanist with grey beard and round glasses; Yuna, East Asian mechanic with straight short black hair and teal overalls; Éléonore, elderly brown-skinned angular-faced cartographer with short straight silver hair, rectangular brass glasses and plum coat; Noé, brown-skinned young poet with mustard scarf; Gaspard, stocky moustached baker in cream. After user feedback, Éléonore was redrawn to differ clearly from Alma in age, facial structure, hairstyle, skin, glasses, expression and clothing. Other five portraits preserved.

**visitors.png** — Six full-body seated character cutouts matching the final portrait atlas, three columns and two rows. Each holding a small cup, entire body visible, no furniture or UI. Same identities, distinct silhouettes and outfits. Transparent alpha background. A second background-extraction pass removed the brown backdrop while preserving the six figures and atlas placement. Final alpha transparency was checked before integration. Cells are displayed with CSS background positions, without raster cropping or repainting.

## Éléonore et Alma

La première proposition rapprochait trop leurs traits. La version finale réserve à Alma les boucles sombres, les lunettes de pilote et l’écharpe orange. Éléonore a un visage plus long et marqué, une coupe argentée courte, des lunettes rectangulaires et un col prune brodé. Les sprites et les portraits utilisent cette même révision.

## Éléments animés

Vapeur de la machine, respiration légère des voyageurs, poussières lumineuses, balancement du décor, pluie à Brumeval, lumières ajoutées par l’aménagement, transition de voyage. Son synthétisé localement avec Web Audio : carillon et moteur doux ; désactivé initialement et suspendu lorsque le jeu passe à l’arrière-plan.

La scène du café et le panorama de l’archipel sont communs aux escales dans cette première version. Les variations de couleur, météo et commerce ne constituent pas six décors peints différents.
