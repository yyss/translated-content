---
title: animation-name
slug: Web/CSS/animation-name
---

{{CSSRef}}

La propriété **`animation-name`** définit une liste d'animations qui doivent être appliquées à l'élément ciblé. Chaque nom indique une règle @ {{cssxref("@keyframes")}} qui définit les valeurs des propriétés pour la séquence.

{{InteractiveExample("CSS Demo: animation-name")}}

```css interactive-example-choice
animation-name: none;
```

```css interactive-example-choice
animation-name: slide;
```

```css interactive-example-choice
animation-name: bounce;
```

```html interactive-example
<section class="flex-column" id="default-example">
  <div class="animating" id="example-element"></div>
</section>
```

```css interactive-example
#example-element {
  animation-direction: alternate;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in;
  background-color: #1766aa;
  border-radius: 50%;
  border: 5px solid #333;
  color: white;
  height: 150px;
  margin: auto;
  margin-left: 0;
  width: 150px;
}

@keyframes slide {
  from {
    background-color: orange;
    color: black;
    margin-left: 0;
  }
  to {
    background-color: orange;
    color: black;
    margin-left: 80%;
  }
}

@keyframes bounce {
  from {
    background-color: orange;
    color: black;
    margin-top: 0;
  }
  to {
    background-color: orange;
    color: black;
    margin-top: 40%;
  }
}
```

Généralement, on pourra utiliser la propriété raccourcie {{cssxref("animation")}} pour définir l'ensemble des propriétés liées aux animations.

## Syntaxe

```css
/* Valeur avec un mot-clé */
animation-name: none;

/* Valeur utilisant un identifiant */
animation-name: test_05;

/* Gestion de plusieurs animations */
animation-name: test1, animation4;

/*  Valeurs globales * /
animation-name: initial
animation-name: inherit
animation-name: unset
```

### Valeurs

- `none`
  - : Un mot-clé qui indique qu'aucune étape (_keyframe_) ne sera utilisée. Il peut être utilisée pour désactiver une animation sans changer l'ordre des autres identifiants ou afin de désactiver les animations provenant de la cascade.
- {{cssxref("custom-ident","&lt;custom-ident&gt;")}}
  - : Une chaîne de caractères qui identifie l'animation. Un identifiant est une séquence, insensible à la casse, de lettres entre `a` et `z`, de nombres entre `0` et `9`, de tirets bas (`_`) et/ou de tirets (`-`). Le première caractère qui n'est pas un tiret doit être une lettre. Il est également interdit d'utiliser deux tirets en début d'identifiant. Enfin, la chaîne de l'identifiant ne peut pas être `unset`, `initial`, `inherit` ou une combinaison analogue avec une casse différente.

> [!NOTE]
> Lorsqu'on utiliser plusieurs valeurs, séparées par des virgules, pour une propriété `animation-*`, selon leur quantité, elles seront différemment affectées aux animations définies par {{cssxref("animation-name")}}. Pour plus d'informations, voir : paramétrer [les valeurs des propriétés pour plusieurs animations](/fr/docs/Web/CSS/CSS_animations/Using_CSS_animations).

## Définition formelle

{{CSSInfo}}

## Syntaxe formelle

{{CSSSyntax}}

## Exemples

### CSS

```css
p {
  animation-duration: 3s;
  animation-name: glissement;
  animation-iteration-count: infinite;
}
@keyframes glissement {
  from {
    margin-left: 100%;
    width: 300%;
  }

  to {
    margin-left: 0%;
    width: 100%;
  }
}
```

### HTML

```html
<p>
  La Chenille et Alice se considérèrent un instant en silence. Enfin la Chenille
  sortit le houka de sa bouche, et lui adressa la parole d’une voix endormie et
  traînante.
</p>
```

### Résultat

{{EmbedLiveSample("Exemples","300","200")}}

## Spécifications

{{Specifications}}

## Compatibilité des navigateurs

{{Compat}}

## Voir aussi

- [Manipuler les animations CSS](/fr/docs/Web/CSS/CSS_animations/Using_CSS_animations)
- {{domxref("AnimationEvent", "AnimationEvent")}}
