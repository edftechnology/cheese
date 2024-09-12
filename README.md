# Como configurar/instalar/usar o `cheese` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `cheese` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `cheese` on `Linux Ubuntu`._


## Descrição [2]

### `cheese`

O `cheese` é uma aplicação simples e leve para captura de fotos e vídeos por meio da webcam em sistemas `Linux`. Com uma interface intuitiva, permite aos usuários tirar fotos ou gravar vídeos com facilidade, oferecendo recursos básicos de edição, como aplicação de efeitos e ajustes de brilho e contraste. É uma opção popular para quem precisa de uma solução rápida e fácil para usar a webcam em sistemas `Linux`.


## 1. Como configurar/instalar/usar o `cheese` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `cheese` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

Para instalar o programa `cheese`, que é um aplicativo de webcam, no `Linux Ubuntu` utilizando o `Terminal Emulator`, você pode seguir os passos abaixo:

3. **Instale o `Cheese`**: Após atualizar a lista de pacotes, você pode instalar o `Cheese` utilizando o seguinte comando: `sudo apt install cheese -y`

4. **Execute o Cheese**: Após a instalação, você pode iniciar o `Cheese` diretamente do Terminal digitando: `cheese`

    Você também pode encontrá-lo no menu de aplicações e iniciá-lo por lá.

### 2. Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `cheese` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean                                                            
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install cheese -y
    cheese
    ```


## 3. Identificar o caminho do dispotivo `webcam`

Para ter certeza do caminho do dispositivo de vídeo da sua `webcam` no `Linux`, você pode seguir estes passos no terminal:

1. Abra um terminal.

2. **Digite o comando a seguir e pressione `Enter`: `ls /dev/video*`

    Este comando vai listar todos os dispositivos de vídeo reconhecidos pelo sistema, geralmente as webcams são listadas como `/dev/video0`, `/dev/video1` etc.

3. **Instalar o `v4l2-utils`**: Faça isso com o comando: `sudo apt-get install v4l-utils`
    
    Se estiver usando uma distribuição baseada em `Debian` ou `Ubuntu`.

4. Se você tiver mais de um dispositivo listado e não tiver certeza de qual é a sua `webcam`, pode testar uma outra opção é usar o comando:  `v4l2-ctl --list-devices`

    Este comando que oferece uma listagem mais detalhada dos dispositivos de vídeo e associa cada um aos respectivos caminhos no `/dev`.Você pode precisar instalar a ferramenta `v4l-utils` para usar o `v4l2-ctl`.


## Referências

[1] OPENAI. ***Install Cheese on Ubuntu.*** Disponível em: <https://chat.openai.com/c/32c45417-de30-40ee-98cc-da1dd95cbf4c> (texto adaptado). Acessado em: 23/04/2023 17:11.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 23/04/2024 17:10.

