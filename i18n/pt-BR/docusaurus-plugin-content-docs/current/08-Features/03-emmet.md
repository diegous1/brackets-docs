---
title: Emmet
---

import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

O **Emmet** ajuda você a expandir rapidamente abreviações curtas em blocos de código completos. Quando você digita uma abreviação compatível com o Emmet, o **Phoenix Code** exibe uma dica de código com o texto da abreviação e um pequeno ícone `Emmet` à direita, indicando que a dica vem do Emmet. Selecionar a dica a expande em um trecho de código completo.

O **Phoenix Code** inclui posicionamento inteligente do cursor. Após expandir uma abreviação do Emmet, ele coloca automaticamente o cursor na posição mais relevante para que você possa começar a digitar imediatamente. Ele também ajusta a indentação do código expandido automaticamente.

> Veja a [folha de dicas completa de abreviações do Emmet](https://docs.emmet.io/cheat-sheet/).

### Emmet em Linguagens de Marcação

O **Emmet** funciona em arquivos **HTML**, **PHP** ou similares a HTML, como **JSP**. **Exemplos:**

* `ul>li*2` expande para:
  ```html
  <ul>
    <li></li>
    <li></li>
  </ul>
  ```
* `!` expande para:
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>

  </body>
  </html>
  ```

> Consulte [este link](https://docs.emmet.io/abbreviations/) para ler mais sobre abreviações do Emmet para linguagens de marcação.

**Referência Visual**

<VideoPlayer src="https://github.com/phcode-dev/phoenix/assets/5336369/11b65e90-c0ec-4811-9e8a-096735529124" />

### Emmet em Linguagens de Folha de Estilo

O **Emmet** também funciona em folhas de estilo (**CSS**, **SCSS**, **Less**). Em folhas de estilo, o ícone do Emmet funciona como um link clicável que abre a documentação correspondente da MDN para essa propriedade (se disponível). ![Link MDN do Emmet](images/Emmet/emmet-link-mdn.png)

**Exemplos:**

* `bgc` expande para:
  ```css
  background-color: ;
  ```
* `mt10` expande para:
  ```css
  margin-top: 10px;
  ```

> Consulte [este link](https://docs.emmet.io/css-abbreviations/) para ler mais sobre abreviações do Emmet para folhas de estilo.

**Referência Visual**

<VideoPlayer src="https://github.com/phcode-dev/phoenix/assets/5336369/b7e08960-9195-4678-b118-e39f72740266" />

### Habilitando/Desabilitando o Emmet

Para habilitar ou desabilitar o recurso **Emmet**, vá em `Editar` > `Emmet`.

![Alternar recurso Emmet](images/Emmet/toggle-emmet.png)

Você também pode alternar o Emmet atualizando a propriedade `emmet` no arquivo de preferências. Veja [Editando Preferências](../03-editing-text.md#editing-preferences) para mais detalhes.

---

## FAQ

#### P. O que acontece se eu tentar expandir uma abreviação muito grande?

O **Phoenix Code** suporta grandes expansões do Emmet, mas aplica limites para manter o aplicativo estável.

* **Contagem máxima de repetições:** 400
Exemplo: `ul>li*10000` cria no máximo **400** elementos `li`.

* **Expansão máxima de palavras:** 100.000 palavras
Exemplo: O **Phoenix Code** define um limite de **100.000** palavras. A dica não aparecerá se a abreviação exceder este limite. `lorem100000` funciona, mas `lorem100001` não.
