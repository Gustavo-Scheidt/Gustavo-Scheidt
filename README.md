
<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:050816,50:0B3D91,100:00BFFF&height=180&section=header&text=Gustavo%20Von%20Scheidt&fontSize=38&fontColor=ffffff&fontAlignY=38&animation=fadeIn&desc=Technology%20%7C%20Data%20%7C%20Development&descAlignY=60&descSize=15"/>

<a href="https://git.io/typing-svg">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=19&duration=3000&pause=1000&color=00BFFF&center=true&vCenter=true&width=650&lines=Ol%C3%A1%2C+eu+sou+Gustavo!;Estudante+de+Engenharia+de+Software;Explorando+o+mundo+dos+Dados;Construindo+solu%C3%A7%C3%B5es+com+tecnologia" alt="Typing SVG"/>
</a>

</div>

---

## 👨‍💻 Sobre mim

Sou estudante de Engenharia de Software, interessado em tecnologia, análise de dados e desenvolvimento de soluções.

Gosto de aprender novas ferramentas, resolver problemas e transformar ideias em projetos práticos. Estou sempre buscando evoluir minhas habilidades técnicas e crescer profissionalmente na área de tecnologia.

---

## 🚀 Tecnologias e ferramentas

<div align="center">

<img src="https://skillicons.dev/icons?i=python,html,css,js,git,github,vscode&theme=dark"/>

<br><br>

<img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
<img src="https://img.shields.io/badge/Data%20Analytics-0078D4?style=for-the-badge&logo=databricks&logoColor=white"/>

</div>

---

## 📊 Estatísticas do GitHub

<div align="center">

<img height="165em" src="https://github-readme-stats.vercel.app/api?username=Gustavo-Scheidt&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true"/>

<img height="165em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Gustavo-Scheidt&layout=compact&theme=tokyonight&hide_border=true"/>

<br>

<img width="65%" src="https://streak-stats.demolab.com?user=Gustavo-Scheidt&theme=tokyonight&hide_border=true"/>

</div>

---

## 🐍 Minhas contribuições

<div align="center">

<img src="https://raw.githubusercontent.com/Gustavo-Scheidt/Gustavo-Scheidt/output/snake.svg" alt="Snake animation"/>

</div>

---

<div align="center">

### ✨ Sempre aprendendo. Sempre evoluindo.

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00BFFF,100:050816&height=100&section=footer"/>

</div>

name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: Generate Snake
        uses: Platane/snk@v3
        with:
          github_user_name: Gustavo-Scheidt
          outputs: |
            dist/snake.svg
            dist/snake-dark.svg?palette=github-dark

      - name: Publish Snake
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
