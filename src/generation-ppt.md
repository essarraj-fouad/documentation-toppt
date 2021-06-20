# Génération d'un fichier présentation Powerpoint

La commande `toppt` permet de générer un fichier Powerpoint à partie d'un fichier Markdown. par exemple la commande suivante permet générer le fichier "introduction-html.ppt" depuis le fichier "introduction-html.md"

``` powershell
toppt introduction-html.md
```

## Template PowerPoint

Par défaut le programme cherche un template nommé "template.potx" qui doit être existe dans le répertoire d'exécution de la commande.

### Fichier de configuration du template

Un fichier de configuration json pour indiquer une description des slides de la template, doit être présent dans le même répertoire du fichier "template.potx"

#### Exemple de fichier de configuration

Le fichier indique que la template contient deux slide. la première slide appelé : "Titre document" et la deuxième slide appelé "Titre contenu".

```json
{
  "Slides": [
    {   
      "Layout": "Titre document",
      "Order": 1,
      "SlideZones": [
        {
          "Name": "Titre",
          "ContentTypes": [
            "Title"
          ]
        },
        {
          "Name": "SousTitre",
          "ContentTypes": [
            "Text"
          ]
        }
      ]

    },
    {
      "Layout": "Titre contenu",
      "Order": 2,
      "SlideZones": [
        {
          "Name": "Titre",
          "ContentTypes": [
            "Title"
          ]
        },
        {
          "Name": "Contenu",
          "ContentTypes": [
            "Text", "Image"
          ]
        }
      ]
    }
  ]
}
```