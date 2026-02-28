title: Embelezar Código

import React from 'react'; import VideoPlayer from '@site/src/components/Video/player';

O recurso **Embelezar Código** garante que seu código seja formatado consistentemente, melhorando a legibilidade e a manutenibilidade. Ele alinha automaticamente seu código com seu estilo preferido, levando em conta a indentação, o espaçamento e outras regras de formatação.

Como Usar
----------

Você pode formatar seu código usando o Embelezar Código através dos seguintes métodos:

### Menu de Contexto :

* Clique com o botão direito no editor.
* Selecione **Embelezar Código** no menu de contexto.

![Imagem do Menu de Contexto do Embelezar Código](images/beautifyCode/Context-Menu.png "Clique na opção Embelezar Código")

### Atalho de Teclado :

* Pressione `Ctrl+B` para formatar seu código. (`Cmd+B` no MacOS)

**Nota**: Você também pode formatar apenas uma parte selecionada do seu código usando o recurso Embelezar Código. No entanto, esta opção só funcionará se o código selecionado for sintaticamente válido.

Formatação Automática ao Salvar
-------------------------------

Para formatar seu código automaticamente toda vez que você salvar:

1. Vá em `Editar` > `Embelezar Código Após Salvar`.
2. Ative esta opção.

![Imagem de Embelezar Código após Salvar](images/beautifyCode/Beautify-Code-after-save.png)

Personalizando o Embelezar Código
---------------------------------

Você pode ajustar as configurações do Embelezar Código para corresponder às suas preferências de codificação:

1. Vá em `Arquivo` > `Abrir Arquivo de Preferências`. Quando você abrir as preferências, dois arquivos aparecerão:
   * **defaultPreferences.json** no painel esquerdo: Este arquivo contém as configurações padrão e não é editável.
   * **phcode.json** no painel direito: Este é o arquivo que você deve editar para personalizar suas configurações.

2. Procure pela seção chamada `beautify.options`.

```json
{
  "beautify.options": {
    "bracketSameLine": true,
    "printWidth": 120,
    "proseWrap": "preserve",
    "quoteProps": "as-needed",
    "semi": true,
    "singleAttributePerLine": false,
    "singleQuote": false,
    "trailingComma": "none"
  }
}
```

3. Modifique as opções conforme necessário para controlar aspectos como:

* **bracketSameLine** :- Esta opção controla o posicionamento do colchete de fechamento `>` em elementos HTML, JSX, Vue ou Angular de várias linhas. Quando definida como `false`, o colchete de fechamento é colocado em sua própria linha. Definir esta opção como `true` posiciona o colchete de fechamento no final da última linha, alinhando-o com o conteúdo para um formato mais compacto e legível, mas isso não se aplica a elementos de fechamento automático.

O valor padrão de `bracketSameLine` é `true`.

Quando definido como True: ![Imagem de Bracket Same Line](images/beautifyCode/bracketSameLine-true.png)

Quando definido como False: ![Imagem de Bracket Same Line](images/beautifyCode/bracketSameLine-false.png)

---

* **printWidth**: Define o comprimento máximo da linha para a formatação do código. O embelezador quebrará as linhas que excederem o número de caracteres especificado pelo valor `printWidth`.

O valor padrão de `printWidth` é `120`.

* **proseWrap**: Determina como o texto em arquivos Markdown é quebrado. Os diferentes valores de `proseWrap` são:
  * **"always"**: Quebra automaticamente a prosa para caber dentro do `printWidth`, independentemente da formatação original.
  * **"never"**: Evita qualquer quebra automática, mantendo a prosa como está, mesmo que exceda o `printWidth`.
  * **"preserve"**: Mantém a formatação original da prosa, quebrando o texto apenas onde as quebras de linha já estão presentes.

O valor padrão de `proseWrap` é `preserve`.

* **quoteProps**: Determina quando as propriedades em objetos devem ser citadas:
  * **"as-needed"**: Cita propriedades apenas quando necessário, como quando um nome de propriedade contém caracteres especiais ou conflita com palavras-chave reservadas.
  * **"consistent"**: Cita todas as propriedades de forma consistente com base no estilo de citação da primeira propriedade. Se a primeira propriedade for citada, todas as propriedades serão citadas e vice-versa.
  * **"preserve"**: Mantém o estilo de citação existente das propriedades, deixando-as citadas ou não como estão no código original.

O valor padrão de `quoteProps` é `as-needed`.

* **semi**: Determina se deve adicionar um ponto e vírgula ao final de cada instrução. Quando definido como `true`, um ponto e vírgula é inserido automaticamente no final de cada instrução. Se definido como `false`, os pontos e vírgulas são omitidos.

O valor padrão de `semi` é `true`.

* **singleAttributePerLine**: Controla se deve forçar a colocação de cada atributo em uma nova linha em elementos HTML, Vue e JSX. Quando definido como `false`, vários atributos podem estar na mesma linha. Se definido como `true`, cada atributo será colocado em sua própria linha.

O valor padrão de `singleAttributePerLine` é `false`.

Quando definido como True: ![Imagem de Atributo Único por Linha](images/beautifyCode/singleAttributePerLine-true.png)

Quando definido como False: ![Imagem de Atributo Único por Linha](images/beautifyCode/singleAttributePerLine-false.png)

* **singleQuote**: Determina se deve usar aspas simples em vez de aspas duplas em seu código. Quando definido como `false`, aspas duplas são usadas para strings. Se definido como `true`, aspas simples são usadas em seu lugar.

O valor padrão de `singleQuote` é `false`.

Quando definido como True: ![Imagem de Aspas Simples](images/beautifyCode/singleQuotes-true.png)

Quando definido como False: ![Imagem de Aspas Simples](images/beautifyCode/singleQuotes-false.png)

* **trailingComma**: Controla o uso de vírgulas finais em estruturas multi-linha separadas por vírgulas.
  * **"none"**: Nenhuma vírgula final é adicionada.
  * **"es5"**: Adiciona vírgulas finais onde for válido no ES5 (por exemplo, em objetos, arrays, etc., mas não em parâmetros de função).
  * **"all"**: Adiciona vírgulas finais em todos os lugares possíveis, incluindo parâmetros de função e imports.

**Nota**: `Nem todos os ambientes JavaScript suportam vírgulas finais em parâmetros de função, e incluílas pode causar problemas de compatibilidade.`

O valor padrão de `trailingComma` é `none`.

Quando definido como none: ![Imagem de Vírgula Final](images/beautifyCode/trailingComma-none.png)

Quando definido como es5: ![Imagem de Vírgula Final](images/beautifyCode/trailingComma-es5.png)

Quando definido como all: ![Imagem de Vírgula Final](images/beautifyCode/trailingComma-all.png)

Modificando a Indentação com o Embelezar Código
----------------------------------------------

Para ajustar o estilo ou o tamanho da indentação em seu código, use o botão Spaces/Tabs na barra de status.

* **Alternar entre espaços e abas**: Clique no botão para alternar entre `spaces` ou `tabs` para a indentação.
* **Ajustar o número de espaços ou abas**: Clique no valor na barra de status ao lado de `spaces`/`tabs` e modifique-o conforme necessário para selecionar o tamanho de indentação desejado.

Depois de alterar o estilo ou o tamanho da indentação, use o **Embelezar Código** para reformatar o arquivo inteiro.

Demonstração Visual
-------------------

<VideoPlayer src="https://docs-images.phcode.dev/videos/beautify-code/beautify-code-edit.mp4" />
