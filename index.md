---
layout: base
title:
---


## Welcome to my website!


<div class="begin-examples"></div>

## The Markdown
We'll abuse some Markdown elements to get the layout we want. You can choose to style your page differently, but here we'll have code examples on the right, and code explanations on the left.

### First, we need to tell Markdown where the two column layout begins.
Anything before this element will be rendered normally.

```
<div class="begin-examples"></div>
```

And we should also tell it where the two column layout ends.

```
<div class="end-examples"></div>
```

### `h2` will be an example section header.

```
## Section title
```

And any text directly after the section title will not be split into two columns.

```
## Section title
This text, along with the title, remains in a single column
```

### Each point in a section starts with an `h3`.

```
### Main you want to make point here
```

### Normal text elements (`p`) are used for more detailed explanations. 
You can put them after the main point.

``` 
### Main point
Some explanatory text.
```

### Code is interleaved with explanatory text.

The main point or explanation for a piece of code should come directly before it.

    ### Main point about code block 1

    ```
    code block 1
    ```

    More text explaining code block 2

    ```
    code block 2
    ```

## Styling
We can use CSS to style the Markdown output to create a two column layout when readers view our page on a larger screen.

### The main section and subsection headings both take up the entire width of the page.

```
article .begin-examples ~ h2,
article .begin-examples ~ h2 + p {
    width: 100%;
    clear: both;
}
```

### Each column element is 50% width

```
article .begin-examples ~ h3,
article .begin-examples ~ p,
article .begin-examples ~ .highlight {
    width: 50%;
}
```

### The left column has the main point and explanation text (`h3` and `p`).
We'll add some padding here too for good measure.

```
article .begin-examples ~ h3,
article .begin-examples ~ p {
    float: left;
    box-sizing: border-box;
    padding-right: 1rem;
    clear: both;
}
```

### While the right column has only the code examples `.highlight`.
And some spacing between the sections.

```
article .begin-examples ~ .highlight {
    float: right;
    clear: right;
    margin-bottom: 1rem;
}
```

### That's it!
But we have to ensure that nothing goes past the end of content.

```
.end-examples {
    clear: both;
}
```

### But we should clean up after ourselves.
Reset the styles to stop the two column layout. This must come after all the other styles in the CSS file.

```
article .end-examples ~ p,
article .end-examples ~ h3,
article .end-examples ~ .highlight {
    width: auto;
    float: none;
    clear: none;
}
```


## Style For Small Screens
Using a media query on screens less that 580px in width, we'll create a single column layout again. 

### All you have to do is reset the styling on the main elements of the two column layout

```
article .begin-examples ~ h3,
article .begin-examples ~ p,
article .begin-examples ~ .highlight {
    width: 100%;
    float: none;
    clear: none;
}
```




## bla bla

![alt text](IMG_3437.jpeg)


I am a development economist and senior researcher at the [Stockholm International Peace Research Institute](https://www.sipri.org/), working in Peace & Development cluster. I am also a research affiliate at the [International Security and Development Center](http://isdc.org/). My research interests span from impact evaluations in developing countries to African pre-colonial development and the impact of Soviet policies on contemporary Russian development. Currently, I work on two large impact evaluations of peacebuilding programmes in Kyrgyzstan and a Panel Study [_Life in Kyrgyzstan (2010-2016)_](http://lifeinkyrgyzstan.org/). I did my PhD at the [Graduate Institute of International and Development Studies](http://graduateinstitute.ch/home.html) in Geneva. I worked for the World Bank on the impact evaluation of community monitoring in health and school facilities in Burkina Faso.

<div class="end-examples"></div>

## bla bla

Research fields: impact evaluations, ethnic diversity, child health and intrahousehold bargaining, social capital, colonialism, Soviet deporatations.

### Contact

<aladysheva@sipri.org>

Stockholm International Peace Research Institute, Signalistgatan, 9, SE-169 72 Solna, Sweden

![alt text](orcid_16x16.png) [orcid.org/0000-0002-4069-0486](http://orcid.org/0000-0002-4069-0486)

### Publications



### Working Papers


You can use the [editor on GitHub](https://github.com/aladysheva/test/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/aladysheva/test/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.


