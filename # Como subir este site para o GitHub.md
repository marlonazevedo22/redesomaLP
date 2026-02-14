# Como subir este site para o GitHub

1. Crie um repositório novo no GitHub (ex: `rede-soma-santacruz`).
2. No seu computador, coloque todos os arquivos do site (`index.html`, `logo.png`, `cupomfeed.png` etc) em uma pasta.
3. Abra o terminal/cmd nessa pasta e execute:
   ```sh
   git init
   git add .
   git commit -m "Landing page Rede Soma Santa Cruz"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
   git push -u origin main
   ```
4. No GitHub, ative o GitHub Pages em **Settings > Pages > Source: main / root**.
5. O site ficará disponível em `https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO`.

Pronto! Seu site estará online e pronto para campanhas.

# Como atualizar este site no GitHub

1. Faça as alterações desejadas nos arquivos do site na sua máquina.
2. Abra o terminal/cmd na pasta do projeto.
3. Execute os comandos abaixo para atualizar o repositório remoto:

   ```sh
   git add .
   git commit -m "Atualização do site"
   git push
   ```

4. Aguarde alguns segundos e recarregue a página do GitHub Pages para ver as mudanças publicadas.

Se aparecer algum erro, verifique se está na pasta correta e se já fez o `git init` e o `git remote add origin` anteriormente.
