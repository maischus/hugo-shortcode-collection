# Hugo Shortcode Collection

[Hugo](https://gohugo.io) is a static site generator that can use Markdown as a content format. But sometimes Markdown falls short and one might want to add raw HTML to the content. This contradicts Markdown's simplicity. Hugo created [shortcodes](https://gohugo.io/content-management/shortcodes/) as way to add HTML snippets in a Markdown manner.

## Use

Just copy the HTML file corresponding to the listed shortcode into one of the following directory.

```
/layouts/shortcodes/
```

or

```
/themes/<THEME>/layouts/shortcodes/
```


## Available Shortcodes

The following shortcodes come with zero dependencies and can be used independently from each other.

### Fingernail

Takes a SVG file and replaces the color `#ff7870` and replaces it with another color.

```
{{< fingernail "fingernail.svg" "Bright Red" "#e33034" >}}
```

### Iframe

Allows to embedded documents (e.g. pdf files) into the page.

```
{{< iframe "manual.pdf#toolbar=0" >}}
```

### Quiz

Allows to create simple muliple-choice quizes. After each question, the possible answers follow. `( )` indicates that only one correct answer exists. This will be rendered to a radio element. `[ ]` indicates that multiple answers are correct. This will be rendered to a checkbox element. `space` between the brackets mark incorrect answers, `X` mark correct answers.

A question-and-answer block has to be seperated with an empty line.

```
{{< quiz >}}

How is the weather today?
(X) sunny
( ) cloudy
( ) rainy

What seasons exists?
[X] spring
[X] summer
[X] fall
[ ] apple tree
[X] winter

{{< /quiz >}}
```

### Video

Embedds a video.

```
{{< video "big-buck-bunny.mp4" >}}
```