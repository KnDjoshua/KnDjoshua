<br clear="both">

<div align="left">
  <img height="200" src="https://media.licdn.com/dms/image/D4D03AQF0QLbyi-CtDQ/profile-displayphoto-shrink_800_800/0/1693807200786?e=1699488000&v=beta&t=I_rmgswxqy87Ox1IsMo947CZ9jQnWULQ7UsHPqrMkh4"  />
</div>

###

<p align="left">Networking and Cyber Security | Penetration Testing | Network Security | Web Developer |<br>Church Media Tech |</p>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="40" alt="react logo"  />
</div>

###

<div align="left">
  <img src="https://profile-counter.glitch.me/kndjoshua /count.svg?"  />
</div>

###

<div align="left">
  <a href="www.linkedin.com/in/kndjoshua-🥷-459a74196" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg" width="52" height="40" alt="linkedin logo"  />
  </a>
  <a href="https://twitter.com/kn_djoshua?lang=en" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/twitter/default.svg" width="52" height="40" alt="twitter logo"  />
  </a>
  <a href="https://www.youtube.com/channel/UCcgzlxuWPeucvPQjVro8xvA?sub_confirmation=1" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/youtube/default.svg" width="52" height="40" alt="youtube logo"  />
  </a>
  <a href="https://m.facebook.com/KnDjoshua/" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/facebook/default.svg" width="52" height="40" alt="facebook logo"  />
  </a>
  <a href="https://wa.me/+256760447637?text=Hello 👋%20KnDjoshua%20🥷%20sale" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/whatsapp/default.svg" width="52" height="40" alt="whatsapp logo"  />
  </a>
</div>

name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v2
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v2.6.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
###

<br clear="both">

<img src="https://raw.githubusercontent.com/kndjoshua /kndjoshua /output/snake.svg" alt="Snake animation" />

###
