<!-- Banner principal com seu nome (corrigido) -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=00F5A0&center=true&vCenter=true&width=600&lines=Henrique+Delgado;Desenvolvedor+em+forma%C3%A7%C3%A3o;Apaixonado+por+tecnologia+e+inova%C3%A7%C3%A3o;Desenvolvimento+de+Sistemas+no+SENAI" alt="Typing SVG" />
</p>
<br>

<!-- Linha divisória animada -->
<img src="https://i.imgur.com/dBaSKWF.gif" height="20" width="100%" />

## 🌟 Sobre mim
💡 Curioso nato e apaixonado por aprender, estou sempre explorando novas áreas da tecnologia.  
📚 Atualmente estudando **Qualidade** no **COTIL-UNICAMP**, com foco em **matemática, física e desenvolvimento de software**.  
🚀 Trabalhando em projetos acadêmicos e pessoais que envolvem **transformação digital, design no Figma e automação**.  
🎯 Objetivo: contribuir para um **Brasil mais digital e inovador**, com impacto positivo na economia e sociedade.

---

## 📊 Estatísticas do GitHub
<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=HenriqueDelgadoo&show_icons=true&theme=radical&count_private=true&hide_border=true" />
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=HenriqueDelgadoo&layout=compact&theme=radical&hide_border=true" />
</div>

---

## 🎮 Github Breakout (Contributions Game)
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="images/breakout-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="images/breakout-light.svg" />
  <img alt="Breakout Game" src="images/breakout-light.svg" />
</picture>

> As imagens acima são geradas automaticamente por GitHub Actions (veja o **setup** mais abaixo).

---

## 💻 Tecnologias & Ferramentas
<details open>
  <summary><b>👨‍💻 Linguagens de Programação</b></summary>
  <p>
    <img src="https://skillicons.dev/icons?i=js,ts,python,dart" />
  </p>
</details>

<details>
  <summary><b>🌐 Front-end</b></summary>
  <p>
    <img src="https://skillicons.dev/icons?i=html,css" />
  </p>
</details>

<details>
  <summary><b>🛠 Ferramentas de Trabalho</b></summary>
  <p>
    <img src="https://skillicons.dev/icons?i=git,github,vscode,figma" />
  </p>
</details>

---

## 🚀 Projetos em Destaque
- 📌 **Impacto das Transformações Digitais na Economia Brasileira** *(TCC - Estudo de caso Magazine Luiza)*
- 🛡 **Sistema de Alerta para Rompimento de Barragens** *(Tecnologias emergentes para prevenção de desastres)*
- 📚 **Design no Figma** para uma **Biblioteca Online**

---

## 📈 Atividade
<div align="center">
  <img src="https://streak-stats.demolab.com?user=HenriqueDelgadoo&theme=radical&hide_border=true" alt="GitHub Streak" />
</div>

---

## 📫 Contato
<p align="center">
  <a href="mailto:henriquedelgado055@gmail.com"><img src="https://img.shields.io/badge/Email-0078D4?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://www.linkedin.com/in/henrique-delgado-a08887305/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
</p>

---

<p align="center">
  <img src="https://profile-counter.glitch.me/{HenriqueDelgadoo}/count.svg" />
</p>

<p align="center">
  <em>"A transformação que você deseja no mundo começa em você mesmo."</em>
</p>

---

## ⚙️ Setup do Breakout (GitHub Action)
Crie o arquivo **`.github/workflows/generate-breakout.yml`** com:

```yaml
name: generate breakout svg

on:
  schedule:
    - cron: "0 */24 * * *"
  workflow_dispatch:

jobs:
  generate-svg:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: generate SVG
        uses: cyprieng/github-breakout@v1.0.0
        with:
          github_username: ${{ github.repository_owner }}

      - name: Move generated SVGs
        run: |
          mkdir -p images
          mv output/light.svg images/breakout-light.svg
          mv output/dark.svg images/breakout-dark.svg

      - name: Configure git
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "github-actions[bot]@users.noreply.github.com"

      - name: Commit and push SVGs
        run: |
          git add images/breakout-light.svg images/breakout-dark.svg
          git commit -m "chore: update breakout SVGs" || echo "No changes to commit"
          git push
