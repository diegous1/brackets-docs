---
title: Instalar/Desinstalar no Linux
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Visão Geral
Este guia detalha como instalar o Phoenix Code em sistemas Linux. Nosso instalador funciona com as principais distribuições Linux (Ubuntu, Debian, Fedora e sistemas baseados em Arch).

## Instalação Automática
Para instalar o Phoenix Code automaticamente, execute o seguinte comando no seu terminal:
```bash
wget -qO- https://updates.phcode.io/linux/installer.sh | bash
```
Este script instala automaticamente o Phoenix Code e todas as dependências necessárias.
Também configura atalhos na gaveta de aplicativos e associações de arquivos.

**Desinstalar**

Execute o seguinte comando no seu terminal.
```bash
wget -qO- https://updates.phcode.io/linux/installer.sh | bash -s -- --uninstall
```

## Instalação Manual
Se a instalação automática falhar ou se a instalação manual for preferida, siga estas etapas:

1. **Verificar a Versão do GLIBC**:
   Determine a versão do GLIBC do seu sistema usando:
   ```bash
   ldd --version | awk '/ldd/{print $NF}'
   ```

2. **Baixar o Pacote**:
   Visite a [Página de Releases do Phoenix Code](https://github.com/phcode-dev/phoenix-desktop/releases) e baixe uma versão compatível com seu GLIBC.

3. **Extrair o Pacote**:
   Descompacte o arquivo baixado com:
   ```bash
   tar -xvf phoenix_code_version.tar.gz
   ```

4. **Ler as Instruções de Instalação**:
   Leia as instruções detalhadas contidas no pacote:
   ```bash
   cat extracted_folder/ReadMe.txt
   ```

5. **Executar os Passos de Instalação**:
   Siga as instruções no `readme.txt` para concluir a instalação.

## Compatibilidade com Ambientes de Desktop
O Phoenix Code é testado com os ambientes de desktop `Gnome` e `KDE`.
Outros ambientes de desktop podem ser compatíveis com a [Instalação Manual](#instalação-manual).

## Perguntas Frequentes
**P: Como posso verificar se minha distribuição é suportada?**

Execute a [Instalação Automática](#instalação-automática). Se for concluída com sucesso, sua distribuição é suportada.

**P: Como faço para atualizar o Phoenix Code?**

Para instalações automáticas, você receberá uma notificação de atualização no próprio aplicativo.
Para [Instalações Manuais](#instalação-manual), siga a seção novamente.

**P: Como faço para desinstalar o Phoenix Code?**

Para instalações automáticas, use o comando:
```bash
wget -qO- https://updates.phcode.io/linux/installer.sh | bash -s -- --uninstall
```
Para instalações manuais, exclua a pasta onde você colocou o aplicativo Phoenix Code e remova quaisquer arquivos relacionados.

**P: O Phoenix não está iniciando após a instalação. O que posso fazer?**

Reinicie o sistema. Confirme que as dependências necessárias listadas abaixo para sua distribuição Linux estão instaladas.

Atualize sua lista de pacotes:
```bash
sudo apt update
```
Instale WebKitGTK e GTK:
```bash
sudo apt install libgtk-3-0 libwebkit2gtk-4.0-37
```
*Nota: No Ubuntu 22+, o WebKitGTK pode já estar pré-instalado.*

Instale plugins opcionais do GStreamer para reprodução de mídia:
```bash
sudo apt install gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-tools gstreamer1.0-libav
```
Atualize sua lista de pacotes:
```bash
sudo dnf update
```
Instale WebKitGTK e GTK:
```bash
sudo dnf install webkit2gtk3 gtk3
```
Instale plugins opcionais do GStreamer para reprodução de mídia:
```bash
sudo dnf install gstreamer1-plugins-base gstreamer1-plugins-good gstreamer1-plugins-bad-free gstreamer1-plugins-bad-freeworld gstreamer1-plugins-ugly gstreamer1-libav
```
Garantir que o sistema esteja atualizado:
```bash
sudo pacman -Syu
```
Instale WebKitGTK e GTK:
```bash
sudo pacman -S webkit2gtk gtk3
```
Instale plugins opcionais do GStreamer para reprodução de mídia:
```bash
sudo pacman -S gst-plugins-base gst-plugins-good gst-plugins-bad gst-plugins-ugly gst-libav
```
