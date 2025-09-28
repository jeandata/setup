# Instalações
Instalar os seguintes softwares:
- <a href="#python">1- Python </a>
 - <a href="#git"> 2- Git </a>
 - <a href="#github"> 3- GitHub </a>
 - <a href="#docker-desktop"> 4- Docker Desktop </a>
 - <a href="#gh-repo"> 5- Gh repo CLI </a>
 - <a href="#astro-cli"> 6- Astro CLI (Airflow) </a>

 ### Python
1- Para realizar a instalação do python acesse o site:
    
    https://www.python.org/downloads/

 2- Após realizar o download vá para o processo de instalação utilizando o .exe baixado. E não se esqueça de na primeira tela do setup marcar a caixinha de ADD Path.

 ### Git
 1- Para realizar a instalação do git acesse o site:
    
    https://git-scm.com/downloads

 2- Após realizar o download vá para o processo de instalação utilizando o .exe baixado.

 3- A primeira ação deverá ser:
 Antes de começar a usar o Git, precisamos configurar o nome e o e-mail do usuário:

    git config --global user.name "Seu Nome"
    git config --global user.email "seu.email@exemplo.com"

    *Seu Nome: Altere pelo seu nome.
    *seu.email@exemplo.com: Altere pelo seu e-mail.
   
 4- Para configurar o diretório inicial

      nano ~/.bash_profile

 Esse comando itá abrir o editor de texto. Dentro dele adicione o caminho que você quer ter padrão para o seu terminal do BASH, exemplo:

      cd /d/Projetos/Pasta

 ### GitHub
 Nesse primeiro momento não é necessário instalar nada do github, mas abaixo apresentarei a ferramenta CLI para ter a integração de criação de repositórios e configurações diretamente pelo terminal do Windows/Linux/Mac.

 Vamos criar nossa SSH para conectar ao GitHub.

 1- Abra o seu GIT Bash, que foi instalado durante o processo do GIT. Todos os comandos de CMD indicados serão realizados nesse terminal a partir de agora.
 Escreva esse comando.
 
    ssh-keygen -t ed25519
 
 2- Aperte ENTER até finalizar e criar sua SSH.

 3- Agora vamos visualizar a nossa SSH e copiá-la para configurar no site do GitHub.

    cat ~/.ssh/id_ed25519.pub
 
 4- Agora, com a chave pública copiada, vá até sua conta do GitHub e siga os passos:

    Vá para Settings (Configurações).
    Na seção SSH and GPG keys, clique em New SSH key.
    Cole a chave pública que você copiou do terminal no campo Key.
    Dê um nome à chave para identificá-la facilmente (por exemplo, "Meu PC").
    Clique em Add SSH key.

 5- Para testar se foi vinculado corretamente use o seguinte código:
    
    ssh -T git@github.com

 6- O que esperar: Se tudo estiver configurado corretamente, você verá uma mensagem como:

    Hi username! You've successfully authenticated, but GitHub does not provide shell access.

 ### Docker Desktop
 O Docker é necessário instalar caso você necessite simular o linux no seu PC Windows. Assim você consegue montar imagens do que será necessário para seus projetos.
 Exemplo para termos o AirFlow.

 1- Acesse o site do Docker Desktop e efetue o download.

    https://docs.docker.com/desktop/setup/install/windows-install/

 2- Após realizar o download vá para o processo de instalação utilizando o .exe baixado. 

 ### GH Repo
 O GH Repo é o cli do github. Com ele é possivel realizar as ações sem precisar acessar o ambiente.

 1- Acesse o site, baixe e instale.

    https://cli.github.com/

 2- Para se conectar use:
    
    gh auth login

 ### Astro CLI (AirFlow)
 1- Para instalar o Astro CLI.
    
    winget install -e --id Astronomer.Astro