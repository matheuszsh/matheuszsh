![header](https://github.com/user-attachments/assets/ce76ff69-2f5f-462f-a415-dd6b72f91f9d)

<br>
<br>

<h3 align="left">Social Medias</h3>

[![E-mail](https://img.shields.io/badge/-Email-000?style=for-the-badge&logo=microsoft-outlook&logoColor=62FF00&color:FFF)](mailto:matheusrodrigues.workmail@gmail.com)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-000?style=for-the-badge&logo=linkedin&logoColor=62FF00&color:FFF)](https://www.linkedin.com/in/matheusrodrigues-me/)

<h3 align="left">Hardskills</h3>
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="25" alt="html5 logo"  />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="25" alt="css3 logo"  />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-plain.svg" height="25" alt="javascript logo"  />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/angular/angular-original.svg" height="25" alt="mysql logo"  />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="25" alt="mysql logo"  />
  <img width="8" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="25" alt="mysql logo"  />
  <img width="8" />
</div>


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
          github_user_name: username matheuszsh
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}****
