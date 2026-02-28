title: Snippets Personalizados

import React from 'react'; import VideoPlayer from '@site/src/components/Video/player';

Os **Snippets Personalizados** permitem que você crie suas próprias dicas de código reutilizáveis. Você pode definir abreviações curtas que se expandem em snippets de código completos quando selecionadas nas dicas de código que aparecem enquanto você digita. Na dica de código, o **Phoenix Code** exibe uma pequena etiqueta `Snippet` à direita, indicando que a dica vem de snippets personalizados.

![Ícone de Snippets Personalizados](images/CustomSnippets/custom-snippet-icon.png)

Você também pode especificar com quais tipos de arquivo cada snippet deve funcionar, para que eles apareçam apenas onde forem relevantes.

Além disso, você pode definir a posição do cursor dentro de um snippet. Após a expansão, o **Phoenix Code** coloca automaticamente seu cursor exatamente onde você deseja, permitindo que você comece a digitar imediatamente.

Os snippets que você define estão disponíveis globalmente, então você não precisa recriá-los para cada pasta.

> **Nota**: Os Snippets Personalizados têm a prioridade mais alta e aparecerão acima de todas as outras dicas de código.

### Painel de Snippets Personalizados

Você pode gerenciar todos os seus snippets a partir do painel de **Snippets Personalizados**. Para acessá-lo, navegue até `Arquivo` → `Snippets Personalizados...`.

![Item de Menu de Snippets Personalizados](images/CustomSnippets/custom-snippets-menu-item.png)

O painel aparece na parte inferior do editor.

![Painel de Snippets Personalizados](images/CustomSnippets/custom-snippets-empty-panel.png) Se você ainda não adicionou nenhum snippet, o painel estará vazio.

### Adicionar Snippet

Para adicionar um snippet, clique no botão `'+'` que aparece no cabeçalho do painel.

> Alternativamente, se o seu painel de snippets estiver vazio, o **Phoenix Code** mostra um botão grande `Adicionar Snippet` no próprio painel.

![Adicionar Snippet](images/CustomSnippets/add-snippet.png)

Clicar nele abre o painel **Adicionar Snippet**.

![Painel Adicionar Snippet](images/CustomSnippets/add-snippet-panel.png)

#### Entendendo o Painel Adicionar Snippet

O painel **Adicionar Snippet** contém quatro campos de entrada, cada um com exemplos de marcadores para guiá-lo:

| Campo | Descrição |
|---|---|
| **Abreviação** (obrigatório) | O texto de atalho que aciona seu snippet. Por exemplo, digitar `clg` poderia expandir para um bloco de código mais longo. |
| **Descrição** (opcional) | Uma breve explicação do que o snippet expande. Isso aparece na dica de código. Exemplo: atalho para console log. |
| **Extensão de Arquivo** (opcional) | Especifica em quais tipos de arquivo o snippet deve estar ativo. Por exemplo, `.js, .ts` tornará o snippet disponível em arquivos JavaScript e TypeScript. ⚠️ Use **extensões** de arquivo, não nomes de arquivos ou linguagens, e separe várias entradas com vírgulas. Quando deixado em branco, o snippet funciona para **todos** os tipos de arquivo. |
| **Texto do Modelo** (obrigatório) | O código real ou conteúdo que seu snippet expande. Por exemplo, digitar `clg` poderia expandir para `console.log();`. |

#### Exemplo de Snippet

A imagem abaixo mostra uma configuração de snippet completa:

![Exemplo de Snippet](images/CustomSnippets/custom-snippet-example.png) Após inserir os valores, clique em `Salvar`.

> Seu snippet será adicionado à lista e poderá ser usado imediatamente no **Phoenix Code**.

![Contagem de Snippets](images/CustomSnippets/custom-snippets-count.png) No cabeçalho do painel, você pode ver o número total de snippets que você adicionou. Você pode criar quantos snippets desejjar.

### Editar Snippet

Você pode editar um snippet existente sempre que precisar fazer alterações. Para editar um snippet, clique no snippet que deseja editar na lista de snippets. Isso abrirá o painel **Editar Snippet**.

![Editar Snippet](images/CustomSnippets/edit-snippet.png)

Atualize os campos que deseja modificar. Por exemplo, no snippet mostrado abaixo, atualizamos a **Abreviação** de `scr` para `script`. Após fazer suas alterações, clique em `Salvar`.

![Sucesso na Edição do Snippet](images/CustomSnippets/after-edit-snippet.png)

Você pode ver que o snippet agora está atualizado com a nova **Abreviação**.

### Excluir Snippet

Excluir um snippet é simples. Na lista de snippets, clique no ícone da Lixeira no lado direito do snippet que deseja remover. Isso excluirá imediatamente o snippet.

![Excluir Snippet](images/CustomSnippets/delete-snippet.png)

> ⚠️
> Cuidado: Excluir um snippet é permanente e não pode ser desfeito.

### Filtrar Snippets

Quando você tem uma grande coleção de snippets, o recurso de **Filtro** ajuda você a restringir rapidamente a lista. Você o encontrará no lado superior direito do painel de snippets.

![Filtrar Snippet](images/CustomSnippets/filter-snippet.png)

Você pode filtrar a lista por qualquer valor, como **Abreviação**, **Descrição**, **Extensão de Arquivo** ou **Texto do Modelo**.

### Posição do Cursor no Snippet

Os snippets personalizados do **Phoenix Code** também permitem definir **posições do cursor** dentro de um snippet para tornar a edição ainda mais rápida. Ao adicionar marcadores de cursor numerados, você pode pular entre pontos-chave no snippet expandido usando a tecla `Tab`.

#### Como Funciona

Dentro do **Texto do Modelo**, você pode incluir marcadores como `${1}`, `${2}`, `${3}`, e assim por diante. Quando o snippet se expande:

1. O cursor começa em `${1}`.
2. Depois de inserir o texto desejado, pressione `Tab` para mover para o próximo marcador.
3. Continue pressionando `Tab` para percorrer as posições numeradas.
4. O cursor finalmente para em `${0}`. Se `${0}` não estiver definido, ele para no **último marcador numerado**.

Aqui está um exemplo de um snippet com marcadores de cursor numerados:

![Posições do Cursor no Snippet](images/CustomSnippets/snippet-cursor.png)

> Para retroceder pelos marcadores, pressione `Shift + Tab`.

Depois de atingir a posição final do cursor, pressionar `Tab` novamente **removerá quaisquer marcadores não preenchidos restantes** do snippet expandido.

Perguntas Frequentes (FAQ)
---

#### P. Existe um limite máximo para o comprimento da abreviação?

Sim. O **Phoenix Code** define alguns limites para certos campos. A **Abreviação** pode ter no máximo 30 caracteres, e a **Descrição** pode ter até 80 caracteres. Não há restrição quanto ao comprimento do **Texto do Modelo** ou da **Extensão de Arquivo**.

#### P. O que acontece se houver dois snippets com a mesma abreviação?

O **Phoenix Code** não permite adicionar dois snippets com a mesma abreviação. No entanto, as abreviações diferenciam maiúsculas de minúsculas, portanto, variações como `log` e `LOG` são tratadas como snippets diferentes.

#### P. Preciso digitar a abreviação completa para que a dica do snippet apareça?

Sim. A dica do snippet aparece apenas quando você digita a abreviação completa. Esta é uma decisão de UX intencional, pois os snippets personalizados têm a prioridade mais alta; mostrar dicas para abreviações parciais poderia poluir as sugestões e ocultar as dicas padrão.
