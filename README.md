# Tendas para makers por Vigo.

Trátase de unha lista de tendas en Vigo e arredores que venden material interesante para un maker.

Se crees que falta algunha (que falta, creeme :P) manda unha "issue" ou un "pull request" ou unha mensaxe a algún dos que mantén á lista coa información que se debería engadir (polo de agora: nome, dirección, coordenadas GPS, páxina web e qué vende que sexa de interese).


Se queredes editar o ficheiro GeoJSON para facer un pull request, os pasos que eu faría serían os seguintes:
 1. Abrir http://geojson.io que é un editor GeoJSON en liña.
 2. Copiar o texto da lista de tendas en https://raw.githubusercontent.com/aindustriosa/tendas_para_makers_por_Vigo/master/lista_de_tendas.geojson
 3. Pegar o texto en geoson.io e engadir a nova tenda.
 4. Engadir a tenda. Básicamente, trátase de engadir unha nova entrada á lista de "features" no JSON. Máis sobre isto despois.
 ![alt text](https://raw.githubusercontent.com/aindustriosa/tendas_para_makers_por_Vigo/master/readme_images/geojson_example.png)

 5. Cando esteas contento co resultado, copia o contido do ficheiro, edita lista_de_tendas.geojson online usando a URL https://github.com/aindustriosa/tendas_para_makers_por_Vigo/edit/master/lista_de_tendas.geojson e pega o teu ficheiro.
 6. Preme ó botón "preview changes" para ver se o resultado é o que esperabas.
 7. Envía un pull request co resultado.
 ![alt text](https://github.com/aindustriosa/tendas_para_makers_por_Vigo/blob/master/readme_images/github_example_1.png)
 ![alt text](https://github.com/aindustriosa/tendas_para_makers_por_Vigo/blob/master/readme_images/github_example_2.png)

 Unha entrada da lista de "features", unha nova tenda, debería ter esta forma:
 
 ```
    {
      "type": "Feature",
      "properties": {
        "marker-color": "#ff0000",
        "marker-size": "medium",
        "marker-symbol": "shop",
        "name": "Iturmendi",
        "address": "Rúa do Progreso, 18, 36202 Vigo, Pontevedra",
        "web": "https://www.ferreteriaiturmendi.es/",
        "sells": "Cousas de ferretería"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [
          -8.723579049110413,
          42.23570859935509
        ]
      }
    }
 ´´´
 
 As cousas que deben ser distintas na túa entrada son:
  - name: que é o nome da tenda.
  - address: a dirección que entenden os humanos.
  - web: dirección da páxina web da tenda (se ten, se non non inclúas esta liña).
  - sells: qué é o que vende que sexa interesante para nos.
  
