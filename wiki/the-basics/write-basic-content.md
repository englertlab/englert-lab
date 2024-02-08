# ✍ Write Basic Content

The creators of this website template, the Greene Lab, have provided an online testbed for what formatting and various tables, paragraph styles, and header types--> 👁 [PREVIEW](https://greenelab.github.io/lab-website-template/testbed#basic-formatting)

[Markdown](https://commonmark.org/help/) is a way to write basic text content and formatting in a clean and simple way. Markdown `.md` files are plain text files that get converted into `.html` pages on your resulting website.

## Links

To an external site:

```markdown
[Link text](https://some-website.org/)
```

To a page within your site:

```markdown
[Meet our team!](team)
```

The example above works in most cases, because your site is likely to only have top-level pages and the URL is relative to the level of the current page. If you have sub-pages or more complex linking needs, see below.

<details>

<summary>Advanced Syntax</summary>



ou can of course use any [standard path syntax](https://www.w3schools.com/html/html\_filepaths.asp):

```markdown
Page/photo located in same folder as current page (i.e. a sub-page)
[Link text](page)
[Link text](photo.jpg)

Photo located in sub-folder of current page
[Link text](assets/photo.jpg)

Photo located in folder one level up from current page
[Link text](../photo.jpg)

Page/sub-page, starting from root of website
[Link text](/page)
[Link text](/page/sub-page)
```

But note, if starting from root (last examples above), you need to prepend your "baseurl", if the [URL you set up](broken-reference) has one (e.g. `your-lab.github.io/your-lab-website`):

```markdown
Manually prepend baseurl
[Link text](/englert-lab/page/sub-page)

Jekyll automatically prepends the right baseurl
[Link text]({{ "/page/sub-page" | relative_url }})
[Link text]({% link page/sub-page/
```

</details>

## Link parameters

The above section shows how you can write links as plain text content. But you will probably more often be linking to images/pages/whatever using the template's components, data lists, and front matters. In these cases, links work slightly differently.

You can still link to an external, absolute URL, e.g. `https://some-website.org/`. But if you are trying to link to something within your repo, the URL **must start from the root of your repo**, without any site name/"baseurl" prefix. You also cannot refer to files relative to the current file, or use the `..` to move up folders.

<mark style="color:green;">**✓ GOOD**</mark>

<pre class="language-liquid"><code class="lang-liquid"><strong>{% include some-component.html image="images/photo.jpg" %}
</strong></code></pre>

<pre class="language-markdown"><code class="lang-markdown">---
<strong>image: https://some-website.org/journal-cover.jpg
</strong>---
</code></pre>

```yaml
- id: 123
  link: team/join
```

<mark style="color:red;">**✘ BAD**</mark>

```liquid
{% raw %}
{% include some-component.html link="../images/photo.jpg" %}
{% endraw %}
```

```markdown
---
image: ./image-in-current-folder.jpg
---
```

```yaml
- id: 123
  link: /your-lab-website/team/join
```

## **Basic text styles**

```markdown
_italic text_
```

```markdown
**bold text**
```

```markdown
~~strike-through text~~
```

## **Line breaks**

```html
<br>
<br>
Text with extra blank lines above and below
<br>
<br>
```

## **Comments**

```markdown
<!-- a comment in HTML -->

{% raw %}
{% comment %}
A comment in Liquid
{% endcomment %}
{% endraw %}
```

## **Lists**

```markdown
- list item a
- list item b
- list item c
```

```markdown
1. ordered list item 1
2. ordered list item 2
3. ordered list item 3
```

## Images

```
![plain image](/images/photo.jpg)
```

For most purposes, prefer using the more richly featured (e.g. captions) and styled [figure](broken-reference) component instead.

## **Headings**

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
```

## **Horizontal rule**

```markdown
---
```

## **Table**

With left-aligned, centered, and right-aligned columns.

```markdown
| TABLE | Game 1 | Game 2 | Game 3 | Total |
| :---- | :----: | :----: | :----: | ----: |
| Anna  |  144   |  123   |  218   |  485  |
| Bill  |   90   |  175   |  120   |  385  |
| Cara  |  102   |  214   |  233   |  549  |
```

## **Block quote**

```markdown
> It was the best of times it was the worst of times.
> It was the age of wisdom, it was the age of foolishness.
> It was the spring of hope, it was the winter of despair.
```

## **Code block**

With syntax highlighting.

````markdown
```javascript
// a comment
const popup = document.querySelector("#popup");
popup.style.width = "100%";
popup.innerText = "Lorem ipsum dolor sit amet.";
```
````

## **Inline code**

```markdown
This sentence has `inline code`, useful for making references to variables, packages, versions, etc. within a sentence.
```

## **Util classes**

In Markdown, you can attach an arbitrary [CSS](broken-reference) class to an element with the syntax `{:.class}`. Depending on the type of element, this code may have to go on the same line or on the next line.

The template comes with a few alignment utility classes:

```markdown
Lorem ipsum dolor sit amet.
{:.left}
Consectetur adipiscing elit.
{:.center}
Sed do eiusmod tempor incididunt.
{:.right}
```

Most things in the template are centered by default where appropriate, and left/right in a few other places where appropriate. But sometimes you may want to force the alignment of something.
