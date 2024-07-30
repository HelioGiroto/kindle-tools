# Baixe em PDF seu livros comprados na Amazon no Linux

Este tutorial é exclusivo para quem deseja baixar seus livros comprados para uso próprio ou para uso do seu próprio material para criar algum recurso de leitura ou audição de seus livros (em caso de deficiência visual, etc). Se conscientize que é proibido, por tanto, não se recomenda a pirataria ou distribuição de material protegido por seus direitos autorais.

**É preciso ter um Kindle para realizar os seguintes passos.**

Passo a Passo Completo e atualizado - Julho/2024:

## 1) Baixar seus livros comprados e obter o número de série do seu Kindle:
- Vá até o site da amazon.com.br
- Contas e Listas

- Em "Biblioteca de Conteúdo" > Ebooks
	- Aparece lista dos ebooks comprados
	- Mais ações
	- Baixar e transferir por USB
	- Marque o seu Kindle
	- Botão "Baixar"	

- Na Aba "Dispositivos"
	- Kindle
	- Clique sobre seu dispositivo
	- Copia o nro de série do seu Kindle


## 2) Baixar o Plugin para desbloquear
- Vá até o blog: https://apprenticealf.wordpress.com/
- Aparecerá um link da versão mais nova do desbloqueador de DRM's
- Clique e vá até o endereço do Github 
- Resumindo: https://github.com/apprenticeharper/DeDRM_tools/releases/tag/v7.2.1
- Baixe a versão clicando sobre o nome do arquivo zip: `DeDRM_tools_nro.zip`
- Depois de baixar, abrir a pasta compactada 
- O plugin é o zip de nome: `DeDRM_plugin.zip`


## 3) Programa Calibre: Baixar no Linux e Instalar plugin

### Baixe o programa Calibre para Linux:
- Ir à https://calibre-ebook.com/download_linux

- Importante que se baixe o link que possa rodar o programa na sua pasta home:

O link está a seguinte mensagem: *You can also do an "isolated" install that only touches files inside the installation folder and does not need to be run as root, like this:*

`wget -nv -O- https://download.calibre-ebook.com/linux-installer.sh | sh /dev/stdin install_dir=~/calibre-bin isolated=y`


Para abrir, digite no Terminal:

`calibre-bin/calibre/calibre`


### Instala plugin no programa:
- Abra o Calibre no Terminal.
- Em Preferências (icone sup.)
- Plugins
- Carregar Plugin a partir de arquivo (botão inf direita)
- Procura na pasta o plugin de nome: `DeDRM_plugin.zip`
- Suba o DeDRM_plugin.zip
- Confirma 


### Insere nro de série do Kindle
- Em Preferências
- Plugins
- Desmarca "Mostrar apenas plugins instalados pelo usuário"
- Sobre o plugin "DeDRM" clica
- Botão "Configurar plugin"
- "elnk Kindle ebooks"
- "+"
- Insere o nro
- Fecha + ok + Aplicar


## 4) Converter livros e salvá-los:

- Depois de baixar o(s) livro(s) do site da Amazon
- Abre a pasta em que está o(s) livro(s)
- Arrasta(m) para o Calibre.
- Botão "Converter livros".
- Escolher extensão para saída de arquivo (PDF, DOCX, EPUB, etc...)
- Botão Salvar em Disco.



## Para desinstalar o Calibre:

Se for preciso desinstalar o programa, basta digitar no Terminal:

`sudo -v && sudo calibre-uninstall`

Ou também se remove com:
- sudo apt purge calibre
- sudo apt autoremove


## Alguns sites interessantes:

https://www.makeuseof.com/tag/best-calibre-plugins-ebook-lovers/

https://www.makeuseof.com/tag/hidden-calibre-features-manage-ebooks/






---

**Erros:**

OBS.: Não há erro se instalada a versão "isolated" comom mencionada acima.

Abaixo: Trecho de https://pt.linux-console.net/?p=31382

Se o método mostrado não funcionar para você e mostrar um erro dizendo que o conteúdo é protegido por DRM, você deverá usar uma versão diferente das ferramentas Caliber e DeDRM:

Remove completamente o calibre:
- sudo apt purge calibre
- sudo apt autoremove

Instale o Calibre versão 4.23

Baixe DeDRM versão 6.8.1

Para instalar o Calibre 4.23, você pode usar o seguinte comando que removerá o Calibre existente e instalará o Calibre versão 4.23:

`sudo -v && sudo calibre-uninstall && wget -nv -O- https://download.calibre-ebook.com/linux-installer.sh | sudo sh /dev/stdin version=4.23.0`


Você pode baixar o DeDRM 6.8.1 na página oficial de download.
	https://github.com/apprenticeharper/DeDRM_tools/releases
	https://github.com/apprenticeharper/DeDRM_tools/releases/tag/v6.8.1



