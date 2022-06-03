Salut !

Aujourd'hui je traduit un tuto en français pour avoir un marqueur custom pour FiveM. => Tuto de base (https://forum.cfx.re/t/how-to-how-to-stream-custom-marker/873319)

Si vous voulez avoir ca comme pointeur custom, par exemple, suivez les etapes suivantes:
![This is an image](https://cdn.discordapp.com/attachments/586539476134658058/643837239922786304/unknown.png)

ÉTAPE 1 : Créez votre fichier PNG ou DDS
ÉTAPE 2 : Importez votre texture png vers ydt via OpenIV. Dans ce tutoriel, nous l'importons dans ma voiture complémentaire

Ouvrir le dossier de flux
![This is an image](https://forum.cfx.re/uploads/default/original/4X/c/d/7/cd7cb86a87945d41160dddf4b2f612176d8d5857.png)


Basculer le mode d'édition dans OpenIV
![This is an image](https://forum.cfx.re/uploads/default/original/4X/d/5/9/d599a72812ec4599db161bc8e3f8bc6b99aa82d1.png)

Open .ytd file and import your png.
![This is an image](https://forum.cfx.re/uploads/default/original/4X/1/4/0/1407f1890d9a7e78802fb357b34b8adfa4c76c60.png)

Enregistrez et diffusez votre fichier
ÉTAPE 3 : Dessinez-le

" DrawMarker(9, x, y, z, 0.0, 0.0, 0.0, 0.0, 90.0, 0.0, 3.0, 3.0, 3.0, 255, 255, 255, 255,false, false, 2, true, "your-ytd-name", "your-png-name", false) "

Exemple : j'ai importé pizza.png vers bmws.ytd, donc

" Citizen.CreateThread(function()
    while true do
        Citizen.Wait(0)
		if not HasStreamedTextureDictLoaded("bmws") then
				RequestStreamedTextureDict("bmws", true)
				while not HasStreamedTextureDictLoaded("bmws") do
					Wait(1)
				end
			else
			DrawMarker(9, -268.8787, -991.3987, 32.00805, 0.0, 0.0, 0.0, 0.0, 90.0, 0.0, 3.0, 3.0, 3.0, 255, 255, 255, 255,false, false, 2, true, "bmws", "pizza", false)
		end
    end
end) "

