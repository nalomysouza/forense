###  Instalando o configurando Guymager 0.8.8 (Fedora 29)

> Descrição: guymager is an imager for forensic media acquisition. Its
> main features are:

* Easy user interface in different languages
* Runs under Linux
* Multi-threaded design, multi-threaded data compression
* Makes full usage of multi-processor machines
* Generates flat (dd) and EWF (E01) images

### Instalando guymager
 1.  Download cert-forensics-tools-release-29 rpm:
    ```
    # wget https://forensics.cert.org/cert-forensics-tools-release-29.rpm && rpm -Uvh cert-forensics-tools-release*rpm
    # rpm -Uvh cert-forensics-tools-release*rpm
    # dnf --enablerepo=forensics install guymager
    ```
### Clonando disco formato Forense
 1. Execute o programa **Guymager**;
 2. Para adicionar discos vá em "**devices > add special device**";
 3. Selecione o dispositivo que deseja clonar e "**acquire image**";
 4. Na tela que abrir escolha a opção "**Expert Witness Format**" e informa o tamanho que quer gerar o arquivo de imagem "**splitFileSize**" , sugestão é gerar um arquivo único assim informar o valor maior que o disco.
 5. Informe a pasta onde vai salvar "**destImageDirectory**" e um nome para a imagem  "**destImageFileName**".
 6. Finalmente, definir um modelo de Hash e verificação, como  as opções **MD5** e **SHA-1**.
 7. aguarde finalizar, vai aparecer "**Finished - 	Verified & ok**".

### Fonte:
[https://fedora.pkgs.org/29/forensics-x86_64/guymager-0.8.8-2.fc29.x86_64.rpm.html](https://fedora.pkgs.org/29/forensics-x86_64/guymager-0.8.8-2.fc29.x86_64.rpm.html)
