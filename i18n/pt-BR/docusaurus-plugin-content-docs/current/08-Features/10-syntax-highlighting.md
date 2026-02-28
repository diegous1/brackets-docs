---
title: Realce de Sintaxe
---

O **realce de sintaxe** melhora a legibilidade do código ao colorir diferentes elementos de sintaxe no seu código. Este recurso ajuda você a identificar rapidamente palavras-chave, variáveis e outros componentes do código, auxiliando na detecção de erros e na compreensão do código.

## Como Funciona

O realce de sintaxe funciona analisando o código e aplicando esquemas de cores a vários elementos:

* `Palavras-chave`: Palavras especiais com significados predefinidos (ex: if, else).
* `Strings`: Literais de texto entre aspas.
* `Comentários`: Texto não executável, usado para anotações.
* `Variáveis`: Nomes atribuídos a valores de dados.
* `Funções`: Operações ou métodos definidos.

O Phoenix usa regras predefinidas para diferentes linguagens de programação para aplicar as cores apropriadas.

![Imagem Padrão de Realce de Sintaxe](images/syntaxHighlighting/syntax-highlighting.png "Realce de Sintaxe no tema padrão Phoenix Dark")
Exemplo de Realce de Sintaxe em um Arquivo JavaScript

## Dependência do TemaCreate 10-syntax-highlighting.md

As cores usadas para o realce de sintaxe dependem do tema que você está usando. Os temas definem os esquemas de cores para vários elementos de sintaxe, permitindo que você escolha um estilo que se adapte à sua preferência ou necessidade.

Exemplo de Realce de Sintaxe [Tema: `Monokai Dark Soda`]
![Imagem do Realce de Sintaxe no Tema Monokai Dark Soda](images/syntaxHighlighting/syntax-highlighting-monokai-dark-soda-theme.png "Realce de Sintaxe pelo Tema Monokai Dark Soda")

Exemplo de Realce de Sintaxe [Tema: `Material Color Light`]
![Imagem do Realce de Sintaxe no Tema Material Color Light](images/syntaxHighlighting/syntax-highlighting-material-color-light-theme.png "Realce de Sintaxe pelo Tema Material Color Light")

Para saber mais sobre temas. [Clique Aqui](./themes)

## Adicionar Realce de Sintaxe para um Tipo de Arquivo Específico

Se você criar um novo arquivo e o tipo de arquivo não for reconhecido, ele será tratado como texto simples por padrão, e nenhum realce de sintaxe será aplicado. No entanto, você pode adicionar manualmente o realce de sintaxe para o arquivo no Phoenix.

1. Clique no botão **Text**: Localize o botão `Text` na Barra de Status na parte inferior do editor.
2. Selecione uma Linguagem: Na lista suspensa, escolha a linguagem cujas regras de sintaxe você deseja aplicar para destacar este arquivo.

![Adicionando Realce de Sintaxe para um novo tipo de arquivo](images/syntaxHighlighting/syntax-highlighting-add.png "Adicionar Realce de Sintaxe para um arquivo específico")

O arquivo agora será tratado como o tipo de linguagem selecionado, e o realce de sintaxe será aplicado de acordo.

Para saber mais sobre **Associações de Tipos de Arquivo**. [Clique Aqui](../03-editing-text.md#file-type-associations)

### Alterar Realce de Sintaxe para um Tipo de Arquivo Específico

Se você precisar alterar o realce de sintaxe para um arquivo existente:

1. Clique no botão **Text**: Clique no botão `Text` na Barra de Status.
2. Selecione uma Nova Linguagem: Escolha uma linguagem diferente da lista para alterar o realce de sintaxe do arquivo. O realce de sintaxe será atualizado de acordo com a nova linguagem selecionada.

## Solução de Problemas

* **Nenhum Realce** : Certifique-se de que o tipo de arquivo seja reconhecido corretamente pelo editor. Verifique a extensão do arquivo e o modo de linguagem.
* **Cores Incorretas** : Verifique as configurações do seu esquema de cores. Pode ser necessário ajustar ou mudar para um tema diferente.
* **Suporte a Linguagem Ausente** : Instale a extensão de linguagem necessária do marketplace do editor.
