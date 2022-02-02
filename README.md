# heroku-lavalink
Easily deploy a [lavalink](https://github.com/freyacodes/Lavalink) server on heroku.
This is a very elementary and barebones approach, but reliable nonetheless.
This branch will automatically download the latest Lavalink jar file.

### *heroku-lavalink will now download the latest Lavalink.jar automatically & directly from GitHub*
*To update your Lavalink.jar, restart all dynos (faster) or redeploy.*

### One Click Deploy:
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/uniaodalua/heroku-lavalink/tree/auto)

Buildpacks should be added automatically, you may modify the `PASS` variable during setup to change the password.

### Github Deploy:
1. Crie uma bifurcação deste repositório
16
2. Navegue até seu projeto heroku @dashboard.heroku.com
17
3. Navegue até o seu projeto *"Settings"*, clique em *"Reaveal Config Vars"* e defina uma nova var chamada *PASS* para o que você deseja que seja sua senha de lavalink.
18
4. No mesmo menu, defina uma nova var chamada JAVA_TOOL_OPTIONS e defina-a como "-XX:+UseContainerSupport -
Xmx500m -Xss256k -XX:CICompilerCount=2 -Dfile.encoding=UTF-8" sem o "" , isso definirá a RAM para o máximo em um dinamômetro livre
19
5. Navegue até a guia *"Implantar"*
20
6. Localize/Clique na seção *"Conectar ao GitHub"* e faça login, se necessário
21
7. Para o nome do repositório, digite *"heroku-lavalink"* e clique em *"Pesquisar"*
22
8. Clique em *"Conectar"*
23
9.
Role para baixo e encontre *"Manual Deploy"*, então mude o branch para auto e *"Deploy Branch"*.

### Heroku CLI Deploy:
1. Baixe os arquivos (Clone ou baixe->Baixar ZIP).
2. Extraia os arquivos em um diretório vazio.
3. Siga https://devcenter.heroku.com/articles/git.
Se o heroku não puder configurar os buildpacks automaticamente, vá para as configurações do seu projeto no site do heroku e adicione java e nodejs.
4. Vá para as configurações do seu projeto-
>config vars no heroku e defina um novo var chamado PASS para o que você deseja que sua senha de lavalink seja.
5. No mesmo menu, defina um novo var chamado JAVA_TOOL_OPTIONS e defina-o como "-XX:+UseContainerSupport -Xmx500m -Xss256k -XX:CICompilerCount=2 -Dfile.encoding=UTF-8" sem o "" , isso definirá ram ao máximo em um dyno grátis

**Notas:**
1.
Após alterar o PASS, você deve reimplantar ou clicar no menu Mais e *reiniciar todos os dynos*.
2. Se o heroku não puder configurar os buildpacks automaticamente, vá para as configurações do seu projeto no site do heroku e adicione java e nodejs.

Por favor, entenda que seu servidor lavalink ***provavelmente ficará sem memória em um dinamômetro gratuito***.
Eu recomendaria atualizar ou mudar para uma alternativa mais leve. Se você atualizar, você deve alterar -Xmx no JAVA_TOOL_OPTIONS para sua nova quantidade de ram.

Precisa de um bot de música leve e funcional, sem usar o lavalink?
Confira [Mandarine](https://github.com/karyeet/Mandarine)!
