# Hexo Theme - Siberia
Focus eye on reading, the posts on siberia.

# Install

1. Move to your hexo `themes` folder and enter the following line.

```
git clone https://github.com/hpcslag/hexo-theme-siberia.git themes/siberia
```

2. Modify `/<hexo_root>/_config.yml` on main folder:

```yaml
theme: siberia
```

3. Restart Hexo Server.

# Plugin Supports

| Name | Default Enabled | Default with Installed |
| -- | -- | -- |
| MathJax.js | no | yes |
| Prism | no | no |

### Prism Code Highlight Support
**Siberia** use [`hexo-prism-plugin`](https://github.com/ele828/hexo-prism-plugin) to display code highlight.

Please follwing the step to install:

1. Move to your hexo folder `/<hexo_root>/` and enter the following line.

```
npm i -S hexo-prism-plugin
```

and edit `/<hexo_root>/_config.yml`: 
 
```yaml
highlight:
  enable: false
```

Then adding the following line after the **last line** in `/<hexo_root>/_config.yml`:

```yaml
prism_plugin:
  mode: 'preprocess'    # realtime/preprocess
  theme: 'default'
  line_number: false    # default false
```

tips: you can change prism theme, please reference: [Prism Offical](http://prismjs.com/)

# Update

Enter the following line to update `Siberia` theme:

```shell
cd themes/siberia/ && git pull && cd ../..
```

# Written

`Siberia` provide addon feature for Post.

| Name | Usage |
| -- | -- |
| Image Description | &lt;p class=&quot;img-desc&quot;&gt;Description Here.&lt;/p&gt; |
| Video Content | &lt;div class=&quot;video-content&quot;&gt;youtube iframe here&lt;/div&gt; |
| LaTeX | $$ your math $$, $ your math$  |
| Tags | Like a usual, set `tags` in the post.md |
| Feature Tag | set the text in `ftag`, this parameter is inside to the post.md, also setup the translate text to `<hexo_root>/<theme>/_config.yml` |
| Feature Background | set the image url in `fbg`, this parameter is inside to the post.md |
| Feature Background Description | set image description in `fbgdesc`, this parameter is inside to the post.md |

### Image Description 
In the article (Read More), `Line-Height` distance are set to all of the element, `Image Description` can ignore the Line-Height set, and put the `Image Description` close to the image.

![](https://i.imgur.com/JoNFkCP.png)

Usage:
```html
![](/image/xxx.jpg)
<p class="img-desc">Reference: Image is download from [google](http://google.com).</p>
```

### Video Content

`Video Content` feature can help video fit to the full width. 

Usage:
```html
<div class="video-content">
	<iframe width="560" height="315" src="https://www.youtube.com/embed/9rzz2c6l-uM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>
```

### LaTeX
`LaTeX` feature is disabled by default, please open the feature in the file `/<hexo_root>/<theme>/_config.yml`, setup the `mathjax_enable` line to : `mathjax_enable: true`.

![](https://i.imgur.com/eJDGH2v.png)

Usage:
```html
When $a \ne 0$, there are two solutions to \(ax^2 + bx + c = 0\) and they are
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}$$
```

### Feature Tag
`Feature Tag` is the special feature by Siberia Theme, parameter are set in the head of post file(.md).
![](https://i.imgur.com/aMQt7Me.png)

Usage:
After create the post, add the following line before post head end.
``` shell
hexo new TEST
```

Example:
```md
---
title: ZoneFlex R500 Series, Unbox Introduction!
date: 2017-07-07 15:15:54
tags:
 - wireless
 - technology
ftag: unbox
---
```

`unbox` is only the viriable, you have to set the corresponding text on `/<hexo_root>/<theme>/_config.yml`, like the following line:

```yaml
#Feature Tags Translate (Only shows in one Language)
ftags:
  science: 科学ジャーナル
  unbox: UNBOX ANY THING
  play: 有好玩
```

### Feature Background and Description
`Feature Background`, `Feature Background Description` is the special feature by Siberia Theme, parameter are set in the head of post file(.md).

![](https://i.imgur.com/o6HIdkM.jpg)
Usage:
After create the post, add the following line before post head end.
``` shell
hexo new TEST
```

Example:
```md
---
title: Firework in Tokyo 2018!
date: 2017-07-07 15:15:54
tags:
 - culture
 - many_photo
ftag: festival
fbg: https://www.nhk-p.co.jp/common/event/main/s-stadium2016_main.jpg
fbgdesc: ＮＨＫサイエンス スタジアム２０１６
---
```

# Blog Config

Setup these configuration on `<hexo_root>/<theme>/_config.yml`.

![](https://i.imgur.com/gWUSI77.png)

| Name | YAML Key | Value | Example |
| -- | -- | -- | -- |
| Title | title_text | String | `Modern Siberia` |
| Bio | bio | String | `Do my best so I can't blame my self for anything.` |
| Avator | avator_image | URI Path | `/avator.jpg`(<hexo_root>/<theme>/source/) |
| Banner | banner | CSS Background | `url(/background/blur-cars-dew-125510.jpg)`(<hexo_root>/<theme>/source/background) |


# Theme Style Config

Setup these configuration on `<hexo_root>/<theme>/_config.yml`.

**Web Fonts Support**

Additional Web Fonts is set in `<hexo_root>/<theme>/layout/layout.ejs`, add your scripts between the mark `<!-- load your font here -->`.

### Title Style

| Name | YAML Key | Value | Example |
| -- | -- | -- | -- |
| Title Color | title_text_color | CSS Colors | `"#4d4d4d"` |
| Title Font | title_text_font | String | `"Artegra Sans Alt"` |

### Bio Style

| Name | YAML Key | Value | Example |
| -- | -- | -- | -- |
| Bio Color | bio_text_color | CSS Colors | `"#0061b5"` |
| Bio Font | bio_text_font | String | `"PT Serif"` |

### Header Style

| Name | YAML Key | Value | Example |
| -- | -- | -- | -- |
| Avator Image Position Offset (X) | avator_image_position_x | CSS Units | `"-31px"` |
| Avator Image Position Offset (Y) | avator_image_position_y | CSS Units | `"0px"` |
| Circle Color | circle_color | CSS Colors | `rgba(83, 207, 220, 0.7)` |
| Banner Filter Effects | banner_filter | CSS Filters | `"blur(2px) grayscale(20%)"` |
| Banner Mask Color | banner_mask_color | CSS Colors | `"#ffffff"` |
| Banner Mask Opacity | banner_mask_opacity | Float | 0.0 |

### Body Style

| Name | YAML Key | Value | Example |
| -- | -- | -- | -- |
| Body Background  | theme_style | CSS Background | `"#f2f2f2"` |
| Footer Background | footer_style | CSS Background | `"#151719"` |
| Footer Copyright Text Color| footer_text_color | CSS Colors | `"#8a8a8a"` |

### Article Reading Style

| Name | YAML Key | Value | Example |
| -- | -- | -- | -- |
| Article Text Size | article_text_size | CSS Units | `"19px"` |
| Article Text Color | article_text_color | CSS Colors | `"#151717"` |
| Article Link Color | article_link_color | CSS Colors | `"#29bcd0"` |
| Article Text Font | article_text_font | String | `"source-han-serif-tc"` |
| Article Title Font | article_title_font | String | `"source-han-serif-tc"` |
| Article Default Font | article_default_font | String | `Helvetica Neue, Helvetica, Microsoft JhengHei , Arial, sans-serif` |

### Layout Style

| Name | YAML Key | Value | Example |
| -- | -- | -- | -- |
| Background Color of Page Navigation In Article When Hovered | prev_next_button_color_hover |  CSS Colors | `"#151719"` |
| Text Color of Page Navigation In Article | prev_next_text_color | CSS Colors | `"#151719"` |
| Text Color of Page Navigation In Article When Hovered | prev_next_text_color_hover | CSS Colors | `white` |

# Theme Config For You

There are some color theme for you, please check out this **[Folder](https://github.com/hpcslag/hexo-theme-siberia/tree/master/colors)**.

# LICENSE
**Hexo Theme - Siberia** is released under the [MIT License.](https://github.com/hpcslag/hexo-theme-siberia/blob/master/LICENSE)

