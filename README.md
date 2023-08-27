### Olá, sou o Alê! 🦄

##

- 👾 Estudante de Ciencias da Computação

<div align="center">
  <a href="https://github.com/allecporfirio">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=allecporfirio&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=allecporfirio&layout=compact&langs_count=7&theme=tokyonight"/>
</div>

  ##
  
  <div>
      <a href="https://www.linkedin.com/in/alessandro-porfírio-124790184/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>

   # Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: allecporfirio #Seu usuario
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  


  </div>

  
  
  ![c633c20ede82f0e0ced7d570dbe3a1f3](https://user-images.githubusercontent.com/70382532/138322189-2db8df52-9dcb-40a0-88a8-c365466bd33d.gif)
