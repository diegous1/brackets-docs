---
title: Modo de Edição do Live Preview
---

import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

:::info Recurso Pro
[Faça o upgrade para o Phoenix Code Pro](https://phcode.io/pricing) para acessar este recurso.
:::

O **Modo de Edição** permite que você modifique sua página diretamente no Live Preview. Você pode editar textos, reorganizar elementos e atualizar imagens e links. Também é possível duplicar, excluir e inspecionar elementos com medições precisas.
O **Phoenix Code** atualiza seu código-fonte automaticamente à medida que você faz as alterações.

<VideoPlayer
src="https://docs-images.phcode.dev/videos/live-preview-edit/live-preview-edit.mp4"
/>

---

## Ativando o Modo de Edição

Para alternar para o Modo de Edição, clique no **menu suspenso do seletor de modo** na barra de ferramentas do Live Preview e selecione **Edit Mode**.

![Modo de Edição do Live Preview](../images/lp-mode.png "Modo de Edição do Live Preview")

Como alternativa, você pode alternar para o Modo de Edição atualizando a configuração `livePreviewMode` no arquivo de preferências. Consulte [Editando Preferências](../editing-text#editing-preferences) para aprender como editar o arquivo de preferências.

---

## Caixa de Informações (Info Box)

A **Caixa de Informações** exibe informações sobre um elemento.
> Por padrão, a Caixa de Informações aparece quando você passa o mouse sobre um elemento no Live Preview, mas esse comportamento pode ser alterado. Consulte a seção [Inspecionar Elemento ao Passar o Mouse](#inspecionar-elemento-ao-passar-o-mouse) para obter mais detalhes.

![Caixa de Informações](../images/info-box.png "Caixa de Informações")

A Caixa de Informações exibe:
- **Nome da tag e dimensões**: O tipo do elemento (por exemplo, `div`, `p`, `img`) e seu tamanho em pixels (largura × altura)
- **ID**: O atributo ID do elemento (se presente), mostrado com um prefixo `#`
- **Classes CSS**: As classes do elemento, mostradas com um prefixo `.`. Se o elemento tiver mais de três classes, apenas as três primeiras serão exibidas, seguidas por um indicador "+N more"
- **URL do link**: O atributo `href` do elemento (se presente). Isso é mostrado apenas para elementos de âncora (`<a>`)

#### Indicadores Visuais

A Caixa de Informações normalmente tem um fundo **azul** para elementos HTML padrão (por exemplo, `div`, `p`, `img`). Para elementos criados dinamicamente (renderizados por JavaScript), ela aparece com um fundo **cinza**, indicando que esses elementos não podem ser editados.

![Caixa de Informações não editável](../images/info-box-gray.png "Caixa de Informações não editável")

---

## Caixa de Ferramentas (Tool Box)

A **Caixa de Ferramentas** exibe um conjunto de ferramentas que você pode usar para modificar elementos no Live Preview.
> A Caixa de Ferramentas aparece apenas quando você clica em um elemento ou o seleciona através do código-fonte.

![Caixa de Ferramentas](../images/tool-box.png "Caixa de Ferramentas")

### Opções da Caixa de Ferramentas

A Caixa de Ferramentas exibe diferentes opções dependendo do tipo de elemento selecionado. Alguns botões estão disponíveis para todos os elementos, enquanto outros são específicos para certos tipos de elementos.

- **Selecionar Pai** (ícone de seta para cima): Seleciona o elemento pai do elemento atualmente selecionado.
  *Este botão aparece apenas quando existe um pai válido (não é mostrado quando o pai é `body`, `html` ou um elemento renderizado por JavaScript).*

- **Editar Texto** (ícone de caneta): Abre a edição de texto in-line para o elemento selecionado. Você pode editar o texto diretamente no Live Preview, e o Phoenix Code atualiza automaticamente o código-fonte.
  *Este botão aparece apenas para elementos que podem conter texto (não está disponível para `img`, `video`, `br`, etc.).*
  Consulte a seção [Edição de Texto In-line](#edição-de-texto-in-line) para mais detalhes.

- **Editar Hiperlink** (ícone de link): Abre uma caixa de entrada flutuante que permite editar o atributo `href` do elemento.
  *Este botão aparece apenas para elementos `<a>`.*
  Consulte a seção [Editar Hiperlink](#editar-hiperlink) para mais detalhes.

- **Galeria de Imagens** (ícone de imagem): Abre uma galeria de imagens na parte inferior do Live Preview, onde você pode navegar e selecionar uma imagem. Você também pode escolher uma imagem do seu computador. O Phoenix Code salva automaticamente a imagem na pasta do seu projeto e atualiza o atributo src do elemento.
  *Este botão aparece apenas para elementos `img`.*
  Consulte [Galeria de Imagens](./02-image-gallery.md) para mais detalhes.

- **Duplicar** (ícone de cópia): Copia o elemento selecionado e o coloca abaixo. Você também pode duplicar elementos usando `Ctrl/Cmd + D` após clicar em um elemento.
  *Esta opção está disponível para todos os elementos.*

- **Excluir** (ícone de lixeira): Exclui o elemento selecionado. Você também pode excluir elementos usando as teclas `Delete` ou `Backspace` após clicar em um elemento.
  *Esta opção está disponível para todos os elementos.*

---

## Edição de Texto In-line

A Edição de Texto In-line permite que você edite o conteúdo de texto dos elementos diretamente no Live Preview.

Para editar o texto:
1. Clique em um elemento para selecioná-lo.
2. Clique no ícone de **Editar Texto** (caneta) na Caixa de Ferramentas.
3. O elemento se tornará editável, permitindo que você digite ou modifique o texto.
4. Clique fora do elemento ou pressione `Esc` para concluir a edição.

O Phoenix Code atualizará o código-fonte em tempo real enquanto você digita.

---

## Editar Hiperlink

A ferramenta Editar Hiperlink permite que você modifique o atributo `href` de elementos de âncora (`<a>`).

Para editar um link:
1. Clique em um elemento de link (`<a>`) para selecioná-lo.
2. Clique no ícone de **Editar Hiperlink** (link) na Caixa de Ferramentas.
3. Uma caixa de entrada flutuante aparecerá. Digite a nova URL ou caminho.
4. Pressione `Enter` para salvar a alteração ou `Esc` para cancelar.

---

## Inspecionar Elemento ao Passar o Mouse

Por padrão, a Caixa de Informações e uma sobreposição de destaque aparecem quando você passa o mouse sobre os elementos no Live Preview. Você pode alterar esse comportamento no **menu suspenso do seletor de modo**.

- **Inspecionar ao Passar o Mouse (Inspect on Hover)**: Mostra a Caixa de Informações e a sobreposição de destaque ao passar o mouse.
- **Clicar para Inspecionar (Click to Inspect)**: Mostra a Caixa de Informações e a sobreposição de destaque apenas quando você clica em um elemento.

---

## Medições Precisas

Quando um elemento é selecionado no Modo de Edição, o Phoenix Code exibe medições precisas e o espaçamento ao redor dele. Isso ajuda você a visualizar o layout e o alinhamento dos elementos.

- **Padding**: Mostrado em **verde**.
- **Margem**: Mostrada em **laranja**.
- **Dimensões**: Mostradas em **azul** (para largura e altura).

Passar o mouse sobre outros elementos enquanto um estiver selecionado mostrará a distância entre eles.
