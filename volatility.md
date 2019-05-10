###  Instalando o configurando Volatility (Fedora 29)

> Descrição: Ferramenta para a extração de artefatos digitais de imagens de memória volátil (RAM)


### Instalando Volatility
 1.  Download cert-forensics-tools-release-29 rpm:
    ```
    # wget https://forensics.cert.org/cert-forensics-tools-release-29.rpm && rpm -Uvh cert-forensics-tools-release*rpm
    # rpm -Uvh cert-forensics-tools-release*rpm
    # dnf --enablerepo=forensics install Volatility
    ```
### Alguns comandos úteis
-   volatility -f hiberfil.sys imagecopy -O hiberfil.raw
	- Para criar uma cópia do arquivo "original" de dump de memória.
-   volatility -f hiberfil.raw imageinfo 
	- Para consultar e detalhar as informações do dump de memória.
-   volatility -f hiberfil.raw --profile=Win7SP1x86_23418 pslist 
	-  Para Mostrar todos os processos executados.
-   volatility -f hiberfil.raw --profile=Win7SP1x86_23418 psxview 
	-  Para Mostrar todos os processos ocultos. Use "| more" -> opcional.
-   volatility -f hiberfil.raw --profile=Win7SP1x86_23418 netscan.
	- Para Mostrar as conexões abertas e ativas do usuário
-   volatility -f hiberfil.raw --profile=Win7SP1x86_23418 connscan.
	- Para Mostra as conexões TCP abertas.
-   volatility -f hiberfil.raw --profile=Win7SP1x86_23418 hashdump.

### Fonte:
> [fedora.pkgs.org](https://fedora.pkgs.org/28/forensics-x86_64/Volatility-2.6-2.fc28.x86_64.rpm.html)
