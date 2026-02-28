---
title: Galeria de Imagens
---

import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

:::info Recurso Pro
[Faça o upgrade para o Phoenix Code Pro](https://phcode.io/pricing) para acessar este recurso.
:::

A **Galeria de Imagens** é um painel que aparece na parte inferior do Live Preview. Ela permite que você navegue por imagens de provedores on-line ou selecione imagens do seu dispositivo.

> A Galeria de Imagens está disponível apenas para elementos `img`.

Por padrão, a Galeria de Imagens aparece quando você seleciona um elemento `img`. Você pode fechá-la clicando no botão Galeria de Imagens na Caixa de Ferramentas ou no botão fechar na própria galeria. Para reabri-la, clique novamente no botão Galeria de Imagens.

![Galeria de Imagens](../images/image-gallery.png "Galeria de Imagens")

---

## Navegando por Imagens

Digite um termo de pesquisa na caixa de busca e pressione `Enter` ou clique no ícone de busca. A galeria exibirá as imagens correspondentes dos provedores. Use as setas para a esquerda e para a direita para navegar pelos resultados.

> A galeria lembra sua última consulta de pesquisa e a exibe quando você a reabre. Se não houver uma pesquisa anterior, o Phoenix Code mostrará resultados para uma consulta aleatória.

Passe o mouse sobre uma miniatura para visualizar a imagem em sua página. A imagem selecionada anteriormente é restaurada quando você move o cursor para fora da galeria.

Para selecionar uma imagem, clique na miniatura. Isso incorpora a imagem diretamente no seu código-fonte.
> Se o provedor de imagem não suportar a incorporação, clicar na miniatura fará o download da imagem.

Para baixar a imagem para o seu projeto, clique no botão **Download image**. O Phoenix Code baixa a imagem, salva-a na pasta selecionada e atualiza automaticamente o atributo `src`.

> Se esta for a primeira vez que você seleciona uma imagem, o Phoenix Code solicitará que você escolha uma pasta onde as imagens devem ser salvas. Consulte [Diálogo de Seleção de Pasta](#diálogo-de-seleção-de-pasta) para obter detalhes.

> As imagens são incorporadas ou baixadas no tamanho selecionado no momento. Consulte [Seleção de Tamanho de Imagem](#seleção-de-tamanho-de-imagem) para obter detalhes.

Abaixo de cada miniatura, o nome do fotógrafo e um link para seu perfil são exibidos.

<VideoPlayer
src="https://docs-images.phcode.dev/videos/live-preview-edit/image-gallery.mp4"
/>

---

## Selecionando do Dispositivo

Clique no botão **Select from device** no topo da galeria para escolher uma imagem dos seus arquivos locais.
Se nenhuma pasta tiver sido selecionada ainda, o Phoenix Code solicitará que você escolha onde a imagem deve ser salva.

![Selecionar do Dispositivo](../images/select-from-device.png "Selecionar do Dispositivo")

---

## Diálogo de Seleção de Pasta

A primeira vez que você seleciona uma imagem, o Phoenix Code solicita que você escolha onde as imagens devem ser salvas em seu projeto.

O diálogo inclui:
- **Entrada do caminho da pasta**: Digite o caminho de uma pasta relativo à raiz do seu projeto. O Phoenix Code sugere pastas correspondentes enquanto você digita.
- **Lembrar esta pasta para este projeto**: Quando marcado (padrão), o Phoenix Code reutiliza esta pasta para futuros downloads de imagens no mesmo projeto.

> Se a pasta não existir, o Phoenix Code a criará.
> Se o caminho da pasta for deixado em branco, as imagens serão salvas em uma pasta `images` na raiz do projeto.

![Diálogo de seleção de pasta](../images/folder-selection-dialog.png "Diálogo de Seleção de Pasta")

Para alterar a pasta salva posteriormente, clique no botão **Seleção de Pasta** (ícone de pasta) no cabeçalho da Galeria de Imagens.

![Botão de seleção de pasta](../images/folder-selection-button.png "Botão de Seleção de Pasta")

---

## Seleção de Tamanho de Imagem

A Galeria de Imagens inclui um **Seletor de Tamanho** que permite escolher a resolução da imagem antes de incorporá-la ou baixá-la.
Passar o mouse sobre uma miniatura exibe o tamanho estimado do arquivo no canto superior direito.
> Resoluções mais altas produzem arquivos de imagem maiores. O tamanho padrão é Standard (1080px).
