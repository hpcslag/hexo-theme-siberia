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

# Blog Config

# Theme Style Config

# Theme Config For You

# LICENSE
**Hexo Theme - Siberia** is released under the [MIT License.](https://github.com/hpcslag/hexo-theme-siberia/blob/master/LICENSE)

