# Localizar em Arquivos

O recurso "Localizar em Arquivos" (Find in Files) no Phoenix Code é uma ferramenta poderosa para pesquisar rapidamente por textos específicos em vários arquivos dentro de um projeto. Este recurso é útil para desenvolvedores que trabalham em grandes bases de código para encontrar referências, nomes de variáveis ou linhas específicas de código.

Para pesquisar em todos os arquivos do seu projeto, use `Ctrl-Shift-F` no Windows/Linux ou `Cmd-Shift-F` no Mac, ou selecione `Localizar > Localizar em Arquivos` no menu. Este recurso pesquisa o seu termo em todos os arquivos do projeto e exibe cada ocorrência com o nome do arquivo, o número da linha e um trecho do código para contexto.

![Texto alternativo](images/find/fif.png)

## Pesquisando Dentro de uma Pasta

Para pesquisar dentro de uma pasta específica no Phoenix:

1. Clique com o botão direito na pasta no painel de Arquivos onde deseja realizar a pesquisa.
2. No menu de contexto que aparece, selecione "Localizar em...".

![Texto alternativo](images/find/folder.png)

3. A barra de busca aparecerá agora com a pesquisa restrita àquela pasta (veja `in y/` na imagem abaixo).

![Texto alternativo](images/find/inFolder.png)

## Usando Filtros de Arquivo

Por padrão, o Localizar em Arquivos pesquisa todos os arquivos na pasta do seu projeto. Você pode excluir ou incluir arquivos, tipos de arquivo, pastas inteiras ou outros padrões:

* Clique no menu suspenso "Nenhum Arquivo Excluído" na barra de pesquisa.

  ![Texto alternativo](images/find/new-exclusion.png)

O Phoenix Code permite que você especifique quais arquivos e pastas devem ser excluídos ou incluídos durante as pesquisas no projeto.

### Para pesquisar apenas em arquivos que correspondam ao padrão

Quando você seleciona a opção `Pesquisar em arquivos` no menu suspenso acima, o filtro pesquisará apenas nos arquivos e pastas que correspondam aos padrões inseridos. Digitar `*.json,*.css` incluirá apenas arquivos JSON e CSS nos seus resultados de busca, ou apenas digite `json` para selecionar qualquer arquivo que tenha os caracteres `json` no seu caminho. Veja mais padrões abaixo.

![Texto alternativo](images/find/search_in_files.png)

### Para Excluir arquivos

Quando você seleciona a opção `Excluir arquivos` no menu suspenso acima, o filtro ignorará os arquivos e pastas que correspondam aos padrões que você inserir. Por exemplo, digitar `*.json` na área de texto excluirá todos os arquivos JSON dos seus resultados de busca. Veja mais padrões abaixo.

## O padrão de filtro

Esta seção descreve o formato do padrão glob para exclusão/pesquisa dentro de arquivos.

1. Cada padrão deve ser inserido como um texto separado por vírgulas. Você pode especificar múltiplos padrões: `*.js, *.json`
2. Para pesquisa aproximada (fuzzy), basta inserir o texto. Ex: digitar `css` corresponderá a todos os nomes de arquivos que tenham as letras `css` no caminho, como `x/st.css` e `cssFile.md`.
3. Para corresponder a todos os arquivos JavaScript em qualquer diretório, use `*.js`. Isso corresponde a arquivos como `a/b/x.js` e `xyz.js`.
4. Para corresponder a arquivos JavaScript apenas na raiz do projeto, use `./*.js`. Isso corresponde a `x.js` na raiz, mas não a `y/x.js` em um subdiretório.
5. Para corresponder a arquivos CSS apenas em uma pasta `search/folder`, use `search/folder/*.css`. Isso corresponde a `search/folder/x.css`, mas não a `y/x.css`.
6. `?.js` corresponderá apenas a `a/b/x.js` e não a `xyx.js`.
7. `**/alguma_pasta/**` corresponderá a `alguma_pasta` em qualquer lugar.
8. `[]` para declarar um intervalo de caracteres para correspondência (`exemplo.[0-9]` para corresponder a `exemplo.0`, `exemplo.1`, …).
9. Para pesquisar por nomes de arquivos com `,` neles, use o caractere de escape `\`. Ex: para corresponder a um arquivo com o nome `ola,mundo.js`, a string de filtro a ser usada é `ola\,mundo.js`.
10. Padrões glob mais complexos podem ser fornecidos. Veja: [https://www.malikbrowne.com/blog/a-beginners-guide-glob-patterns/](https://www.malikbrowne.com/blog/a-beginners-guide-glob-patterns/)
