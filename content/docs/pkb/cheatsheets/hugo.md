---
Title: "Hugo"
---

# Hugo Cheatsheet

Useful reference while I'm building my site.

## Shortcodes

### Buttons

```tpl
{{</* button relref="/" [class="..."] */>}}Go Home{{</* /button */>}}
{{</* button href="https://github.com/alex-shpak/hugo-book" */>}}Hugo-book repo{{</* /button */>}}
```

{{< button relref="/" >}}Go Home{{< /button >}}
{{< button href="https://github.com/alex-shpak/hugo-book" >}}Hugo-book repo{{< /button >}}

---

### Columns

```html
{{</* columns */>}} <!-- begin columns block -->
# Left Content
Lorem markdownum insigne...

<---> <!-- magic sparator, between columns -->

# Mid Content
Lorem markdownum insigne...

<---> <!-- magic sparator, between columns -->

# Right Content
Lorem markdownum insigne...
{{</* /columns */>}}
```

{{< columns >}}
### Left Content
Lorem markdownum insigne.


<--->

### Mid Content
Lorem markdownum insigne. 

<--->

### Right Content
Lorem markdownum insigne. 
{{< /columns >}}

---

### Expand

```tpl
{{</* expand "Optional-label 1" "label 2" */>}}
## Markdown content
Lorem markdownum insigne...
{{</* /expand */>}}
```

{{< expand "Optional-label 1" "label 2" >}}
### Markdown content
Lorem markdownum insigne...
{{< /expand >}}

---

### Hints

```tpl
{{</* hint [info|warning|danger] */>}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{</* /hint */>}}
```

{{< hint info >}}
**Markdown content**  
Lorem markdownum insigne. 
{{< /hint >}}

{{< hint warning >}}
**Markdown content**  
Lorem markdownum insigne. 
{{< /hint >}}

{{< hint danger >}}
**Markdown content**  
Lorem markdownum insigne.
{{< /hint >}}

---

### Maths - KaTeX

```latex
{{</* katex [display] [class="text-center"]  */>}}
x = \begin{cases}
   a &\text{if } b \\
   c &\text{if } d
\end{cases}
{{</* /katex */>}}
```

{{< katex >}}
x = \begin{cases}
   a &\text{if } b \\
   c &\text{if } d
\end{cases}
{{< /katex >}}

#### Inline/Display

```
Example: {{</* katex */>}}\pi(x){{</* /katex */>}}, rendered in the same line

below is `display` example, having `display: block`
{{</* katex display */>}}
x = \begin{cases}
   a &\text{if } b \\
   c &\text{if } d
\end{cases}
{{</* /katex */>}}
Etc.
```

Example: {{< katex >}}\pi(x){{< /katex >}}, rendered in the same line

below is `display` example, having `display: block`
{{< katex display >}}
x = \begin{cases}
   a &\text{if } b \\
   c &\text{if } d
\end{cases}
{{< /katex >}}
Etc.

---

### Charts - Mermaid

```tpl
{{</* mermaid [class="text-center"]*/>}}
sequenceDiagram
    Alice->>Bob: Hello Bob, how are you?
    alt is sick
        Bob->>Alice: Not so good :(
    else is well
        Bob->>Alice: Feeling fresh like a daisy
    end
    opt Extra response
        Bob->>Alice: Thanks for asking
    end
{{</* /mermaid */>}}
```

{{< mermaid >}}
sequenceDiagram
    Alice->>Bob: Hello Bob, how are you?
    alt is sick
        Bob->>Alice: Not so good :(
    else is well
        Bob->>Alice: Feeling fresh like a daisy
    end
    opt Extra response
        Bob->>Alice: Thanks for asking
    end
{{< /mermaid >}}

---

### Tabs

```tpl
{{</* tabs "uniqueid" */>}}
{{</* tab "MacOS" */>}} # MacOS Content {{</* /tab */>}}
{{</* tab "Linux" */>}} # Linux Content {{</* /tab */>}}
{{</* tab "Windows" */>}} # Windows Content {{</* /tab */>}}
{{</* /tabs */>}}
```

{{< tabs "uniqueid" >}}
{{< tab "MacOS" >}}
# MacOS

This is tab **MacOS** content.

{{< /tab >}}

{{< tab "Linux" >}}

# Linux

This is tab **Linux** content.

{{< /tab >}}

{{< tab "Windows" >}}

# Windows

This is tab **Windows** content.

{{< /tab >}}
{{< /tabs >}}
