---
title: Início Rápido de Projeto
---
import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

Esta seção fornece uma visão geral de como criar e gerenciar projetos usando o Diálogo de Início de Projeto no Phoenix Code.

## Diálogo de Início de Projeto (Start Project Dialog)
Quando você abre o aplicativo desktop ou a versão web do Phoenix Code, você é recebido pela caixa do `Diálogo de Início de Projeto`. Ela serve como um hub de acesso rápido, permitindo que você crie novos projetos, retome os recentes, importe do GitHub e muito mais.

![Imagem do Diálogo de Início de Projeto](images/quickStartProject/start-project-dialog.png "Diálogo de Início de Projeto")

> Você pode reabrir a caixa do Diálogo de Início de Projeto a qualquer momento clicando aqui.

![Imagem de Reabrir o Diálogo de Início de Projeto](images/quickStartProject/reopen-start-project-dialog.png "Imagem de Reabrir o Diálogo de Início de Projeto clicando no ícone da pasta")

Além disso, se preferir que o Diálogo de Início de Projeto não apareça toda vez que você abrir o Phoenix Code, siga estas etapas:
1. Clique no `ícone de pasta` no canto superior esquerdo para abrir o Diálogo de Início de Projeto ou, alternativamente, você pode reiniciar o Phoenix Code para que ele apareça automaticamente.
2. No canto inferior direito do diálogo, clique no `ícone de configurações`.
3. Desative a opção **`Mostrar Este Diálogo ao Iniciar`** (Show This Dialog on Startup).

<VideoPlayer
  src="https://docs-images.phcode.dev/videos/quick-start-project/turn-off-start-dialog.mp4"
/>

## Projeto Padrão (Default Project)
O Diálogo de Início de Projeto inclui uma opção para criar um Projeto Padrão. Quando selecionado, um projeto será gerado com alguns arquivos para fornecer um ponto de partida simples para testar e usar o editor Phoenix Code.

<VideoPlayer
  src="https://docs-images.phcode.dev/videos/quick-start-project/default-project.mp4"
/>

## Abrir Pasta (Open Folder)
Você pode abrir uma pasta do seu computador no Phoenix Code seguindo estas etapas:
1. Clique no botão **`Abrir Pasta`** (Open Folder) no Diálogo de Início de Projeto.
2. Navegue até a pasta do projeto desejada e selecione-a.
3. Uma vez selecionada, o Phoenix Code carregará todos os arquivos, permitindo que você comece a trabalhar imediatamente.

> O recurso **Abrir Pasta** não é suportado no navegador Firefox devido a restrições de acesso a pastas locais. Por favor, use Chrome, Edge ou Opera para trabalhar com pastas locais.

![Imagem de Abrir Pasta](images/quickStartProject/open-folder.png "Clique em Abrir Pasta para trabalhar com pastas locais")

## Criar um Projeto HTML
Você pode criar um novo projeto HTML que inclui arquivos essenciais seguindo estas etapas:
1. Abra o `Diálogo de Início de Projeto`.
2. Clique no botão **`HTML5`**. Isso abrirá uma nova página para seleção de pasta.
3. Forneça um nome para o projeto, escolha a pasta desejada e clique em **`Criar Projeto`** (Create Project).

Uma vez concluído, uma estrutura básica de projeto será gerada na pasta selecionada.

<VideoPlayer
  src="https://docs-images.phcode.dev/videos/quick-start-project/html-project.mp4"
/>

## Criar um projeto a partir do Github
> Atualmente, este recurso está disponível apenas na versão web. Em breve nos aplicativos desktop.

Você pode criar um projeto a partir do GitHub e importá-lo facilmente para sua máquina local. Siga estas etapas:
1. Abra o `Diálogo de Início de Projeto`.
2. Clique no botão **`GitHub Project`**.
3. Insira a URL do repositório GitHub em que deseja trabalhar.
4. Especifique o local da pasta onde deseja copiar os arquivos do repositório.
5. Clique em **`Criar Projeto`** (Create Project).

Após a criação do projeto, você terá todos os arquivos necessários em sua máquina local, prontos para o desenvolvimento.

## Projetos Recentes (Recent Projects)
No Diálogo de Início de Projeto, a seção **`Projetos Recentes`** exibe uma lista de todos os projetos nos quais você trabalhou recentemente.

> Para remover um projeto da lista de Projetos Recentes, clique no botão **X** ao lado do nome do projeto.

![Imagem de Projetos Recentes](images/quickStartProject/recent-projects.png "Projetos Recentes exibe a lista de projetos em que você trabalhou recentemente")

Se nenhum projeto recente estiver disponível, um vídeo do YouTube explicando as opções do diálogo de Início de Projeto será exibido no lugar.

![Imagem de Nenhum Projeto Recente](images/quickStartProject/start-project-dialog.png "Se não houver Projetos Recentes disponíveis, o link para um vídeo do YouTube será exibido")

## Opção Ver Mais (View More)
No Diálogo de Início de Projeto, o botão **`Ver Mais`** (View More) fornece acesso a uma seleção de modelos de página HTML pré-fabricados, como página inicial, página de blog e painel HTML.

Para usar esses modelos:
1. Clique no botão **`Ver Mais`**.
2. Uma nova página aparecerá, permitindo que você selecione a pasta onde deseja criar o projeto.
3. Clique em **`Criar Projeto`** (Create Project) para gerar o modelo escolhido.
