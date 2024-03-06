Pour ajouter un item
######################
1. créer votre modèle (pas obligatoire)
2. créer votre texture
######################
~model~ = nom de l'item (dans presque tous les cas)
#####################
1. chercher dans assets/minecraft/models/item  quel item vous voulez changer (si vous ne le trouvez, demandez à Paul ou uploadez le modèle vanilla)
2. Ouvrir le fichier
3. ci-dessous le modèle de "test" :

{
  "parent": "minecraft:item/generated",
  "textures": {
    "layer0": "minecraft:item/totem_of_undying"
  },
  "overrides": [
    { "predicate": { "custom_model_data": 1 }, "model": "custom:item/test" }
  ]
}

est-ce qu'il y a "overrides" ?
a. si il n'y est pas
ajouter : 
,
  "overrides": [
    { "predicate": { "custom_model_data": 1 }, "model": "custom:item/~model~" }
  ]

b. si il y est déjà
ajouter: 
[la ligne précédente],
{ "predicate": { "custom_model_data": 1 }, "model": "custom:item/~model~" }

######################
si vous n'utilisez pas de modèle 3d
1. ajouter votre texture dans assets/custom/textures/item
2. dans assets/custom/models/item
dupliquer test.json et renommer en ~model~
3. dans "custom:item/test" changer test vers le nom de la texture
######################
si vous utilisez de modèle 3d
1. ajouter votre texture dans assets/custom/textures/item
2. ajouter votre modèle dans assets/custom/models/item
3. changer le chemin d'accès du modèle :
   "textures": {
		"0": "custom:item/~texture~",
		"particle": "custom:item/~texture~"
	},
