# Arthea

Arthea is a single-page art gallery website written in Turkish. One HTML file contains
15 sections that are shown one at a time with JavaScript:

- **Giriş**: home page
- **Sanat Eserleri** (Galeri I–V): 5 sections with 4 artworks each. Every artwork card has a
  "Hikayeyi Oku" button that opens the artwork's story in a modal.
- **Sanatçılar** (Portreler I–V): 5 sections with 3 artist portraits and short bios each. Clicking a
  portrait image opens an enlarged version in a modal.
- **Müzeler**: 4 sections about the Louvre, MoMA, the Uffizi and the Prado.

Navigation uses dropdown menus on desktop and a hamburger menu on small screens. Menu links
and modal buttons can be used with the keyboard (Tab / Enter / Escape).

## Tech

- HTML, CSS, and vanilla JavaScript in a single `index.html`
- [Tailwind CSS](https://tailwindcss.com/) loaded from the Play CDN (`cdn.tailwindcss.com`)
- Google Fonts (Cormorant Garamond, Raleway)

## Project structure

```
index.html   # markup, <style> and <script> for the whole site
resimler/    # all images (JPG)
```

## How to run

No build step is needed. Either open `index.html` in a browser, or serve the folder locally:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

You need an internet connection because Tailwind and the fonts load from CDNs.

## Known limitations

- **Single page, no URLs per section.** All 15 sections live in one HTML file and JavaScript
  switches between them. The address bar does not change, so you cannot bookmark or share a
  section, the browser Back button does not move between sections, and reloading returns to
  the home page. The site requires JavaScript.
- **Tailwind Play CDN.** The Tailwind Play CDN is meant for development and prototyping. The
  Tailwind docs do not recommend it for production. A production setup would compile Tailwind
  into a static CSS file.
- **External dependencies.** Tailwind and Google Fonts are loaded from third-party CDNs.
- **Image placeholders.** Copyrighted modern works are shown as a coloured text placeholder
  instead of an image: Dalí's *The Persistence of Memory*, Picasso's *Guernica*, Pollock's
  *No. 5, 1948*, Basquiat's *Untitled (1982)*, Banksy's *Girl with Balloon*, Yayoi Kusama's
  *Infinity Mirror Room* and Ai Weiwei's *Sunflower Seeds*. Vermeer's portrait card also uses
  a placeholder because no verified portrait of him exists.
- **Image sources.** Eight artwork images are reproductions of public-domain paintings whose
  original download source was not recorded: `ademin-yaratilisi`, `atina-okulu`,
  `gece-devriyesi`, `inci-kupeli-kiz`, `sis-denizi`, `yildizli-gece`, `opucuk`,
  `kompozisyon-vii`. All other images come from Wikimedia Commons (see Credits).
- **Portrait zoom.** Enlarging an artist portrait works with a mouse or touch only. The
  portrait images are not keyboard-focusable.

## Credits

The images below were downloaded from Wikimedia Commons and resized for the web. No other
changes were made. Each image keeps the licence shown on its Commons file page. The site
footer lists the same credits under "Görsel Kaynakları (Credits)".

| File | Commons source | Author | Licence |
|---|---|---|---|
| `resimler/mona-lisa.jpg` | [Mona Lisa, by Leonardo da Vinci, from C2RMF retouched.jpg](https://commons.wikimedia.org/wiki/File:Mona_Lisa,_by_Leonardo_da_Vinci,_from_C2RMF_retouched.jpg) | Leonardo da Vinci | Public domain |
| `resimler/venusun-dogusu.jpg` | [Sandro Botticelli - La nascita di Venere - Google Art Project - edited.jpg](https://commons.wikimedia.org/wiki/File:Sandro_Botticelli_-_La_nascita_di_Venere_-_Google_Art_Project_-_edited.jpg) | Sandro Botticelli | Public domain |
| `resimler/halka-yol-gosteren-ozgurluk.jpg` | [Eugène Delacroix - Le 28 Juillet. La Liberté guidant le peuple.jpg](https://commons.wikimedia.org/wiki/File:Eug%C3%A8ne_Delacroix_-_Le_28_Juillet._La_Libert%C3%A9_guidant_le_peuple.jpg) | Eugène Delacroix | Public domain |
| `resimler/niluferler.jpg` | [Claude Monet - Seerosen.jpg](https://commons.wikimedia.org/wiki/File:Claude_Monet_-_Seerosen.jpg) | Claude Monet | Public domain |
| `resimler/ciglik.jpg` | [Edvard Munch, 1893, The Scream, oil, tempera and pastel on cardboard, 91 x 73 cm, National Gallery of Norway.jpg](https://commons.wikimedia.org/wiki/File:Edvard_Munch,_1893,_The_Scream,_oil,_tempera_and_pastel_on_cardboard,_91_x_73_cm,_National_Gallery_of_Norway.jpg) | Edvard Munch | Public domain |
| `resimler/leonardo-da-vinci.jpg` | [Leonardo self.jpg](https://commons.wikimedia.org/wiki/File:Leonardo_self.jpg) | Leonardo da Vinci | Public domain |
| `resimler/michelangelo.jpg` | [Michelangelo Daniele da Volterra (dettaglio).jpg](https://commons.wikimedia.org/wiki/File:Michelangelo_Daniele_da_Volterra_(dettaglio).jpg) | Attributed to Daniele da Volterra | Public domain |
| `resimler/raphael.jpg` | [Raffaello Sanzio.jpg](https://commons.wikimedia.org/wiki/File:Raffaello_Sanzio.jpg) | Raphael | Public domain |
| `resimler/rembrandt.jpg` | [Rembrandt van Rijn - Self-Portrait - Google Art Project.jpg](https://commons.wikimedia.org/wiki/File:Rembrandt_van_Rijn_-_Self-Portrait_-_Google_Art_Project.jpg) | Rembrandt | Public domain |
| `resimler/caravaggio.jpg` | [Bild-Ottavio Leoni, Caravaggio.jpg](https://commons.wikimedia.org/wiki/File:Bild-Ottavio_Leoni,_Caravaggio.jpg) | Ottavio Leoni | Public domain |
| `resimler/claude-monet.jpg` | [Claude Monet 1899 Nadar crop.jpg](https://commons.wikimedia.org/wiki/File:Claude_Monet_1899_Nadar_crop.jpg) | Nadar | Public domain |
| `resimler/vincent-van-gogh.jpg` | [Vincent van Gogh - Self-Portrait - Google Art Project.jpg](https://commons.wikimedia.org/wiki/File:Vincent_van_Gogh_-_Self-Portrait_-_Google_Art_Project.jpg) | Vincent van Gogh | Public domain |
| `resimler/renoir.jpg` | [Renoir, Pierre-Auguste, by Dornac, BNF Gallica.jpg](https://commons.wikimedia.org/wiki/File:Renoir,_Pierre-Auguste,_by_Dornac,_BNF_Gallica.jpg) | Dornac | Public domain |
| `resimler/salvador-dali.jpg` | [Salvador Dalí by Carl Van Vechten, 1934.jpg](https://commons.wikimedia.org/wiki/File:Salvador_Dal%C3%AD_by_Carl_Van_Vechten,_1934.jpg) | Carl Van Vechten | Public domain |
| `resimler/pablo-picasso.jpg` | [Pablo picasso 1.jpg](https://commons.wikimedia.org/wiki/File:Pablo_picasso_1.jpg) | Vea y Lea magazine (Argentina) | Public domain |
| `resimler/frida-kahlo.jpg` | [Frida Kahlo, by Guillermo Kahlo.jpg](https://commons.wikimedia.org/wiki/File:Frida_Kahlo,_by_Guillermo_Kahlo.jpg) | Guillermo Kahlo | Public domain |
| `resimler/wassily-kandinsky.jpg` | [Vassily-Kandinsky.jpeg](https://commons.wikimedia.org/wiki/File:Vassily-Kandinsky.jpeg) | Anonymous | Public domain |
| `resimler/jackson-pollock.jpg` | [Jackson Pollock (cropped).jpg](https://commons.wikimedia.org/wiki/File:Jackson_Pollock_(cropped).jpg) | Unknown | Public domain |
| `resimler/andy-warhol.jpg` | [Andy Warhol by Jack Mitchell.jpg](https://commons.wikimedia.org/wiki/File:Andy_Warhol_by_Jack_Mitchell.jpg) | Jack Mitchell | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
| `resimler/louvre-cour-carree.jpg` | [Cour Carrée, Louvre Museum, 2 April 2009.jpg](https://commons.wikimedia.org/wiki/File:Cour_Carr%C3%A9e,_Louvre_Museum,_2_April_2009.jpg) | Benh LIEU SONG | [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) |
| `resimler/louvre-galerie-apollon.jpg` | [Galerie d'Apollon (Louvre).jpg](https://commons.wikimedia.org/wiki/File:Galerie_d%27Apollon_(Louvre).jpg) | Wilfredo Rafael Rodriguez Hernandez | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) |
| `resimler/moma-dis-cephe.jpg` | [Museum of Modern Art, New York City - panoramio.jpg](https://commons.wikimedia.org/wiki/File:Museum_of_Modern_Art,_New_York_City_-_panoramio.jpg) | Colin W | [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) |
| `resimler/moma-giris.jpg` | [Museum of Modern Art (MoMA) (51395759113).jpg](https://commons.wikimedia.org/wiki/File:Museum_of_Modern_Art_(MoMA)_(51395759113).jpg) | ajay_suresh | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) |
| `resimler/uffizi-avlu.jpg` | [Piazzale degli Uffizi perspective view, Florence, Italy, August 2025.jpg](https://commons.wikimedia.org/wiki/File:Piazzale_degli_Uffizi_perspective_view,_Florence,_Italy,_August_2025.jpg) | Verum3414 | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| `resimler/uffizi-koridor.jpg` | [Firenze - Galleria delle pitture e delle statue degli Uffizi - 2025-10-07 006.jpg](https://commons.wikimedia.org/wiki/File:Firenze_-_Galleria_delle_pitture_e_delle_statue_degli_Uffizi_-_2025-10-07_006.jpg) | C_messier | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
| `resimler/prado-cephe.jpg` | [Museo del Prado (Madrid) 20.jpg](https://commons.wikimedia.org/wiki/File:Museo_del_Prado_(Madrid)_20.jpg) | Fernando Bueno | [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/) |
| `resimler/prado-giris.jpg` | [Museo del Prado (Madrid) 06.jpg](https://commons.wikimedia.org/wiki/File:Museo_del_Prado_(Madrid)_06.jpg) | Abi Skipp | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) |
