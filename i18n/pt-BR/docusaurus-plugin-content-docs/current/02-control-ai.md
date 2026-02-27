---
title: Controle de IA para Escola e Trabalho
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Controle de IA para Escola e Trabalho

🔐 Desative ou gerencie recursos de IA no Phoenix Code para ambientes educacionais e empresariais.

:::info Linha do Tempo Importante
A IA do Phoenix Code será lançada após 20 de jan. de 2026. Os recursos de IA exigirão login com uma conta Phoenix Code com um plano de IA gratuito/pago e opt-in explícito do usuário.
Instituições educacionais devem configurar os controles de IA em todo o campus antes desta data para desativar a IA.
:::

## Visão Geral

O Controle de IA do Phoenix Code fornece ferramentas para administradores de sistema gerenciarem a funcionalidade de IA em ambientes educacionais e empresariais. Este recurso ajuda escolas e organizações a:

- Desativar recursos de IA em todo o sistema
- Habilitar IA seletivamente para usuários específicos
- Configurar contatos administrativos para gerenciamento de IA
- Verificar o status do controle de IA em dispositivos de usuários finais

## Instalação

### Requisitos do Sistema

- Windows 10/11, macOS 10.15+, ou Linux baseado em Ubuntu/Debian
- Acesso administrativo para instalação em todo o sistema
- Phoenix Code versão Desktop ou Navegador

### Instalando Scripts de Configuração

Baixe o script apropriado para sua plataforma neste [link](https://github.com/phcode-dev/phoenix-code-ai-control/releases/latest/).

<Tabs
  defaultValue="windows"
  values={[
    { label: 'Windows', value: 'windows' },
    { label: 'macOS', value: 'macos' },
    { label: 'Linux', value: 'linux' },
  ]}>

<TabItem value="windows">

#### Instalação no Windows

1. Baixe o script Batch do Windows:
   - [setup_phoenix_ai_control_win.bat](https://github.com/phcode-dev/phoenix-code-ai-control/releases/latest/)
2. Abra o Prompt de Comando como Administrador:
   - Pressione Win+X e selecione "Prompt de Comando (Admin)"
   - Navegue até o local do download usando o comando `cd`
3. Execute com parâmetros, por exemplo:
   ```batch
   setup_phoenix_ai_control_win.bat --managedByEmail escola.admin@exemplo.com --disableAI
   ```

:::note
O parâmetro `--managedByEmail` é opcional, mas recomendado. Ele fornece um contato administrativo para gerenciar o acesso a recursos de IA e educacionais no futuro.
:::

</TabItem>

<TabItem value="macos">

#### Instalação no macOS

1. Baixe o script macOS:
   - [setup_phoenix_ai_control_mac.sh](https://github.com/phcode-dev/phoenix-code-ai-control/releases/latest/)
2. Abra o Terminal e navegue até o local do download
3. Torne o script executável:
   ```bash
   chmod +x setup_phoenix_ai_control_mac.sh
   ```
4. Execute com parâmetros:
   ```bash
   sudo ./setup_phoenix_ai_control_mac.sh --managedByEmail escola.admin@exemplo.com --disableAI
   ```

:::note
O parâmetro `--managedByEmail` é opcional, mas recomendado.
:::

</TabItem>

<TabItem value="linux">

#### Instalação no Linux

1. Baixe o script Linux:
   - [setup_phoenix_ai_control_linux.sh](https://github.com/phcode-dev/phoenix-code-ai-control/releases/latest/)
2. Abra o Terminal e navegue até o local do download
3. Torne o script executável:
   ```bash
   chmod +x setup_phoenix_ai_control_linux.sh
   ```
4. Execute com parâmetros:
   ```bash
   sudo ./setup_phoenix_ai_control_linux.sh --managedByEmail escola.admin@exemplo.com --disableAI
   ```

:::note
O parâmetro `--managedByEmail` é opcional, mas recomendado.
:::

</TabItem>

</Tabs>

## Opções de Linha de Comando do Script

Todos os scripts de instalação suportam as mesmas opções de linha de comando:

| Opção | Descrição |
|--------|-------------|
| `--help` | Exibir ajuda |
| `--managedByEmail <email>` | Opcional mas recomendado. E-mail do administrador que gerencia a política de IA. |
| `--allowedUsers "<usuários>"` | Lista separada por vírgulas de nomes de usuários permitidos usar IA mesmo quando desabilitada para outros |
| `--disableAI` | Se presente, a IA será desabilitada por padrão para todos os usuários, exceto os especificados em `allowedUsers` |

:::important
Sempre coloque a lista `--allowedUsers` entre aspas para evitar erros de parsing (ex: `--allowedUsers "alice,bob"`)
:::

## Exemplos Comuns de Configuração

### Desativar IA para Todos os Usuários

```bash
sudo ./setup_phoenix_ai_control_linux.sh --disableAI --managedByEmail escola.admin@exemplo.com
```

### Habilitar IA para Todos os Usuários

```bash
sudo ./setup_phoenix_ai_control_linux.sh --managedByEmail escola.admin@exemplo.com
```

### Habilitar IA apenas para Usuários Específicos

```bash
sudo ./setup_phoenix_ai_control_linux.sh --disableAI --allowedUsers "professor1,admin2" --managedByEmail escola.admin@exemplo.com
```

## Perguntas Frequentes

**P: Quando a IA será ativada no Phoenix Code?**

A IA do Phoenix Code será lançada após **`20 de maio de 2025`**. Instituições educacionais devem configurar os controles de IA antes desta data.

**P: O controle de IA é obrigatório?**

Não, o controle de IA é opcional e destinado a instituições educacionais ou empresas que precisam regular o uso de IA. Por padrão, todos os usuários têm acesso aos recursos de IA.

**P: Bloquear a IA afeta outros recursos do Phoenix Code?**

Não, todos os outros recursos do Phoenix Code continuarão a funcionar normalmente. Apenas os recursos com IA, como geração e explicações de código, serão afetados.

## Recursos Adicionais

Para solicitações especiais ou problemas técnicos, entre em contato pelo nosso fórum de discussões em https://github.com/orgs/phcode-dev/discussions/new/choose.
