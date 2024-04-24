# Teste de Sistemas Operativos - Módulo 3

Faz *fork* do repositório para teres a tua cópia.

Preenche o ficheiro README diretamente no GitHub. A partir da página principal do repositório, clica em "Edit File" (ícone representando um lápis).

Escreve as respostas dentro dos blocos correspondentes. Substitui as reticências pelo que é pedido em cada pergunta. Não desformates o documento.

Quando acabares, carrega no botão "Commit Changes".

## Informação do aluno

    Nome: vitor santos

## P1 - Para as seguintes questões, assinala a opção correta: (2.5v)

  1. Qual das seguintes afirmações caracteriza melhor um SO servidor?

    a) Projetado para computação de uso geral
    b) Otimizado para alta disponibilidade e confiabilidade
    c) Destinado a usuários individuais
    d) Usado principalmente para jogos
    
    Resposta: b)

  2. Das seguintes, qual é a função mais apropriada para um SO servidor?

    a) Executar aplicações de desktop
    b) Desenvolver aplicações móveis
    c) Fornecer software de entretenimento
    d) Gerir recursos e serviços de rede
    
    Resposta: d)
   
  3. Qual dos seguintes é um sistema operativo servidor popular?

    a) Windows 11
    b) macOS Big Sur
    c) Ubuntu Server
    d) Android
    
    Resposta: c)

  4. Qual é o papel de um servidor num modelo cliente-servidor?

    a) Consumir recursos fornecidos pelos clientes
    b) Fornecer recursos e serviços aos clientes
    c) Atuar como uma estação de trabalho independente
    d) Facilitar a comunicação ponto a ponto
    
    Resposta: b)

  5. Qual dos seguintes protocolos é mais usado para aceder remotamente a servidores?

    a) FTP
    b) HTTP
    c) SSH
    d) SMTP
    
    Resposta: c)

## P2 - Indica, sequencialmnente, os comandos para realizar as seguintes instruções: (7.5v)

  1. Cria um diretório com o nome "ex1", entra no mesmo, e cria 3 ficheiros vazios com os nomes "f1", "f2", "f3". No fim, lista os conteúdos do diretório atual.

    Resposta:
    
    mkdir ex1
    cd ex1
    touch f1 f2 f3
    ls

    
  2. Assumindo que estás no diretório "ex1", renomeia os ficheiros "f1" e "f2" para que acabem com "_antigo", e cria cópias dos mesmos.

    Resposta:
    mv f1 f1_antigo
    mv f2 f2_antigo
    cp f1_antigo f1_copia
    cp f2_antigo f2_copia


  3. Assumindo que estás no diretório "ex1", cria o diretório "ex2", e move os ficheiros copiados no exercício anterior para o novo diretório. Seguidamente, apaga os ficheiros originais.

    Resposta:
    mkdir ex2
    mv f1_copia f2_copia ex2
    rm f1_antigo f2_antigo
        

  4. Atualiza os repositórios de *packages* para garantir acesso às *packages* mais recentes, e instala o serviço **htop**.

    Resposta:
    sudo apt update
    sudo apt install htop


  5. Cria um novo utilizador com o teu primeiro nome, e com o diretório "/home/nome_de_utilizador". Mostra a informação (ID) do utilizador criado.

    Resposta:
    sudo adduser primeiro_nome
    id primeiro_nome


## P3 - Realiza os seguintes exercícios, com respostas detalhadas: (6v)

  1. Indica alguns aspetos que diferenciam um SO cliente de um SO servidor.

    Resposta:
Propósito: Um SO cliente é projetado para atender às necessidades individuais de computação de um usuário, fornecendo uma interface gráfica amigável e suporte para aplicativos de uso geral. Por outro lado, um SO servidor é otimizado para oferecer serviços a outros dispositivos ou usuários, com ênfase em estabilidade, segurança e desempenho.
Recursos e Serviços: Um SO cliente geralmente não fornece serviços de rede avançados, como hospedagem de sites, compartilhamento de arquivos ou execução de aplicativos em rede. Um SO servidor, por outro lado, é projetado para oferecer esses tipos de serviços e gerenciar recursos de rede.
Interface de Usuário: Enquanto um SO cliente geralmente possui uma interface gráfica de usuário (GUI) para facilitar a interação do usuário com o sistema, um SO servidor muitas vezes opera sem uma GUI ou com uma GUI mínima, já que a maioria das interações ocorre remotamente via linha de comando ou interfaces web.
     
  2. Explica a importância de otimizar um sistema operativo servidor, com exemplos de técnicas para otimização.

    Resposta:
    Desempenho: A otimização de um SO servidor é crucial para garantir um desempenho consistente e eficiente, especialmente em ambientes de alto tráfego. Técnicas de otimização incluem ajustes de configuração do sistema, otimização de recursos de hardware, ajustes de rede e afinidade de processo.
Segurança: A otimização também desempenha um papel importante na segurança do servidor, garantindo que apenas os serviços necessários estejam em execução, que as configurações de segurança sejam adequadas e que as atualizações de segurança sejam aplicadas regularmente.
Escalabilidade: Servidores otimizados podem lidar melhor com picos de carga e escalonamento de recursos, garantindo que os serviços permaneçam disponíveis mesmo sob demanda intensa. Isso pode envolver a distribuição de carga entre servidores, balanceamento de carga e implementação de caches.
Exemplos de técnicas de otimização: Uso de sistemas de arquivos otimizados, ajustes de parâmetros de rede, configuração de cache de disco, ajustes de memória e afinidade de CPU, otimização de consultas de banco de dados, implementação de balanceamento de carga e redundância de hardware, entre outros.

  3. Descreve o processo de instalar e configurar um servidor web num SO servidor, incluindo as etapas necessárias.

    Resposta:
    Escolha do servidor web: Selecionar um servidor web adequado, como Apache, Nginx ou Lighttpd, com base nos requisitos específicos do projeto.
Instalação do servidor web: Usar o gerenciador de pacotes do sistema operacional para instalar o servidor web escolhido. Por exemplo, no Ubuntu, você pode usar apt para instalar o Apache: sudo apt install apache2.
Configuração básica: Após a instalação, o servidor web pode exigir configurações básicas, como definição de diretórios de documentos raiz, configuração de permissões de acesso e definição de opções de segurança.
Configuração de hospedagem: Configurar o servidor web para hospedar sites ou aplicativos, criando virtual hosts (no caso do Apache) ou configurando blocos de servidor (no caso do Nginx) para cada site a ser hospedado.
Teste e ajuste: Testar a configuração do servidor web para garantir que os sites estejam sendo servidos corretamente. Ajustar as configurações conforme necessário para otimizar o desempenho e a segurança.
Adição de funcionalidades: Dependendo dos requisitos do projeto, podem ser necessárias instalações adicionais, como PHP, MySQL (ou outro banco de dados), SSL/TLS para criptografia, entre outros. Estas são configuradas e integradas ao servidor web conforme necessário.

## P4 - Indica os comandos **git** para realizar as seguintes operações: (4v)

  1. Considera que estás no ramo 'master' de um repositório git criado localmente. Associa este repositório ao repositório remoto contido no url 'https://github.com/SO/OMeuRepositorioRemoto'. Altera o nome do ramo atual para 'main', e envia os *commits* já feitos localmente para o repositório remoto.

    Resposta:
    git remote add origin https://github.com/SO/OMeuRepositorioRemoto
    git branch -M main
    git push -u origin main


  2. Considera que estás na pasta raiz do teu repositório local, onde atualizaste um ficheiro de nome 'index.html'. Envia **apenas** esta atualização para o teu repositório remoto, com uma mensagem de commit apropriada.

    Resposta:
    git add index.html
    git commit -m "Atualização do arquivo index.html"
    git push origin main

