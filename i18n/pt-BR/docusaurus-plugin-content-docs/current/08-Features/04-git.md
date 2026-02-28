---
title: Git
---

import React from 'react';
import VideoPlayer from '@site/src/components/Video/player';

## Introdução ao Git no Phoenix Code

O **Phoenix Code** inclui suporte integrado ao Git, permitindo que você gerencie o controle de versão diretamente dentro do editor. O Git pode ser acessado pelo ícone na barra de ferramentas ou pelo menu Arquivo na barra de menus.

![Visão Geral do Git](images/git-images/git-overview.png)

> Para usar os recursos do Git dentro do Phoenix Code, certifique-se de que o Git esteja instalado em seu computador. [Baixar Git](https://git-scm.com/downloads)

### Clonando um Repositório

Para clonar um repositório existente no **Phoenix Code**, siga estas etapas:

1. Clique no botão `Iniciar Projeto`.

![Iniciar Projeto](images/git-images/start-project.png)

> Isso abrirá a caixa de diálogo do projeto de Início Rápido, que oferece várias opções. [Leia mais](https://github.com/diegous1/brackets-docs/blob/main/docs/05-quick-start-project.md) sobre o projeto de Início Rápido aqui.

2. Selecione `Obter do Git`.

![Obter do Git](images/git-images/get-from-git.png)

3. Insira a URL de Clonagem do Git e escolha um local para salvar o projeto.

![Caixa de diálogo Obter do Git](images/git-images/get-from-git-dialog.png)

4. Clique em `Criar Projeto`. O repositório será clonado para o local especificado.

### Método Alternativo de Clonagem

Você também pode clonar um repositório através do menu:

1. Vá em `Arquivo > Git > Clonar`.
2. Insira a URL do repositório na caixa de diálogo que aparece.

![Clonagem Git](images/git-images/git-clone-dialog.png)

#### Mais Opções

Na caixa de diálogo Clonar Repositório, clicar em `Mais Opções` expande configurações adicionais para autenticação.

![Mais opções de Clonagem Git](images/git-images/git-clone-more-options.png)

**Credenciais**: Esta seção permite que você insira seu nome de usuário e senha para repositórios que exigem autenticação. Normalmente, se suas credenciais já estiverem armazenadas em um gerenciador de credenciais (como chaves SSH ou um gerenciador de credenciais do Git), você não precisa preencher esses campos.

**Salvar Credenciais na URL Remota**: Se habilitado, as credenciais fornecidas (nome de usuário e senha) serão armazenadas em texto simples dentro da URL remota.

Se a clonagem falhar devido a problemas de autenticação (por exemplo, erros de tempo limite), você pode precisar fornecer suas credenciais manualmente.

### Inicializando um repositório Git

Para inicializar um repositório Git em um projeto que ainda não possui um, clique em `Arquivo > Git > Iniciar`. Isso configurará o Git para o seu projeto atual. Após a inicialização, o ícone do Git aparecerá na barra de ferramentas, indicando que o controle de versão está ativo.

![Iniciar Git](images/git-images/git-init.png)

> Nota: Para projetos sem um repositório Git existente, o ícone do Git não aparecerá por padrão. Para inicializar ou conectar um repositório Git, use the menu Arquivo para configurar o Git em seu projeto.

Assim que o Git estiver configurado, o Painel Git fornece uma interface amigável para gerenciar o controle de versão. Você pode acompanhar alterações, confirmar atualizações, interagir com repositórios remotos e muito mais — tudo dentro do editor.

![Painel Git](images/git-images/git-panel.png)

## Status do Arquivo

Todos os arquivos com alterações são exibidos no painel Git junto com seu status, como Modificado, Não Rastreado e Excluído. Para arquivos modificados, um botão de diferença do Git (Git diff) está disponível.

![Ícone Git diff](images/git-images/git-diff-icon.png)

O Git diff é usado para exibir as alterações feitas em um arquivo — Linhas verdes indicam conteúdo adicionado, enquanto linhas vermelhas mostram conteúdo removido. Clicar no ícone do Git diff abre a página da caixa de diálogo do Git diff.

![Caixa de diálogo Git diff](images/git-images/git-diff-dialog.png)

### Descartar alterações

Para os status de arquivo Modificado e Excluído, um botão `Descartar Alterações...` é exibido. Clicar nele redefinirá as alterações para arquivos Modificados e restaurará arquivos Excluídos.

Para arquivos Não Rastreados, um botão `Excluir Arquivo...` está disponível. Clicar nele excluirá o arquivo.

![Descartar alterações ou Excluir arquivo](images/git-images/discard-changes.png)

Você também pode descartar todas as alterações feitas em todos os arquivos de uma só vez clicando nos três pontos no canto superior direito e selecionando a opção `Descartar todas as alterações desde a última confirmação...`. Isso removerá todas as modificações feitas desde o seu último commit.

![Descartar todas as alterações](images/git-images/discard-all-changes.png)

## Navegar pelas Alterações do Git

Ao visualizar um arquivo com várias alterações do Git, você pode usar os botões Próxima Alteração e Alteração Anterior para se mover rapidamente entre as modificações.

* **Próxima Alteração**: Move o cursor para a próxima alteração no arquivo. ![Mover para próxima alteração](images/git-images/move-to-next-change.png)
* **Alteração Anterior**: Move o cursor para a alteração anterior no arquivo. ![Mover para alteração anterior](images/git-images/move-to-previous-change.png)

**Referência Visual**

## Atualizar Painel

O botão **Atualizar Painel** garante que as informações do repositório exibidas estejam atualizadas. Embora as alterações geralmente sejam atualizadas automaticamente, este botão ajuda nos casos em que a interface fica lenta, garantindo que todas as modificações sejam refletidas corretamente.

![Atualizar Painel](images/git-images/refresh-panel.png)

## Commit (Confirmar)

Para preparar (stage) ou desmarcar (unstage) os arquivos, clique no ícone da caixa de seleção no canto superior esquerdo do painel Git. Isso afetará todos os arquivos na árvore de trabalho.

![Preparar todos os arquivos](images/git-images/stage-files.png)

Você também pode preparar/desmarcar arquivos individuais selecionando ou desmarcando a caixa de seleção ao lado de cada arquivo.

Assim que tiver todos os arquivos necessários na área de preparação, clique no botão `Commit`.

![Confirmar os arquivos](images/git-images/git-commit.png)

Isso abrirá a caixa de diálogo de commit do Git, que exibirá todas as alterações feitas nos arquivos que serão confirmados. Você pode inserir sua mensagem de commit na caixa de entrada fornecida.

![Caixa de diálogo Git Commit](images/git-images/commit-dialog.png)

> A caixa de entrada de Commit também exibe o número de caracteres na mensagem de commit.

Se sua mensagem de commit for longa, você pode usar o botão `Expandido` no canto superior direito da caixa de diálogo. Isso expande a área de entrada, facilitando a escrita de mensagens de commit detalhadas.

A caixa de diálogo de commit também fornece opções para:

* **Corrigir Último Commit (Amend)**: Selecionar esta opção permite que você modifique o commit mais recente em vez de criar um novo.
* **Ignorar Verificações de Pré-Commit**: Habilitar esta opção ignora quaisquer hooks de pré-commit ou etapas de validação.

> A caixa de diálogo de commit do Git também exibe problemas de inspeção de código, se houver:

![Erros de inspeção de código no Commit](images/git-images/git-commit-errors.png)

## Push (Enviar)

Para enviar seus commits locais para o repositório remoto, use a opção `Push` no painel Git. Isso garante que suas alterações sejam sincronizadas com o repositório remoto.

![Git Push](images/git-images/git-push.png)

Quando você inicia um push, a caixa de diálogo **Push para Remoto** aparece, permitindo que você configure as definições de envio.

![Caixa de diálogo Git Push](images/git-images/push-dialog.png)

### Ramo de Destino (Target Branch)

* **Push para o ramo de rastreamento atual**: Envia as alterações para o ramo atualmente vinculado ao seu ramo local.
* **Push para outro ramo**: Permite enviar para um ramo diferente no remoto.

### Comportamento do Push

* **Push padrão**: Envia suas alterações locais para o ramo remoto.
* **Push forçado**: Sobrescreve o ramo remoto com suas alterações locais.
* **Excluir ramo remoto**: Remove permanentemente o ramo selecionado do repositório remoto.

### Mais Opções

Clicar em Mais Opções expande configurações de push adicionais, permitindo mais controle sobre a operação de envio.

![Mais opções de push do Git](images/git-images/git-push-more-options.png)

* **Enviar tags**: Se habilitado, esta opção garante que as tags do Git sejam enviadas junto com os commits. Se você criou tags localmente e deseja que elas sejam refletidas no repositório remoto, habilite esta opção.
* **Ignorar verificações de pré-push (--no-verify)**: Habilitar esta opção ignora quaisquer hooks de pré-push ou etapas de validação.
* **Credenciais**: Esta seção permite que você insira seu nome de usuário e senha para repositórios que exigem autenticação. Normalmente, se suas credenciais já estiverem armazenadas em um gerenciador de credenciais (como chaves SSH ou um gerenciador de credenciais do Git), você não precisa preencher esses campos.
* **Salvar Credenciais na URL Remota**: Se habilitado, as credenciais fornecidas (nome de usuário e senha) serão armazenadas em texto simples dentro da URL remota.

## Fetch (Buscar)

Para baixar as últimas alterações do repositório remoto sem modificar seu repositório local, use a opção `Fetch` no painel Git. Isso trará as últimas alterações do repositório remoto, mas não atualizará seu diretório de trabalho nem mesclará as alterações em seus ramos locais.

![Git fetch](images/git-images/git-fetch.png)

## Pull (Puxar)

Para baixar as últimas alterações do repositório remoto para sua máquina local, use a opção `Pull` no painel Git. Isso garante que seu repositório local esteja atualizado com as últimas alterações do repositório remoto.

![Git pull](images/git-images/git-pull.png)

Quando você inicia um pull, a caixa de diálogo **Pull do Remoto** aparece, permitindo que você configure as definições de puxada.

![Caixa de diálogo Git pull](images/git-images/git-pull-dialog.png)

### Ramo de Destino (Target Branch)

* **Pull do ramo de rastreamento atual**: Puxa as últimas alterações do ramo remoto rastreado atualmente.
* **Pull de outro ramo**: Permite que você puxe alterações de um ramo remoto diferente.

### Comportamento do Pull

* **Mesclagem padrão (Merge)**: Mescla as alterações buscadas em seu ramo atual.
* **Evitar mesclagem manual**: Tenta resolver conflitos automaticamente sem intervenção manual.
* **Mesclar sem confirmar**: Mescla as alterações, mas não cria um commit automático.
* **Usar rebase**: Aplica as alterações recebidas sobre seus commits locais para um histórico mais limpo.
* **Usar reset suave**: Redefine para o commit remoto mais recente sem descartar as alterações locais.

## Log (Histórico)

O **Phoenix Code** fornece duas opções para visualizar o histórico do Git:

### Mostrar Histórico

![Mostrar Histórico](images/git-images/show-history.png) Clicar no botão **Mostrar Histórico** exibe uma lista completa de commits feitos em todo o repositório para ajudar você a acompanhar as alterações feitas no projeto ao longo do tempo.

### Mostrar Histórico do Arquivo

![Mostrar Histórico do Arquivo](images/git-images/show-file-history.png) Clicar no botão **Mostrar Histórico do Arquivo** exibe o histórico de commits de um arquivo específico, mostrando todas as modificações desde que ele foi adicionado ao repositório.

### Visualizador de Histórico

Ao selecionar um commit específico no painel de histórico, o **Visualizador de Histórico** aparece, exibindo todas as alterações feitas naquele commit.

![Visualizador de Histórico](images/git-images/history-viewer.png)

* Cada arquivo modificado é recolhido por padrão.
* Clicar em um arquivo o expande para mostrar as alterações exatas.

![Visualizador de Histórico expandido](images/git-images/history-viewer-expanded.png)

* Você pode expandir ou recolher todos os arquivos de uma vez usando o botão Expandir Tudo/Recolher Tudo.

Isso permite que você inspecione as alterações diretamente dentro do editor.

## Branch (Ramo)

### Criando um novo ramo

Para criar um novo ramo no Git, clique no botão `main > Criar novo ramo...` na barra lateral. O nome mostrado (por exemplo, main) representa seu ramo atual, portanto, se você estiver em um ramo diferente, ele poderá exibir outro nome.

![Ramo Git](images/git-images/git-branch.png)

Isso abrirá uma caixa de diálogo onde você pode:

![Caixa de diálogo de novo ramo Git](images/git-images/git-new-branch-dialog.png)

* Selecionar o ramo a partir do qual o novo ramo se originará.
* Inserir um nome para o seu novo ramo.

Uma vez criado, ele muda automaticamente para o novo ramo e você pode começar a trabalhar de forma independente.

### Mesclando um ramo (Merging)

Para mesclar um ramo no ramo atual, clique no nome do ramo atual (por exemplo, main) na barra lateral. Isso abrirá um popup exibindo todos os ramos disponíveis. À direita de cada nome de ramo, você verá um ícone de mesclagem.

![Mesclar ramo](images/git-images/merge-branch.png)

Clique neste ícone para o ramo que deseja mesclar.

Isso abrirá uma caixa de diálogo de mesclagem com as seguintes opções:

![Caixa de diálogo de mesclagem de ramo](images/git-images/merge-branch-dialog.png)

* **Ramo de destino**: Exibe o ramo onde o ramo selecionado será mesclado.
* **Mensagem de mesclagem**: Fornece uma mensagem padrão para a mesclagem, que você pode editar.
* **Usar REBASE**: Se marcado, ele rebaseia os commits em vez de mesclá-los.
* **Criar um commit de mesclagem mesmo quando a mesclagem for resolvida como fast-forward**: Se marcado, ele força um commit de mesclagem mesmo se uma mesclagem fast-forward for possível.

### Excluindo um ramo

Para excluir um ramo local no Git, clique no nome do ramo atual (por exemplo, main) na barra lateral. Isso abrirá um menu suspenso exibindo a lista de todos os ramos disponíveis.

![Excluir ramo](images/git-images/delete-branch.png)

Em seguida, passe o mouse sobre o ramo que deseja excluir e clique no ícone de cruz 'x' ao lado dele. Isso excluirá o ramo selecionado.

## Remoto (Remote)

### Adicionando um Novo Remoto

Para adicionar um novo remoto ao seu repositório Git, abra o painel Git e clique em `origin > Criar novo remoto...`.

![Git remoto](images/git-images/git-remote.png)

O nome mostrado (por exemplo, origin) representa seu remoto atual, portanto, se você estiver em um remoto diferente, ele poderá exibir outro nome.

Isso abrirá uma caixa de diálogo, solicitando que você insira o nome do novo remoto.

![Nome do remoto Git](images/git-images/git-remote-name.png) Depois disso, uma nova caixa de diálogo aparecerá, solicitando que você insira a URL do novo remoto. Insira a URL e clique em `OK`.

Isso adiciona um novo remoto.

### Excluindo um Remoto

Para excluir um remoto do seu repositório Git, clique no nome do remoto atual no painel Git. Isso abrirá um menu suspenso exibindo a lista de todos os remotos.

Em seguida, passe o mouse sobre o remoto que deseja excluir e clique no ícone de cruz 'x' ao lado dele. Isso removerá o remoto selecionado do seu repositório.

![Excluir remoto Git](images/git-images/git-delete-remote.png)

> Nota: Não é possível excluir o remoto 'origin'.

### Alternando Entre Remotos

Para alternar entre remotos em seu repositório Git, clique no nome do remoto atual no painel Git. Um menu suspenso aparecerá mostrando todos os remotos disponíveis.

Selecione o remoto para o qual deseja alternar, e o Git usará esse remoto para operações como buscar (fetch), puxar (pull) ou enviar (push).

## Menu Git

O Menu Git fornece várias ações relacionadas ao Git para gerenciar o controle de versão dentro do aplicativo. Para acessar este menu, navegue até `Arquivo > Git`.

![Menu Git](images/git-images/git-menu.png)

Alternativamente, você também pode acessar o menu Git clicando nos três pontos no canto superior direito do painel Git.

![Menu Git pelo painel](images/git-images/git-menu-from-panel.png)

Aqui estão as opções disponíveis no painel Git:

### Opções gerais

* **Mostrar Painel Git**: Alterna a visibilidade do painel Git na interface.
* **Atualizar Git**: Atualiza o painel Git para refletir as alterações mais recentes no repositório. [Leia mais](#atualizar-painel) sobre como atualizar o Git.

### Opções de navegação

* **Ir para a Próxima Alteração do Git**: Move o cursor para a próxima alteração rastreada pelo Git no arquivo.
* **Ir para a Alteração Anterior do Git**: Move o cursor para a alteração anterior rastreada pelo Git no arquivo. [Leia mais](#navegar-pelas-alterações-do-git) sobre as opções de navegação.
* **Fechar Arquivos Não Modificados**: Fecha todos os arquivos abertos que não possuem alterações não confirmadas.

### Histórico de versões

* **Ver Autores da Seleção...**: Exibe o histórico do Git de uma parte selecionada do código, mostrando quem fez as alterações e quando. ![Ver Autores](images/git-images/view-authors.png)
* **Ver Autores do Arquivo...**: Mostra o histórico de commits e colaboradores para o arquivo inteiro.

### Confirmando Alterações (Committing)

* **Confirmar Arquivo Atual...**: Abre uma caixa de diálogo para confirmar as alterações no arquivo ativo no momento.
* **Confirmar Todos os Arquivos...**: Abre uma caixa de diálogo para confirmar todas as alterações preparadas no repositório.

[Leia mais](#commit-confirmar) sobre como confirmar alterações.

### Operações Remotas

* **Buscar do Remoto (Fetch)**: Recupera as alterações mais recentes do repositório remoto sem mesclá-las no ramo local. [Leia mais](#fetch-buscar) sobre como buscar alterações do remoto.
* **Puxar do Remoto (Pull)...**: Busca e integra as alterações do repositório remoto no ramo atual. [Leia mais](#pull-puxar) sobre como puxar alterações do remoto.
* **Enviar para o Remoto (Push)...**: Envia os commits locais para o repositório remoto (mostra o número de commits à frente do ramo remoto). [Leia mais](#push-enviar) sobre como enviar alterações para o remoto.

### Configuração

* **Usar Push Ref Compatível com Gerrit**: Habilita referências de push compatíveis com o Gerrit, um sistema de revisão de código baseado na web. [Leia mais](https://www.gerritcodereview.com/) sobre o Gerrit.
* **Alterar Nome de Usuário do Git...**: Permite atualizar o nome de usuário do Git para os commits.
* **Alterar E-mail do Git...**: Permite atualizar o endereço de e-mail do Git para os commits.

### Configurações

* **Configurações do Git...**: Abre a caixa de diálogo Configurações do Git para configurar o comportamento do Git dentro do aplicativo. [Leia mais](#configurações-do-git) sobre as configurações do Git.

## Configurações do Git

A caixa de diálogo Configurações do Git fornece opções para configurar o comportamento do Git dentro do aplicativo. Para abrir a caixa de diálogo Configurações do Git, vá em `Arquivo > Git > Configurações do Git...`.

![Configurações do Git no menu Arquivo](images/git-images/git-settings-from-file-menu.png)

Alternativamente, você pode acessá-la pelo painel Git clicando nos três pontos no canto superior direito e selecionando `Configurações do Git...`.

![Configurações do Git no Painel](images/git-images/git-settings-from-panel.png)

### Configurações Gerais

![Caixa de diálogo de Configurações do Git](images/git-images/git-settings-dialog.png)

> As configurações com um ícone de informação exigem a reinicialização do aplicativo para entrarem em vigor.

* **Habilitar Git**: Ativa ou desativa a integração com o Git.
* **Remover espaços em branco ao final nos commits:** Remove automaticamente espaços extras no final das linhas ao confirmar as alterações.
* **Adicionar quebra de linha ao final do arquivo**: Garante que um caractere de nova linha seja adicionado ao final de cada arquivo.
* **Remover BOM dos arquivos**: Remove a Marca de Ordem de Byte (BOM) dos arquivos para manter a consistência.
* **Normalizar quebras de linha (para \n)**: Converte diferentes quebras de linha (como Windows \r\n) para o estilo Unix \n.
* **Usar marcas de calha do Git**: Exibe indicadores de alteração na calha (área de números de linha) do editor.
* **Marcar arquivos modificados na árvore de arquivos**: Destaca arquivos modificados no explorador de arquivos para fácil rastreamento.
* **Mostrar saída detalhada em diffs**: Fornece uma saída detalhada ao visualizar as diferenças entre as versões dos arquivos.
* **Usar difftool para diffs**: Permite o uso de uma ferramenta de diff externa para comparar alterações.
* **Limpar espaços em branco ao salvar o arquivo**: Remove espaços em branco desnecessários sempre que um arquivo é salvo.

### Configuração do Sistema

* **Caminho para o executável do Git**: Permite especificar um caminho personalizado para a instalação do Git, se necessário.
* **Tempo limite padrão da operação Git (em segundos)**: Define a duração máxima para as operações do Git antes que expirem (padrão: 30 segundos).

## FAQ

#### P. Por que o ícone do Git não é exibido na barra de ferramentas do Phoenix?

O ícone do Git não aparece na barra de ferramentas se o projeto que você abriu não for um repositório Git. Também pode estar ausente se o Git não estiver instalado em sua máquina.

#### P. Por que recebo um erro ao tentar enviar alterações para o remoto?

Se você vir o erro "Falha ao enviar para o remoto" (Pushing to remote failed), significa que há novas alterações no repositório remoto que você ainda não puxou.

![Erro de push do Git](images/git-images/git-push-error.png)

**Como corrigir:** Antes de enviar suas alterações, puxe as atualizações mais recentes do repositório remoto. [Saiba como puxar alterações](#pull-puxar).
