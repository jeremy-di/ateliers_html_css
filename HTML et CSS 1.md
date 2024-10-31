
# HTML

### 1. **Structure de base d'une page HTML**




```html
<!DOCTYPE html> 
<html lang="fr"> 
	<head> 
		<meta charset="UTF-8"> 
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title>Ma Première Page HTML</title> 
	</head> 
	<body> 
		<h1>Bienvenue sur mon site</h1> 
		<p>Ceci est un exemple simple de page web.</p> 
	</body> < 
/html>
```

### 2. **Les titres et les paragraphes**



```html
<h1>Titre Principal</h1>
<h2>Sous-titre</h2>
<p>Ceci est un paragraphe de texte. Vous pouvez en ajouter autant que vous voulez.</p>
<p>Ceci est un autre paragraphe pour plus d'exemples.</p>
```

### 3. **Liens hypertextes (ancre)**

target="_blank" permet d'ouvrir un lien dans un nouvel onglet 

```html
<p><a href="https://www.example.com" target="_blank">Lien vers un autre site</a></p>
```

### 4. **Images**


```html
<img src="https://www.example.com/image.jpg" alt="Description de l'image" width="300" height="200">
<!-- Pas la meilleure pratique pour changer une largeur et une hauteur -->
```

### 5. **Listes (ordonnées et non ordonnées)**

#### Liste non ordonnée


```html
<ul>
    <li>Élément de liste 1</li>
    <li>Élément de liste 2</li>
    <li>Élément de liste 3</li>
</ul>
```

#### Liste ordonnée


```html
<ol>
    <li>Premier élément</li>
    <li>Deuxième élément</li>
    <li>Troisième élément</li>
</ol>
```

### 6. **Tableaux**


```html
<table>
	<thead>
		<tr>
			<th>Nom</th>
			<th>Prénom</th>
			<th>Adresse</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Doe</td>
			<td>John</td>
			<td>2 rue des fleurs</td>
		</tr>
		<tr>
			<td>Doe</td>
			<td>Jane</td>
			<td>12 rue des ruelles</td>
		</tr>
	</tbody>
</table>
```

### 7. **Formulaire**


```html
<form action="/submit" method="post">
    <label for="name">Nom:</label>
    <input type="text" id="name" name="name"><br><br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br><br>
    <label for="message">Message:</label><br>
    <textarea id="message" name="message"></textarea><br><br>
    <input type="submit" value="Envoyer">
</form>
```

### 8. **Balises de mise en forme (gras, italique, souligné)**


```html
<p><strong>Texte en gras</strong></p>
<p><em>Texte en italique</em></p>
<p><u>Texte souligné</u></p>
```

### 9. **Commentaires en HTML**


```html
<!-- Ceci est un commentaire qui ne sera pas affiché sur la page -->
```


# CSS

### 1. **CSS intégré dans le HTML**

Tu peux inclure du CSS directement dans une page HTML en utilisant la balise `<style>` dans la section `<head>` mais cela est devenu une mauvaise pratique:


```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page avec CSS intégré</title>
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        h1 {
            color: #333;
            text-align: center;
        }
        p {
            font-size: 16px;
            color: #555;
            line-height: 1.5;
        }
    </style>
</head>
<body>
    <h1>Bienvenue sur ma page</h1>
    <p>Ceci est un exemple de page avec du CSS intégré directement dans le HTML.</p>
</body>
</html>
```

### 2. **CSS externe (fichier séparé)**

Dans cet exemple, le CSS est dans un fichier séparé appelé `style.css`. Voici comment lier un fichier CSS externe dans une page HTML :

#### HTML :


```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page avec CSS externe</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Bienvenue sur ma page</h1>
    <p>Ceci est un exemple de page avec du CSS dans un fichier séparé.</p>
</body>
</html>
```

#### Fichier CSS (`style.css`) :


```css
body {
    background-color: #e0e0e0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

h1 {
    color: #0066cc;
    text-align: center;
    font-size: 2.5em;
}

p {
    color: #333;
    font-size: 18px;
    line-height: 1.8;
}
```

### 3. **Sélecteurs CSS de base**

Les sélecteurs permettent de cibler des éléments HTML spécifiques pour leur appliquer un style.

#### Sélecteur d'élément


```css
h1 {
    color: blue;
    font-size: 2em;
}
```

#### Sélecteur de classe


```css
.intro { color: green; font-weight: bold; }
```

HTML associé :


```html
<p class="intro">Ceci est un paragraphe avec une classe.</p>
```

#### Sélecteur d'ID


```css
#main-header { background-color: #ffcc00; padding: 10px; text-align: center; }
```

HTML associé :

```html
<h1 id="main-header">Titre Principal</h1>
```

### 4. **Mise en page avec Flexbox**

Flexbox est une méthode de mise en page très utilisée en CSS.


```css
.container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100vh;
}

.box {
    width: 200px;
    height: 200px;
    background-color: #66ccff;
    text-align: center;
    line-height: 200px;
    color: white;
    font-size: 1.5em;
}
```

HTML associé :


```html
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
```

### 5. **Utilisation de couleurs, bordures, marges et padding**


```css
p {
    color: #333;
    background-color: #f9f9f9;
    border: 1px solid #ccc;
    padding: 20px;
    margin: 10px;
    font-size: 16px;
}
```

### 6. **Pseudo-classes pour les interactions**

Les pseudo-classes permettent de styliser les éléments en fonction de leur état (par exemple, au survol avec la souris).


```css
a {
    color: #0066cc;
    text-decoration: none;
}

a:hover {
    color: red;
    text-decoration: underline;
}
```

HTML associé :


```html
<p>Visitez notre site <a href="https://www.example.com">ici</a>.</p>
```

### 7. **Polices avec Google Fonts**

Tu peux inclure des polices personnalisées depuis Google Fonts en ajoutant un lien dans le `<head>` et en les appliquant via le CSS.

#### HTML :


```html
<head>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap">
</head>
```

#### CSS :


```css
body {
    font-family: 'Roboto', sans-serif;
}
```

### 8. **Mise en page avec Grid Layout**

Grid est un système de mise en page puissant en CSS.


```css
.container {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    grid-gap: 10px;
}

.box {
    background-color: #66ccff;
    padding: 20px;
    color: white;
    text-align: center;
}
```

HTML associé :


```html
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
```

# CSS Notions plus complexes

### 1. **Utilisation de `calc()` pour les calculs dynamiques**

La fonction `calc()` te permet de faire des calculs directement dans ton CSS, comme définir des largeurs ou marges basées sur des combinaisons de pourcentages et de valeurs fixes.


```css
.container {
    width: calc(100% - 40px); /* Largeur du conteneur égale à 100% de la fenêtre moins 40px */
    margin: 20px auto;
}

.box {
    width: calc(50% - 10px); /* Chaque boîte prendra 50% de l'espace avec un écart de 10px entre elles */
    background-color: #66ccff;
    padding: 10px;
    margin: 5px;
}
```

#### HTML associé :


```html
<div class="container">
    <div class="box">Boîte 1</div>
    <div class="box">Boîte 2</div>
</div>
```

### 2. **Sélecteurs d'enfants avec `:nth-child()` et `:first-child()`**

Ces sélecteurs te permettent de cibler des éléments en fonction de leur position dans le DOM. Par exemple, pour styliser les enfants pairs ou impairs, ou cibler spécifiquement le premier ou le dernier enfant.


```css
/* Styliser les enfants impairs */
.box:nth-child(odd) {
    background-color: #ffcc00;
}

/* Styliser les enfants pairs */
.box:nth-child(even) {
    background-color: #66ccff;
}

/* Le premier enfant */
.box:first-child {
    border: 2px solid red;
}

/* Le dernier enfant */
.box:last-child {
    border: 2px solid green;
}
```

#### HTML associé :


```html
<div class="container">
    <div class="box">Boîte 1</div>
    <div class="box">Boîte 2</div>
    <div class="box">Boîte 3</div>
    <div class="box">Boîte 4</div>
</div>
```

### 3. **Variables CSS (Custom Properties)**

Les variables CSS te permettent de définir des valeurs réutilisables, ce qui facilite la gestion des couleurs, des tailles ou autres propriétés.

### 4. **Sélecteurs de pseudo-éléments (`::before` et `::after`)**

Les pseudo-éléments te permettent d’ajouter du contenu avant ou après un élément sans modifier le HTML.


```css
h1::before {
    content: "→ ";
    color: #ff5722;
}

h1::after {
    content: " ←";
    color: #ff5722;
}
```

Code ASCII pour les flèches : 

`→` : alt + 26
`←` : alt + 27
#### HTML associé :


```html
<h1>Titre avec des pseudo-éléments</h1>
```

### 5. **Sélecteurs de frères avec `~` et `+`**

Ces sélecteurs te permettent de cibler des éléments en fonction de leur relation avec d'autres éléments dans le DOM.


```css
/* Cible un élément qui suit immédiatement un autre */
h1 + p {
    color: #00695c;
    font-weight: bold;
}

/* Cible tous les éléments suivants qui sont des frères d'un autre élément */
h1 ~ p {
    color: #009688;
}
```

#### HTML associé :


```html
<h1>Titre</h1>
<p>Ce paragraphe est juste après le h1.</p>
<p>Ce paragraphe est aussi affecté car il est un frère de h1.</p>
```

### 6. **Transformations et transitions CSS**

Les transformations permettent de manipuler visuellement les éléments (rotation, échelle, déplacement), et les transitions permettent d’ajouter des animations lors du changement de propriétés.


```css
.box {
    width: 100px;
    height: 100px;
    background-color: #66ccff;
    transition: transform 0.5s ease;
}

.box:hover {
    transform: scale(1.2) rotate(10deg);
}
```

#### HTML associé :


```html
<div class="box">Survole-moi !</div>
```

# Exercices

## Niveau Facile

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
</head>
<body>
    <h1>Je suis un titre</h1>
</body>
</html>
```

Avec ce code html : 

1. Mettre le titre en rouge
2. Changer la police du titre en :  'Courier New', Courier, monospace
3. Mettre en place une balise P avec le texte suivant : Le loup est descendu du nord
4. Le mot loup doit être mit en gras et de la couleur bleu 
5. Aligner le titre et le paragraphe
6. Mettre tout le titre en majuscule
7. Changer la taille du paragraphe
8. Changer l'espacement des lettres du titre
9. Changer la couleur de fond du site
10. Centrer le paragraphe
11. Ajouter une bordure sur le titre avec une marge intérieure
12. Faire en sorte de faire grossir le titre au passage de la souris
13. Effacer ce que contient votre body et placer 4 paragraphes et faites en sorte que les éléments pair soient coloré en rouge et les impairs en vert
