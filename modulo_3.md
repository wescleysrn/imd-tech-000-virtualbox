[Voltar para o início](./README.md)

## Módulo 3 - Templates e Sistemas Linux

**🎯 Objetivo**

<p align="justify">Apresentar o conceito de templates, mostrar onde encontrar distribuições Linux confiáveis e preparar o ISO que será usado na criação da máquina virtual.</p>

### 3.1 - O Que São Templates (Ou ISOS) ?

<p align="justify">No contexto de virtualização, um <strong>template</strong> é um modelo pronto para criar uma nova máquina virtual. Ele pode ser:</p>

-   Uma **ISO**: arquivo de imagem de disco que contém o instalador de um sistema operacional.
-   Um **disco virtual pré-instalado**: onde o sistema já está configurado e pronto para uso.

<p align="justify">No VirtualBox, quando falamos de instalar do zero, geralmente utilizamos arquivos <strong>ISO</strong>.</p>
<p align="justify">Essas ISOs funcionam como se fossem o "DVD" de instalação de um sistema operacional, só que em formato digital.</p>
<p align="justify">Ao anexar a ISO à máquina virtual, você inicializa o processo de
instalação como faria em um computador físico.</p>

### 3.2 - Onde Encontrar ISO de Distribuições Linux ?

<p align="justify">As distribuições Linux costumam disponibilizar suas ISOs gratuitamente em seus sites oficiais ou em repositórios espelhados (<strong>mirrors</strong>). Alguns
exemplos:</p>

-   **Ubuntu**:[
    ](https://ubuntu.com/download)[*https://ubuntu.com/download*](https://ubuntu.com/download)
-   **Debian**:
    [*https://www.debian.org/distrib*](https://www.debian.org/distrib)
-   **CentOS Stream**:
    [*https://www.centos.org/download/*](https://www.centos.org/download/)
-   **Fedora**: [*https://getfedora.org*](https://getfedora.org)
-   **Oracle Linux**:
    [*https://yum.oracle.com/oracle-linux-isos.html*](https://yum.oracle.com/oracle-linux-isos.html)

> [!TIP]
> <p align="justify">Sempre baixe de fontes oficiais para evitar imagens modificadas que possam comprometer a segurança da sua VM.</p>

### 3.3 - Escolhendo a ISO do Oracle Linux

<p align="justify">Como objetivo do nosso curso é criar um <strong>servidor web com Oracle Linux</strong>, vamos utilizar a ISO oficial dessa distribuição.</p>

No site da Oracle, existem geralmente dois tipos principais de ISO:

1.  **Full ISO**

    <p align="justify">Contém todos os pacotes necessários para a instalação completa, inclusive em ambientes offline.</p>

    -   Vantagem: não depende da internet para instalar.

    -   Desvantagem: arquivo maior (em torno de 8 GB ou mais).

2.  **Boot ISO (ou Minimal)**

    <p align="justify">Contém apenas o instalador básico, que baixa os pacotes da internet durante a instalação.</p>

    -   Vantagem: arquivo menor (cerca de 1 GB).

    -   Desvantagem: requer conexão com a internet durante a instalação.

<p align="justify">Para este curso, vamos optar pela <strong>Full ISO</strong>, garantindo que todos os recursos estejam disponíveis mesmo sem conexão constante.</p>

### 3.4 - Verificando Integridade (Opcional, Mas Recomendado)

<p align="justify">Ao baixar uma ISO, especialmente de distribuições corporativas como o Oracle Linux, é recomendado verificar sua integridade antes de usá-la. Isso garante que o arquivo não foi corrompido no download ou adulterado.</p>

<p align="justify">O processo envolve comparar o <strong>hash</strong> do arquivo baixado com o hash oficial disponibilizado pelo site da distribuição.</p>

No Linux ou macOS:

```
sha256sum OracleLinux.iso
```

No Windows (PowerShell):

```
Get-FileHash .\\OracleLinux.iso -Algorithm SHA256
```

<p align="justify">Se o resultado for idêntico ao publicado no site, a ISO está íntegra e segura.</p>

### 3.5 - Dica: Sites com VM's Prontas

<p align="justify">Além de instalar do zero usando ISOs, existem sites que oferecem máquinas virtuais já prontas, o que pode economizar tempo em testes e estudos. Alguns exemplos:</p>

-   **OSBoxes** ([*https://www.osboxes.org*](https://www.osboxes.org))\
    Oferece VMs para VirtualBox e VMware de várias distribuições Linux.
-   **VirtualBoxes**
    ([*https://virtualboxes.org/images/*](https://virtualboxes.org/images/))\
    Repositório com imagens de sistemas operacionais para uso direto no
    VirtualBox.
-   **Vagrant Cloud**
    ([*https://app.vagrantup.com/boxes/search*](https://app.vagrantup.com/boxes/search))\
    Mais voltado para automação de ambientes, mas também útil para
    iniciar rapidamente máquinas pré-configuradas.

> [!IMPORTANT]
> 💡 **Observação importante**: <p align="justify">VMs prontas são práticas, mas podem não estar configuradas exatamente como você precisa. Para ambientes de produção ou estudos aprofundados, instalar do zero oferece mais controle sobre o processo.</p>

[Voltar para o início](./README.md)

[Próximo 4 - CRIANDO E INSTALANDO ORACLE LINUX](./modulo_4.md)
