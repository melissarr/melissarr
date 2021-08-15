### hello coders! <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="25px">
<a href="#"><img align="right" src="https://github.com/blackcater/blackcater/raw/main/images/banner.gif" width="200 " height="200" /></a> 

꒷꒦꒷꒦꒷꒦꒷꒦꒷꒦꒷

She/her

[![Melissar's GitHub stats](https://github-readme-stats.vercel.app/api?username=melissarr&theme=dracula)](https://github.com/anuraghazra/github-readme-stats)

## <img height="40" src="https://raw.githubusercontent.com/innng/innng/master/assets/kyubey.gif"/> some links
[![](https://img.shields.io/badge/-music-0073B1?style=flat-square)](https://youtu.be/1w7OgIMMRc4)
[![](https://img.shields.io/badge/-animals-1C9CEA?style=flat-square)](https://twitter.com/BichinhosFB?s=09)
[![](https://img.shields.io/badge/-instagram-EE3E5D?style=flat-square)](https://www.instagram.com/steisser/)
[![](https://img.shields.io/badge/-github-332B40?style=flat-square)](https://github.com/melissarr/)
[![](https://img.shields.io/badge/-my.wish.list-2D4E00?style=flat-square)](https://www.amazon.com.br/hz/wishlist/ls/6PB7FHQF8GWA?ref_=wl_share)

![Visitor Count](https://profile-counter.glitch.me/melissarr/count.svg)

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: kamisinha
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output 
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
