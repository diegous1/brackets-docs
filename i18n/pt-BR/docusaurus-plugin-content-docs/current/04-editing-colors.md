---
title: Editando Cores
---
import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

Esta seção fornece uma visão geral dos principais recursos de edição de cores no **Phoenix Code**.

---

## Editor de Cores Inline (Inline Color Editor)
O **Editor de Cores Inline** permite editar cores diretamente dentro do **Phoenix Code** usando um seletor de cores.

### Acessando o Editor de Cores Inline
Para abrir o **Editor de Cores Inline**, basta passar o mouse sobre a cor que deseja editar.

![Editor de Cores Inline](./images/editingColors/inlineColorEditor.png "Editor de Cores Inline")

O **Editor de Cores Inline** fornece um botão `Editar`, clique nele para abrir o seletor de cores.

![Seletor de Cores](./images/editingColors/colorPicker.png "Seletor de Cores")

### Entendendo o Diálogo do Seletor de Cores
O diálogo do **Seletor de Cores** permite editar as cores visualmente. Aqui estão os principais componentes:

* **Espectro de Cores**: O quadrado à esquerda ajusta o brilho e a intensidade da cor. Arraste o círculo para selecionar uma tonalidade específica.
* **Slider de Matiz (Hue)**: O controle deslizante vertical ajusta a cor principal (matiz). Mova-o para cima ou para baixo para alternar entre cores como vermelho, verde ou azul.
* **Slider de Transparência**: O controle deslizante quadriculado ajusta o Alpha (transparência) da cor. Mova-o para definir a cor entre totalmente sólida e totalmente transparente.
* **Visualização da Cor**: No canto superior direito, você verá uma Visualização da Cor. A visualização é dividida em duas partes:
    * *Lado Direito: Exibe a nova cor sendo selecionada. Ele atualiza dinamicamente conforme você ajusta os controles.*
    * *Lado Esquerdo: Exibe a cor original antes da edição.*
* **Sugestões de Cores**: À direita, uma lista de cores já usadas no arquivo é exibida. Passar o mouse sobre uma cor mostra quantas vezes ela foi usada no arquivo. Isso ajuda você a escolher cores consistentes sem precisar lembrar de seus códigos.
* **Seleção de Formato de Código**: Abaixo do Espectro de Cores, temos a opção de alternar entre diferentes formatos:
    * *RGBA: Vermelho, Verde, Azul e Alpha (transparência).*
    * *Hex: Código de cor hexadecimal padrão.*
    * *HSLa: Matiz (Hue), Saturação, Luminosidade e Alpha.*
    * *Hex 0x: Formato hexadecimal com um prefixo 0x, como 0xFF5733.*
* **Campo de Entrada**: Na parte inferior do diálogo, você pode digitar valores de cores específicos diretamente (por exemplo, #FF5733, rgb(255, 87, 51, 1), orange).

### Referência Visual
<VideoPlayer
  src="https://docs-images.phcode.dev/videos/editing-colors/inlineColorEditor.mp4"
/>

---

## Visualização de Cores (Color Preview)
O recurso **Color Preview** exibe a(s) cor(es) usada(s) na linha atual na área da calha (gutter).

![Visualização de Cores](./images/editingColors/colorPreview.png "Visualização de Cores")

> Um máximo de quatro cores pode ser exibido para uma única linha.

### Interação ao Passar o Mouse
* Passar o mouse sobre um quadrado de cor destaca o texto da cor correspondente no editor com um fundo da mesma cor.
* Se um contêiner tiver várias cores, o quadrado de cor sobre o qual o mouse está posicionado aumenta para facilitar o acesso, e seu texto de cor é destacado com a mesma cor.

![Visualização de Cores ao Passar o Mouse](./images/editingColors/colorPreviewHover.png "Visualização de Cores ao Passar o Mouse")

### Comportamento do Clique
Clicar em uma cor na calha move o cursor para sua posição no editor e abre o Seletor de Cores para edição.

### Ativando/Desativando a Visualização de Cores
Você pode ativar/desativar o recurso atualizando a propriedade `colorPreview` no arquivo de preferências.

[Clique Aqui](./03-editing-text.md#editing-preferencias) para ler sobre como editar as preferências.

---

## Dicas de Cores (Color Hints)
Depois de digitar uma propriedade relacionada a cores, o **Phoenix Code** exibe uma lista de sugestões de cores.

![Dicas de Cores](./images/editingColors/colorHints.png "Dicas de Cores")

### Sugestões de Cores Usadas Anteriormente
Se um arquivo já contém cores, o **Phoenix Code** prioriza those colors in the color hint list. As cores são classificadas em *ordem decrescente* com base na contagem de uso no arquivo.

![Cores Usadas Anteriormente](./images/editingColors/previously-used-colors.png "Cores Usadas Anteriormente")

> Isso ajuda a reutilizar cores frequentemente usadas sem procurá-las manualmente.
---
