---
title: Gerenciamento de Arquivos
---
import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

Esta seção descreve como o **Phoenix Code** permite que você gerencie, organize e navegue por arquivos e pastas dentro de seus projetos.

---

## Árvore de Arquivos (File Tree)
A **Árvore de Arquivos** aparece na barra lateral e mostra a estrutura completa de pastas do projeto aberto. Ela lista todos os arquivos e pastas em uma visualização hierárquica.

![Árvore de Arquivos](./images/fileManagement/file-tree.png "Árvore de Arquivos")

### Menu de Contexto da Árvore de Arquivos
Quando você clica com o botão direito na Árvore de Arquivos, aparece um menu de contexto que permite realizar várias operações.

> Todas as operações de arquivos e pastas, como criar, renomear, excluir e muitas outras, são geralmente realizadas através deste menu de contexto.

O elemento no qual você clica com o botão direito na Árvore de Arquivos torna-se o contexto selecionado, o que significa que qualquer operação realizada será aplicada a esse item. Por exemplo:
- Clique com o botão direito em um **arquivo** → a ação se aplica a esse arquivo.
- Clique com o botão direito em uma **pasta** → a ação se aplica à pasta ou ao seu conteúdo (ex: adicionar arquivo, criar subpasta, excluir conteúdo).
- Clique com o botão direito em um **espaço vazio** → a ação se aplica ao diretório raiz do projeto.

> Na imagem abaixo, `index.html` está selecionado como o contexto. Qualquer ação do menu de contexto será aplicada a esse arquivo.

![Atalhos de Teclado da Árvore de Arquivos](./images/fileManagement/file-tree-context-menu-key-shortcut.png "Atalhos de Teclado da Árvore de Arquivos")

Você também pode atribuir ou atualizar atalhos de teclado para qualquer ação da Árvore de Arquivos através do menu de contexto, usando o botão de teclado ao lado. Veja o [Guia de Atalhos de Teclado](./Features/keyboard-shortcuts) para detalhes completos.

### Ordenando Arquivos e Pastas
Por padrão, a Árvore de Arquivos ordena primeiro as pastas (em ordem crescente *a-z*), seguidas pelos arquivos.

Para ordenar pastas e arquivos juntos:
1. Clique na **seta dupla** no canto superior direito da barra lateral.
2. No menu suspenso, desmarque **Ordenar Pastas Primeiro** (Sort Folders First).

![Ordenação de pastas na Árvore de Arquivos](./images/fileManagement/file-tree-sort-folders-option.png "Ordenação de pastas na Árvore de Arquivos")

Como alternativa, você pode controlar esse comportamento atualizando a propriedade `sortDirectoriesFirst` no arquivo de preferências. Veja [Editando Preferências](./editing-text#editing-preferences) para mais detalhes.

Agora, arquivos e pastas são ordenados juntos em uma única lista crescente.

![Árvore de arquivos ordenada](./images/fileManagement/file-tree-sorted.png "Árvore de arquivos ordenada")

> Observe como a pasta `images` agora aparece em ordem alfabética com outros itens.

### Recolher Todas as Pastas (Collapse All Folders)
O recurso **Recolher Todas as Pastas** ajuda você a redefinir rapidamente sua visualização, recolhendo todas as pastas expandidas para o nível raiz, deixando apenas os itens de nível superior visíveis na Árvore de Arquivos.

Para recolher todas as pastas:
1. Passe o mouse sobre o cabeçalho da Árvore de Arquivos no canto superior direito.
2. Clique no `ícone de recolher` (duas setas apontando uma para a outra) que aparece.

<VideoPlayer
  src="https://docs-images.phcode.dev/videos/file-management/collapse-folders.mp4"
/>

---

## Barra de Abas (Tab Bar)
A **Barra de Abas** aparece no topo do editor e exibe todos os arquivos abertos. Cada arquivo na Barra de Abas é chamado de **aba**, e você pode abrir quantas abas desejar.

*A Barra de Abas ajuda você a alternar rapidamente entre arquivos enquanto trabalha.*

![Barra de Abas](./images/fileManagement/tab-bar.png "Barra de Abas")

A aba ativa é destacada com um marcador **azul** para distingui-la das inativas. Para alternar entre abas, basta clicar na aba que deseja visualizar.

Para fechar uma aba, clique no botão `×` ao lado de seu nome. Para abas inativas, este botão aparece apenas quando você passa o mouse sobre elas.

O **Phoenix Code** mostra um pequeno ícone `•` nas abas que possuem alterações não salvas. Se você tentar fechar uma aba com alterações não salvas, o **Phoenix Code** exibirá um diálogo de confirmação com três opções:
* **Não Salvar**: Fecha a aba sem salvar as alterações. Todas as alterações não salvas serão perdidas.
* **Salvar**: Salva o arquivo e depois fecha a aba.
* **Cancelar**: Mantém a aba aberta e retorna à edição.

![Diálogo de Salvar Arquivo](./images/fileManagement/save-file-dialog.png "Diálogo de Salvar Arquivo")

Quando várias abas têm o mesmo nome de arquivo, o **Phoenix Code** exibe o nome da pasta pai para que você possa distingui-las facilmente.

> Passar o mouse sobre uma aba mostrará uma dica (tooltip) com seu caminho completo.

![Interface da Barra de Abas](./images/fileManagement/tab-bar-main.png "Interface da Barra de Abas")

> A imagem acima mostra vários elementos da interface de uma aba.

### Abas de Visualização (Preview Tabs)
Abas de Visualização são abas temporárias criadas quando você clica uma única vez em um arquivo na Árvore de Arquivos. Elas são úteis para navegação rápida sem poluir seu espaço de trabalho. As Abas de Visualização são visíveis apenas na Barra de Abas e não são adicionadas ao Conjunto de Trabalho (Working Set). Elas aparecem em *itálico* com um texto *cinza* mais claro.

![Aba de Visualização](./images/fileManagement/preview-tab.png "Aba de Visualização")

Uma aba de visualização torna-se uma aba permanente e é adicionada ao seu Conjunto de Trabalho quando você:
- Faz qualquer alteração no arquivo
- Clica na própria aba de visualização
- Salva o arquivo
- Clica duas vezes no arquivo na Árvore de Arquivos

Apenas uma aba de visualização pode existir por painel. Abrir outro arquivo substitui a aba de visualização atual, a menos que ela já tenha sido convertida em uma aba permanente.

> Clicar duas vezes em um arquivo pula a visualização e o abre como uma aba permanente imediatamente.

### Barra de Abas em Painéis Divididos
Quando vários painéis estão abertos, cada painel tem sua própria Barra de Abas e mantém sua própria lista de abas abertas. A aba ativa no **painel ativo** é marcada em **azul**, enquanto a aba ativa em um **painel inativo** aparece em **cinza**.

![Barra de Abas em Painéis Divididos](./images/fileManagement/split-panes-tabs.png "Barra de Abas em Painéis Divididos")

> Um arquivo pode aparecer como uma aba em mais de um painel.

### Abas Ocultas
Quando você abre um novo arquivo, sua aba é adicionada à direita das abas existentes. Se houver mais abas do que cabe na área visível, o **Phoenix Code** exibe um botão **Mostrar Abas Ocultas** (Show Hidden Tabs).

![Botão de mostrar abas ocultas](./images/fileManagement/overflow-button.png "Botão de mostrar abas ocultas")

Clicar neste botão abre uma lista suspensa de todas as abas que não estão totalmente visíveis. Desta lista, você pode selecionar uma aba para trazê-la à visualização ou fechar abas diretamente do menu suspenso.

### Arrastar e Soltar Abas
Você pode reordenar as abas arrastando-as e soltando-as. Enquanto arrasta, o **Phoenix Code** destaca a posição de soltura com um marcador azul vertical, mostrando exatamente onde a aba será colocada. As abas também podem ser arrastadas entre painéis.

### Menu de Contexto da Barra de Abas
Quando você clica com o botão direito em uma aba, aparece um menu de contexto com várias opções para trabalhar facilmente com as abas.

![Menu de contexto da barra de abas](./images/fileManagement/tab-bar-context-menu.png "Menu de contexto da barra de abas")

> Essas opções fornecem acesso rápido a operações de arquivos comuns diretamente da Barra de Abas.

### Git - Barra de Abas
A Barra de Abas exibe indicadores de status de arquivo do Git, mostrando quais arquivos não estão sendo rastreados (**untracked**) ou foram modificados (**modified**).

![Git na barra de abas](./images/fileManagement/tab-bar-git.png "Git na barra de abas")
- Um **marcador verde** indica um arquivo não rastreado (*untracked*).
- Um **marcador laranja** indica um arquivo modificado (*modified*).

Para arquivos que estão no `.gitignore`, o **Phoenix Code** mostra o nome da aba em *itálico cinza*.

> Esses indicadores aparecem apenas quando seu projeto é um repositório Git.

### Limitando o Número de Abas
O **Phoenix Code** permite que você controle o número máximo de abas exibidas na Barra de Abas de uma só vez. Por padrão, o valor é definido como `-1`, o que significa que todas as abas abertas são exibidas.

Por exemplo, se você quiser mostrar no máximo **3 abas** na Barra de Abas, você pode adicionar o seguinte às suas preferências:

```json
"tabBar.options": {
  "numberOfTabs": 3,
  "showTabBar": true
}
```

Você pode definir `numberOfTabs` para qualquer número positivo para definir o limite máximo de abas. Se definido como `0`, a Barra de Abas será totalmente ocultada. Qualquer valor negativo (como `-1`) exibe todas as abas abertas sem restrição.

> A aba ativa está sempre visível, exceto quando o valor `numberOfTabs` é definido como `0`.

### Mostrando ou Ocultando a Barra de Abas
Você pode ativar ou desativar a Barra de Abas de várias maneiras:

#### 1. Pelo Menu Ver
Vá em `Ver > Barra de Abas de Arquivos` (View > File Tab Bar) para alternar entre ativado ou desativado.

![Ver > Barra de Abas de Arquivos](./images/fileManagement/disable-tab-bar-1.png "Ver > Barra de Abas de Arquivos")

#### 2. Pela Barra Lateral
Clique no ícone de **seta dupla** no canto superior direito da barra lateral e use a opção **Mostrar Barra de Abas de Arquivos** no menu suspenso.

![Desativar Barra de Abas](./images/fileManagement/disable-tab-bar-2.png "Desativar Barra de Abas")

#### 3. Pelas Preferências
Você também pode alternar a Barra de Abas atualizando a opção `showTabBar` no arquivo de preferências.

```json
"tabBar.options": {
  "showTabBar": false
}
```

*Adicione isso em seu arquivo de preferências para ocultar a Barra de Abas.* Defina o valor como `true` para ativá-la. Veja [Editando Preferências](./editing-text#editing-preferences) se precisar de ajuda para editar as preferências.

---

## Arquivos de Trabalho (Working Files)
**Arquivos de Trabalho** (também chamado de **Working Tree**) fornece outra maneira de visualizar e gerenciar arquivos abertos. Ele aparece na barra lateral, acima da **Árvore de Arquivos**.

![Arquivos de Trabalho](./images/fileManagement/working-files.png "Arquivos de Trabalho")

Arquivos de Trabalho e a Barra de Abas são sincronizados, o que significa que qualquer operação realizada em um (fechar, reordenar, abrir arquivos, etc.) é automaticamente refletida no outro.

Arquivos de Trabalho exibe os mesmos elementos de interface que a Barra de Abas:
* Ícone `•` para arquivos não salvos
* Botão `×` para fechar arquivos
* Nomes de pastas pai quando vários arquivos têm o mesmo nome
* Tooltip mostrando o caminho completo do arquivo ao passar o mouse
* Indicadores de status do Git (verde para não rastreados, laranja para modificados e itálico cinza para arquivos ignorados pelo git)

> Veja a seção [Barra de Abas](#barra-de-abas) para explicações detalhadas desses recursos.

> **Nota**: Ao contrário da Barra de Abas, você não pode controlar o número máximo de arquivos exibidos nos Arquivos de Trabalho.

### Arquivos de Trabalho em Painéis Divididos
Ao usar painéis divididos, cada painel mantém sua própria lista de arquivos abertos nos Arquivos de Trabalho. Os painéis são rotulados com base na orientação da divisão:
* **Divisão Vertical**: **Esquerda** (primeiro painel) e **Direita** (segundo painel)
* **Divisão Horizontal**: **Topo** (primeiro painel) e **Base** (segundo painel)

![Arquivos de Trabalho em Painéis Divididos](./images/fileManagement/working-files-split-panes.png "Arquivos de Trabalho em Painéis Divididos")

### Arrastar e Soltar nos Arquivos de Trabalho
Você pode reordenar arquivos nos Arquivos de Trabalho arrastando-os e soltando-os, assim como na Barra de Abas.

### Menu de Contexto dos Arquivos de Trabalho
Quando você clica com o botão direito em um arquivo nos Arquivos de Trabalho, aparece um menu de contexto com várias operações de arquivo.

![Menu de contexto dos arquivos de trabalho](./images/fileManagement/working-files-context-menu.png "Menu de contexto dos arquivos de trabalho")

> Essas opções fornecem acesso rápido a operações de arquivos comuns diretamente dos Arquivos de Trabalho.

### Mostrando ou Ocultando Arquivos de Trabalho
Você pode mostrar ou ocultar o painel de Arquivos de Trabalho de duas maneiras:

#### 1. Pela Barra Lateral
Clique no ícone de **seta dupla** no canto superior direito da barra lateral e use a opção **Mostrar Arquivos de Trabalho** no menu suspenso.

![Desativar Arquivos de Trabalho](./images/fileManagement/disable-working-files.png "Desativar Arquivos de Trabalho")

#### 2. Pelas Preferências
Você também pode alternar os Arquivos de Trabalho atualizando a propriedade `showWorkingSet` no arquivo de preferências.

```json
"showWorkingSet": true
```

Defina o valor como `false` para ocultar os Arquivos de Trabalho. Veja [Editando Preferências](./editing-text#editing-preferences) se precisar de ajuda para editar as preferências.

---

## Arquivos Recentes (Recent Files)
O diálogo **Arquivos Recentes** fornece acesso rápido aos arquivos nos quais você trabalhou recentemente.

### Abrindo Arquivos Recentes
* **Aplicativo Desktop**: Pressione `Ctrl + R`.
* **Navegador**: Pressione `Ctrl + Alt + Shift + O` (pois `Ctrl + R` é reservado para recarregar o navegador).

Para personalizar o atalho de teclado, consulte o [Guia de Atalhos de Teclado](./Features/keyboard-shortcuts#changing-a-keyboard-shortcut).

![Diálogo de Arquivos Recentes](./images/fileManagement/recent-files.png "Caixa de Diálogo de Arquivos Recentes")

O diálogo mostra seus arquivos abertos recentemente. Arquivos fechados aparecem em cinza. Passe o mouse sobre eles para ver um ícone `x`. Clique nele para removê-los da lista. O botão `Limpar` (Clear) na parte inferior remove todos os arquivos fechados de uma vez.

> Arquivos atualmente abertos não podem ser removidos desta lista. Feche-os primeiro para removê-los.

Para ver o caminho completo de um arquivo, passe o mouse sobre ele ou verifique o canto inferior esquerdo do diálogo quando um arquivo estiver selecionado.

---

## Recuperação de Arquivo (File Recovery)
O **Phoenix Code** possui um recurso integrado de **Recuperação de Arquivo** para ajudar você a recuperar alterações não salvas após eventos inesperados, como falhas ou fechamentos acidentais.

### Recuperando Arquivos Após uma Falha
Quando você reabre o editor, se houver alterações não salvas da sessão anterior, uma caixa de diálogo aparecerá com duas opções: `Descartar` (Discard) e `Restaurar` (Restore).

![Caixa de Diálogo de Recuperação de Arquivo](./images/fileManagement/file-recovery.png "Caixa de Diálogo de Recuperação de Arquivo")

* **Restaurar**: Recupera seus arquivos não salvos reintegrando todas as alterações feitas antes do último salvamento.
* **Descartar**: Remove as alterações não salvas. *Isso excluirá os dados permanentemente.*
