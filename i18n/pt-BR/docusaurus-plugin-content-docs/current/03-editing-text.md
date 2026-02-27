---
title: Editando Texto
---
import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

Esta seção fornece uma visão geral dos principais recursos de edição de texto e código no **Phoenix Code**.

---

## Multi Cursor

Usando o **Multi-Cursor**, você pode colocar vários cursores em diferentes locais, permitindo editar texto simultaneamente. Este recurso é especialmente útil para fazer alterações rápidas e consistentes em várias linhas ou seções de um arquivo.

### Criando múltiplos cursores

#### **Usando o Mouse** :
Mantenha pressionada a tecla `Alt` no Windows/Linux (`Option` no macOS) e `Clique` nos locais desejados para colocar cursores adicionais. Para colocar cursores rapidamente em várias linhas, arraste o mouse enquanto segura a mesma tecla.
<VideoPlayer
  src="https://docs-images.phcode.dev/videos/editing-text/multi_cursor.mp4"
  winLinuxTitle="Multi Cursors: Alt + Click"
  macTitle="Multi Cursors: Option + Click"
/>

#### **Usando o Teclado** :
Se você quiser que o cursor seja colocado na linha acima, use `Alt + Shift + Seta para Cima` no Windows/Linux e `Option + Shift + Seta para Cima` no MacOS. Se você quiser que o cursor seja colocado na linha abaixo, use `Alt + Shift + Seta para Baixo` no Windows/Linux e `Option + Shift + Seta para Baixo` no MacOS.

### Voltando para cursor único
Para voltar a um cursor único, basta pressionar a tecla `Esc`.

---

## Snippets Personalizados
Com **Snippets Personalizados**, você pode definir suas próprias dicas de código personalizadas. Você pode escrever abreviações curtas que, quando digitadas no editor, expandem-se para blocos de código completos ao serem selecionadas.

[Leia Mais](./Features/custom-snippets)

---

## Edição Rápida (Quick Edit)
Com a **Edição Rápida**, você pode editar seu arquivo CSS diretamente dentro de arquivos HTML.

[Leia Mais](./Features/quick-edit)

---

## Documentação Rápida (Quick Docs)
O **Quick Docs** fornece acesso imediato à documentação para elementos de código diretamente dentro do editor.

### Acessando o Quick Docs
1. Clique com o botão direito no elemento sobre o qual você deseja detalhes.
2. Um menu de contexto aparecerá, clique em **Quick Docs** ou simplesmente pressione `F1` para abrir o Quick Docs diretamente.

![Imagem do Quick Docs](images/editingText/quick-docs.png "Clique com o botão direito no elemento e selecione a opção Quick Docs")

---

## Localizar em Arquivos
Com o **Localizar em Arquivos**, você pode pesquisar por um texto específico em vários arquivos dentro de um projeto.

[Leia Mais](./Features/find-in-files)

---

## Renomeação Automática de Tag (Auto Rename Tag)
O recurso **Auto Rename Tag** atualiza as tags correspondentes automaticamente quando você renomeia uma delas. Funciona com arquivos HTML, XHTML, HTM, XML, SVG, PHP e JSP.

### Como Funciona
Quando você renomeia uma tag de abertura ou fechamento, a tag correspondente é atualizada instantaneamente.

### Ativando/Desativando o recurso Auto Rename Tag

#### Alternar o Recurso
Para ativar ou desativar o recurso **Auto Rename Tag**, vá em `Editar` > `Renomear Tags HTML Automaticamente`.

![Imagem de Desativar Auto Rename Tag](images/editingText/auto-rename-tag.png "Clique em Editar e alterne a opção Renomear Tags HTML Automaticamente")

*O recurso **Renomear Tags HTML Automaticamente** vem ativado por padrão.*

#### Desativação Temporária
Para desativar temporariamente a sincronização de tags para a tag atual:
Pressione `ESC`.
Para reativar a sincronização: Mova seu cursor para fora da tag e depois de volta para dentro da tag.

---

## Emmet
Com o **Emmet**, você pode escrever HTML e CSS mais rápido usando abreviações curtas. Se uma abreviação for compatível com Emmet, o Phoenix Code Editor mostra dicas de código e as expande em estruturas de código completas quando selecionadas.

[Leia Mais](./Features/emmet)

---

## Ajustes de Zoom e Tamanho da Fonte
As opções de **Zoom da UI e Fontes** permitem que você ajuste a escala geral da interface e o tamanho da fonte.

### Zoom da UI
**Mais Zoom** :- Amplia a interface geral, tornando todos os elementos maiores.
**Menos Zoom** :- Reduz a interface geral, tornando todos os elementos menores.

### Ajuste do Tamanho da Fonte
**Aumentar Tamanho da Fonte** :- Amplia o texto no editor sem afetar outros elementos da interface.
**Diminuir Tamanho da Fonte** :- Reduz o tamanho do texto no editor sem afetar outros elementos da interface.
**Restaurar Tamanho da Fonte** :- Redefine o texto do editor para seu tamanho padrão.

### Usando as Opções de Zoom da UI e Fontes

#### Usando o Menu
![Imagem de Zoom](images/editingText/zoom.png "Clique em Ver e passe o mouse sobre Zoom da UI e Fontes")
1. Clique em "Ver" na barra de menu.
2. Passe o mouse sobre "Zoom da UI e Fontes".
3. Selecione a opção desejada no submenu.

#### Usando Atalhos de Teclado
* **Mais Zoom**: `Ctrl + +` (`Cmd + +` no MacOs)
* **Menos Zoom**: `Ctrl + -` (`Cmd + -` no MacOs)
* **Aumentar Tamanho da Fonte**: `Ctrl + Shift + +` (`Cmd + Shift + +` no MacOs)
* **Diminuir Tamanho da Fonte**: `Ctrl + Shift + -` (`Cmd + Shift + -` no MacOs)
* **Restaurar Tamanho da Fonte**: `Ctrl + Shift + (` (`Cmd + Shift + (` no MacOs)

*Nota :- O nível de zoom atual é exibido ao lado da opção **Mais Zoom**.*

---

## Altura da Linha (Line Height)
O recurso de **Altura da Linha** permite personalizar o espaçamento vertical entre as linhas de texto no editor.

### Ajustando a Altura da Linha
Para ajustar a altura da linha:
1. Clique em `Ver` na barra de menu.
2. Navegue até a opção `Temas...`.
3. Use o controle deslizante de Altura da Linha para definir um valor entre 1 e 3. O padrão é 1.5.

![Altura da Linha](./images/editingText/line-height.png "Vá em Ver > Temas... para ajustar a altura da linha")

Os ajustes são aplicados instantaneamente, atualizando o editor dinamicamente.

### Modificando a Altura da Linha via Preferências
Você também pode modificar a altura da linha atualizando a propriedade `themes.editorLineHeight` no arquivo de preferências.

[Clique Aqui](#editando-preferencias) para ler sobre como editar as preferências.

---

## Linhas de Guia de Indentação
![Imagem de Linhas de Guia de Indentação](images/editingText/indent-display.png "As linhas verticais são Linhas de Guia de Indentação")

**Linhas de Guia de Indentação** são linhas verticais que ajudam a alinhar visualmente blocos de código e indicam níveis de indentação. Elas auxiliam na compreensão da hierarquia do código e estruturas aninhadas, melhorando a legibilidade geral.

### Ativando/Desativando Linhas de Guia de Indentação
![Imagem de Ativar Linhas de Guia de Indentação](images/editingText/indent-lines.png "Clique no menu Ver e alterne a opção Linhas de Guia de Indentação")
Para ativar ou desativar as Linhas de Guia de Indentação, vá em `Ver > Linhas de Guia de Indentação`.

### Preferências do Editor para Guias de Indentação
Você pode personalizar o comportamento das guias de indentação nas preferências do editor com as seguintes opções:

[Clique aqui](#editando-preferencias) para ler sobre como editar as preferências.

**editor.indentGuides**: Defina como `true` para exibir linhas de guia de indentação; defina como `false` para ocultá-las.
**editor.indentHideFirst**: Defina como `true` para ocultar a primeira linha de guia de indentação; defina como `false` para exibi-la.

---

## Codificação de Arquivo (File Encoding)
A **Codificação de arquivo** é o método usado para representar texto em um arquivo, convertendo caracteres em bytes. Precisamos dela para garantir que o texto seja exibido corretamente em diferentes plataformas e para lidar com caracteres ou símbolos especiais. O Phoenix Code Editor suporta vários formatos de codificação de arquivo.

*`UTF-8`* é o formato de codificação padrão no Phoenix.

### Definir Codificação de um arquivo
1. Clique no botão `utf8` na barra de status. (UTF-8 representa o formato de codificação padrão).
2. Uma lista de formatos de codificação disponíveis aparecerá. Selecione o formato desejado ou comece a digitar para filtrar e encontrar opções correspondentes no menu suspenso.

![Imagem de Codificação de Arquivo](images/editingText/file-encoding.png "Clique no botão utf8 na barra de status e selecione o formato de codificação")

---

## Associações de Tipo de Arquivo
**Associações de Tipo de Arquivo** *(Associar um tipo de arquivo a uma linguagem)* permitem que o Phoenix Code Editor forneça recursos específicos da linguagem, como realce de sintaxe, preenchimento de código e verificação de erros, com base na extensão do arquivo. Isso garante que seus arquivos sejam tratados de acordo com sua linguagem de programação ou marcação pretendida.

*Quando você cria um novo arquivo, se a extensão do arquivo for reconhecida, ele será associado à linguagem padrão. Se a extensão for desconhecida, um arquivo de texto genérico será aberto.*

### Associar um novo tipo de arquivo a uma linguagem
Para associar um novo tipo de arquivo a uma linguagem específica no Phoenix Code Editor, use o botão suspenso de Linguagem na barra de status. Por exemplo, se você quiser que arquivos com extensão `.myjs` sejam tratados como arquivos JavaScript, siga estas etapas:

1. Crie um novo arquivo com a extensão desejada. Para nosso exemplo, criamos (newfile.myjs). Por padrão, ele será associado a um arquivo de Texto.
2. Clique no botão `Texto` na barra de status.
3. Uma lista de todas as linguagens suportadas aparecerá. Selecione a linguagem que deseja associar ao tipo de arquivo. Para nosso exemplo, selecionamos `JavaScript`.

![Imagem de Associação de Arquivo](images/editingText/file-association.png "Clique no botão Texto na barra de status e selecione a linguagem")

4. No topo da caixa pop-up, você encontrará uma opção rotulada `Definir como padrão para arquivos .myjs`. Clique nela.
Agora, arquivos com extensão `.myjs` serão tratados como arquivos JavaScript.

---

## Embelezar Código (Beautify Code)
Com o **Embelezar Código**, você pode formatar seu código para seguir regras de estilo consistentes, melhorando a legibilidade e facilitando a manutenção.

[Leia Mais](./Features/beautify-code)

---

## Modo de Inserção e Sobrescrita
Os usuários podem alternar entre o **Modo de Inserção** e o **Modo de Sobrescrita** para diferentes comportamentos de entrada de texto.

*O Modo de Inserção é ativado por padrão quando você começa a digitar em um arquivo.*

### Entendendo o Modo de Inserção
Quando no **Modo de Inserção**, qualquer texto que você digitar é inserido na posição atual do cursor, empurrando o texto existente para a direita.

### Entendendo o Modo de Sobrescrita
O **Modo de Sobrescrita** substitui o texto existente na posição do cursor pelo novo texto que você digitar. Em vez de empurrar o texto para a direita, ele sobrescreve os caracteres diretamente sob o cursor.

### Alternar entre Modo de Inserção e Modo de Sobrescrita

#### **Usando a Interface do Editor**
Clique no botão `INS(OVR)` na barra de status para alternar entre Modo de Inserção e Modo de Sobrescrita.
`INS` representa Modo de Inserção.
`OVR` representa Modo de Sobrescrita.

![Imagem do Modo Inserção/Sobrescrita](images/editingText/toggle-ins-ovr.png "Clique no botão INS/OVR na barra de status para alternar entre os modos Inserção e Sobrescrita")

#### **Usando o Teclado**
Pressione a tecla `Ins` ou a tecla Insert para alternar entre Modo de Inserção e Modo de Sobrescrita.

---

## Detecção Automática de Espaço
O recurso de **Detecção Automática de Espaço** no Phoenix Code Editor foi projetado para detectar e adaptar-se automaticamente ao estilo de indentação usado em seus arquivos, sejam eles tabs ou espaços.

### Modos Automático e Fixo
* **Modo Auto**: Detecta e aplica automaticamente o estilo de indentação (tabs ou espaços) com base no código existente no arquivo.
* **Modo Fixo**: Bloqueia o editor para usar um estilo de indentação específico, independentemente da formatação existente no arquivo.

### Alternar entre Modo Auto e Modo Fixo
Quando você abre um novo arquivo, por padrão ele é definido para o modo `Auto`, mas você pode alternar facilmente para o modo `Fixo`.
Na barra de status do editor, você encontrará o botão `Auto`. Quando clicado, ele alterna entre os modos `Auto` e `Fixo`.
Você pode alternar entre espaços e tamanho de tabulação clicando no botão `Tamanho da Tabulação` ou `Espaços` na barra de status. Você pode ajustar a largura do tamanho da tabulação ou o número de espaços clicando no valor na barra de status e modificando-o conforme necessário.

![Imagem de Detecção Automática de Espaço](images/editingText/auto-spacing.png "O modo Auto detecta e adapta-se automaticamente ao estilo de indentação")

### Dicas Rápidas
* Se precisar recomputar a configuração de espaçamento de tabulação para um arquivo, clique no botão `Auto` duas vezes (mude para o modo Fixo e volte para Auto). Isso atualizará as configurações de espaçamento para o arquivo atual.
* Mudar para o modo `Fixo` aplicará um espaçamento fixo em todo o sistema.
* Você pode usar o recurso `Embelezar Código` para reformatar o arquivo de acordo com o novo tamanho de tabulação ou configurações de espaçamento após fazer as alterações (use `Ctrl-B` no Windows/Linux, `Cmd-B` no macOS ou `clique com o botão direito` e selecione `Embelezar Código`).

---

## Modo Sem Distrações
O **Modo Sem Distrações** ajuda você a se concentrar minimizando a poluição visual e ocultando elementos não essenciais da interface, criando um ambiente de edição limpo e minimalista.

### Ativando o Modo Sem Distrações

#### **Usando a Interface do Editor** :
Alterne entre o modo `Sem Distrações` e o modo `Normal` através da opção `Ver > Menu`.

![Imagem do Modo Sem Distrações](images/editingText/no-distractions.png "Clique na aba Ver na barra de menu e selecione Sem Distrações")

#### **Usando o Teclado** :
Pressione `Shift + F11` para alternar entre o modo `Sem Distrações` e o modo `Normal`.

---

## Editando Preferências
Você pode personalizar o Phoenix para se adequar ao seu fluxo de trabalho ajustando as preferências.

### Abrir o Arquivo de Preferências:
![Imagem de Abrir Arquivo de Preferências](images/editingText/preferences.png "Clique em Arquivo e depois em Abrir Arquivo de Preferências")
Para modificar as preferências, vá em `Arquivo` > `Abrir Arquivo de Preferências`.

### Entendendo o Layout das Preferências
Uma vez selecionado, dois arquivos aparecerão lado a lado:
* defaultPreferences.json (à esquerda) :- Este arquivo é apenas para leitura e contém as configurações padrão.
* phcode.json (à direita) :- Este arquivo é editável e usado para quaisquer preferências personalizadas que você deseje aplicar.

### Modificando Preferências
![Imagem de Modificar Preferências](images/editingText/modify-preferences.png "Modifique o arquivo phcode.json para atualizar as configurações de preferências")
Para alterar uma preferência, basta escrever a configuração e os valores desejados no **phcode.json** e salvar o arquivo. Essas configurações personalizadas substituirão automaticamente os valores correspondentes nas preferências padrão.
---
