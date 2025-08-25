**SUMÁRIO**

[]{#anchor}

[]{#anchor-1}1 - INTRODUÇÃO AO VIRTUALBOX

**🎯 Objetivo**

[]{#anchor-2}Apresentar o VirtualBox, seus principais casos de uso e
diferenciais para quem deseja criar ambientes virtuais para testes,
desenvolvimento ou aprendizado.** **

[]{#anchor-3}1.1 - O QUÊ É O VIRTUALBOX

O VirtualBox é um software de virtualização de código aberto,
desenvolvido e mantido pela Oracle, que permite criar e gerenciar
máquinas virtuais em seu computador. Em outras palavras, ele possibilita
executar sistemas operacionais adicionais -- chamados de *convidados* --
dentro de um sistema operacional principal -- chamado de *hospedeiro*.

Imagine que você tenha um computador rodando Windows, mas precisa
trabalhar com Linux ou até mesmo com outra versão do próprio Windows.
Com o VirtualBox, você pode criar um ambiente virtual onde esse sistema
extra rodará de forma isolada, sem alterar a configuração principal do
seu computador.

Uma das grandes vantagens do VirtualBox é que ele é multiplataforma:
funciona no Windows, Linux, macOS e até em algumas distribuições
Solaris. Além disso, suporta uma ampla variedade de sistemas
operacionais como convidados, incluindo várias distribuições Linux,
versões do Windows, BSD, e outros sistemas menos comuns.

[]{#anchor-4}1.2 - POR QUE USAR O VIRTUALBOX ?

Existem diversos motivos para escolher o VirtualBox como ferramenta de
virtualização, entre eles:

-   **Custo Zero:** Ele é totalmente gratuito para uso pessoal e
    educacional, com licença GPL (na versão de código aberto).\
-   **Versatilidade:** Permite criar máquinas virtuais para os mais
    variados fins, desde testes de software até simulação de ambientes
    de produção.\
-   **Isolamento e Segurança:** O sistema virtual não interfere
    diretamente no sistema hospedeiro, minimizando riscos de
    instabilidade ou infecção por malware.\
-   **Facilidade de Uso:** Interface intuitiva e recursos que facilitam
    a criação, configuração e gerenciamento de máquinas virtuais.\
-   **Compatibilidade Ampla:** Suporte para vários sistemas
    operacionais, além de recursos como USB pass-through, snapshots e
    compartilhamento de pastas.\

Na prática, usar o VirtualBox significa poder experimentar, testar e
aprender sem comprometer a estabilidade do seu sistema principal. É como
ter vários computadores dentro de um só.

[]{#anchor-5}1.3 - CASOS DE USO COMUNS

O VirtualBox é uma ferramenta versátil, utilizada em diferentes
contextos. Alguns exemplos práticos incluem:

1.  **Ambientes de Desenvolvimento\
    **Desenvolvedores podem criar ambientes controlados para testar
    aplicativos em diferentes sistemas operacionais sem precisar de
    múltiplos computadores físicos.\
2.  **Laboratórios de Teste e Aprendizado\
    **Estudantes e profissionais de TI utilizam o VirtualBox para
    estudar redes, servidores e sistemas operacionais, simulando
    cenários reais de forma segura.\
3.  **Testes de Segurança e Pentest\
    **É possível criar máquinas virtuais para testar ferramentas de
    segurança e realizar auditorias sem colocar em risco o ambiente
    real.\
4.  **Compatibilidade de Software\
    **Softwares antigos ou legados podem ser executados em sistemas
    antigos instalados virtualmente, mesmo que o hardware físico seja
    moderno.\
5.  **Simulação de Ambientes Corporativos\
    **Administradores podem criar múltiplas máquinas virtuais para
    simular servidores e estações de trabalho, facilitando treinamentos
    e testes.

[]{#anchor-6}1.4 - ALTERNATIVAS AO VIRTUALBOX

Embora o VirtualBox seja uma solução muito popular, existem outras
ferramentas de virtualização que podem ser usadas em diferentes
cenários. Entre as principais:

-   **VMware Workstation / VMware Player\
    ** Ferramenta robusta e com mais recursos avançados em algumas
    áreas, muito utilizada por profissionais. Possui versão gratuita
    (Player) e versão paga (Workstation Pro).
-   **Microsoft Hyper-V\
    ** Integrado ao Windows 10/11 Pro e Windows Server, é uma solução de
    virtualização da própria Microsoft, focada em ambientes
    corporativos.
-   **Proxmox VE\
    ** Plataforma de virtualização e gerenciamento de contêineres
    baseada em Linux, muito utilizada em servidores.
-   **KVM (Kernel-based Virtual Machine)\
    ** Tecnologia nativa do Linux para virtualização, indicada para
    usuários avançados e ambientes de produção.
-   **Parallels Desktop\
    ** Voltada principalmente para usuários de macOS, permitindo rodar
    Windows e Linux com integração otimizada.

Cada alternativa tem seus pontos fortes e fracos. O VirtualBox se
destaca pela facilidade de uso, compatibilidade, custo zero e grande
comunidade de suporte.

[]{#anchor-7}2 - INSTALAÇÃO E CONFIGURAÇÃO INICIAL

**🎯 Objetivo**

Guiar o aluno na instalação do VirtualBox e na criação do ambiente
básico para executar máquinas virtuais.

[]{#anchor-8}2.1 - REQUISITOS

Antes de instalar o VirtualBox, é importante verificar se seu computador
atende aos requisitos mínimos para executar máquinas virtuais de forma
satisfatória:

-   **Sistema Operacional Hospedeiro**: Windows 8 ou superior, macOS
    10.13 ou superior, distribuições Linux modernas ou Solaris.\
-   **Processador**: Arquitetura x86 de 64 bits, com suporte a
    virtualização por hardware (*Intel VT-x* ou *AMD-V*) ativada na
    BIOS/UEFI.\
-   **Memória RAM**: Mínimo de 4 GB (o ideal é ter 8 GB ou mais para
    trabalhar com várias VMs).\
-   **Armazenamento**: Espaço livre suficiente para armazenar discos
    virtuais e snapshots (mínimo recomendado: 20 GB livres).\
-   **Conexão com a Internet**: Necessária para baixar o instalador e
    eventuais pacotes de extensão.\

💡 **Dica**: Caso sua CPU tenha suporte a virtualização, mas ela esteja
desativada, será necessário habilitar a função na BIOS/UEFI antes de
prosseguir.

[]{#anchor-9}2.2 - BAIXANDO O VIRTUALBOX

O VirtualBox pode ser baixado diretamente do site oficial da Oracle:

1.  Acesse: https://www.virtualbox.org

2.  No menu lateral, clique em **Downloads**.

3.  Escolha o pacote adequado ao seu sistema operacional hospedeiro:

    -   **Windows hosts**

    -   **macOS hosts**

    -   **Linux distributions**

4.  (Opcional) Baixe também o **Extension Pack**, que adiciona recursos
    como suporte a USB 2.0/3.0, inicialização via PXE e criptografia de
    disco.

💡 **Importante**: Sempre utilize a versão mais recente, pois ela contém
correções de segurança e melhorias de desempenho.

[]{#anchor-10}2.3 - INSTALANDO O VIRTUALBOX

O processo de instalação é simples, mas varia levemente conforme o
sistema hospedeiro.

**No Windows:**

-   Execute o instalador .exe baixado.
-   Aceite os termos de licença.
-   Escolha os componentes a instalar (mantenha as opções padrão).
-   Defina o local de instalação.
-   Clique em **Install** e aguarde a conclusão.
-   Ao final, o VirtualBox estará pronto para uso.

**No Linux:**

Em distribuições baseadas no Debian/Ubuntu:\
\
sudo apt update

sudo apt install virtualbox

Ou instale manualmente baixando o pacote .deb no site.

Em Fedora/Red Hat:\
sudo dnf install VirtualBox

**No macOS:**

-   Baixe o arquivo .dmg.
-   Arraste o ícone do VirtualBox para a pasta **Aplicativos**.
-   Caso o sistema bloqueie a instalação, libere o aplicativo em
    **Preferências do Sistema → Segurança e Privacidade**.

[]{#anchor-11}2.4 - PRIMEIROS PASSOS

Ao abrir o VirtualBox pela primeira vez, você verá uma interface limpa,
dividida em:

-   **Lista de Máquinas Virtuais** (à esquerda)
-   **Painel de Detalhes e Configurações** (à direita)

Neste ponto, o VirtualBox está vazio, aguardando a criação da sua
primeira máquina virtual.\
Antes disso, é recomendável acessar **Arquivo → Preferências** e
ajustar:

-   **Pasta padrão de VMs** (onde serão salvos os discos virtuais)
-   **Idioma** (se necessário)
-   **Atualizações** (ativar para receber notificações)

[]{#anchor-12}2.5 - CRIANDO SUA PRIMEIRA VM

Vamos criar uma máquina virtual passo a passo:

1.  Clique no botão **Novo**.

2.  Informe um **nome** (ex: *OracleLinux-Server*).

3.  Escolha o **tipo** e **versão** do sistema operacional (ex: Linux →
    Oracle Linux 64-bit).

4.  Defina a quantidade de **RAM** (mínimo 2 GB para uso básico, 4 GB
    para desempenho melhor).

5.  Crie um **disco rígido virtual**:

    -   Tipo: VDI (VirtualBox Disk Image)

    -   Armazenamento: Dinamicamente alocado

    -   Tamanho: mínimo 20 GB (ajuste conforme necessidade)

6.  Finalize e sua VM estará listada na interface principal.

💡 **Dica**: Use nomes descritivos para evitar confusão caso trabalhe
com várias VMs.

[]{#anchor-13}2.6 - CONFIGURAÇÕES ADICIONAIS

Antes de iniciar a máquina virtual, é interessante ajustar alguns
parâmetros:

-   **Processadores**: Alocar mais núcleos (2 ou mais, se disponíveis)
    melhora o desempenho.

-   **Placa de Rede**:

    -   *NAT*: Mais simples, acesso à internet garantido.

    -   *Bridge*: Torna a VM parte da mesma rede do hospedeiro, ideal
        > para servidores.

-   **Armazenamento**: Conectar a imagem ISO do sistema operacional que
    será instalado.

-   **USB**: Ativar suporte a dispositivos USB (requer Extension Pack).

-   **Pastas Compartilhadas**: Facilita a troca de arquivos entre o host
    e a VM.

[]{#anchor-14}2.7 - SNAPSHOTS

Snapshots são "fotos" do estado atual de uma máquina virtual, incluindo
configurações, disco e memória. Eles permitem voltar exatamente ao ponto
salvo, sendo extremamente úteis para testes e aprendizado.

**Como criar um snapshot:**

1.  Selecione a VM.
2.  Vá em **Máquina → Tirar Instantâneo**.
3.  Dê um nome e, se quiser, uma descrição.

💡 **Exemplo prático**: Antes de instalar um novo software no servidor,
crie um snapshot. Se algo der errado, basta restaurar e a VM volta ao
estado anterior.

[]{#anchor-15}3 - TEMPLATES E SISTEMAS LINUX

**🎯 Objetivo**

Apresentar o conceito de templates, mostrar onde encontrar distribuições
Linux confiáveis e preparar o ISO que será usado na criação da máquina
virtual.

[]{#anchor-16}3.1 - O QUE SÃO TEMPLATES (OU ISOS) ?

No contexto de virtualização, um **template** é um modelo pronto para
criar uma nova máquina virtual. Ele pode ser:

-   Uma **ISO**: arquivo de imagem de disco que contém o instalador de
    um sistema operacional.
-   Um **disco virtual pré-instalado**: onde o sistema já está
    configurado e pronto para uso.

No VirtualBox, quando falamos de instalar do zero, geralmente utilizamos
arquivos **ISO**.\
Essas ISOs funcionam como se fossem o "DVD" de instalação de um sistema
operacional, só que em formato digital.\
Ao anexar a ISO à máquina virtual, você inicializa o processo de
instalação como faria em um computador físico.

[]{#anchor-17}3.2 - ONDE ENCONTRAR ISO DE DISTRIBUIÇÕES LINUX ?

As distribuições Linux costumam disponibilizar suas ISOs gratuitamente
em seus sites oficiais ou em repositórios espelhados (*mirrors*). Alguns
exemplos:

-   **Ubuntu**:[
    ](https://ubuntu.com/download)[*https://ubuntu.com/download*](https://ubuntu.com/download)
-   **Debian**:
    [*https://www.debian.org/distrib*](https://www.debian.org/distrib)
-   **CentOS Stream**:
    [*https://www.centos.org/download/*](https://www.centos.org/download/)
-   **Fedora**: [*https://getfedora.org*](https://getfedora.org)
-   **Oracle Linux**:
    [*https://yum.oracle.com/oracle-linux-isos.html*](https://yum.oracle.com/oracle-linux-isos.html)

💡 **Dica**: Sempre baixe de fontes oficiais para evitar imagens
modificadas que possam comprometer a segurança da sua VM.

[]{#anchor-18}3.3 - ESCOLHENDO A ISO DO ORACLE LINUX

Como objetivo do nosso curso é criar um **servidor web com Oracle
Linux**, vamos utilizar a ISO oficial dessa distribuição.

No site da Oracle, existem geralmente dois tipos principais de ISO:

1.  **Full ISO\
    **Contém todos os pacotes necessários para a instalação completa,
    inclusive em ambientes offline.

    -   Vantagem: não depende da internet para instalar.

    -   Desvantagem: arquivo maior (em torno de 8 GB ou mais).

2.  **Boot ISO (ou Minimal)\
    **Contém apenas o instalador básico, que baixa os pacotes da
    internet durante a instalação.

    -   Vantagem: arquivo menor (cerca de 1 GB).

    -   Desvantagem: requer conexão com a internet durante a instalação.

Para este curso, vamos optar pela **Full ISO**, garantindo que todos os
recursos estejam disponíveis mesmo sem conexão constante.

[]{#anchor-19}3.4 - VERIFICANDO INTEGRIDADE (OPCIONAL, MAS RECOMENDADO)

Ao baixar uma ISO, especialmente de distribuições corporativas como o
Oracle Linux, é recomendado verificar sua integridade antes de usá-la.
Isso garante que o arquivo não foi corrompido no download ou adulterado.

O processo envolve comparar o **hash** do arquivo baixado com o hash
oficial disponibilizado pelo site da distribuição.\
No Linux ou macOS:

sha256sum OracleLinux.iso

No Windows (PowerShell):

Get-FileHash .\\OracleLinux.iso -Algorithm SHA256

Se o resultado for idêntico ao publicado no site, a ISO está íntegra e
segura.

[]{#anchor-20}3.5 - DICA: SITES COM VMS PRONTAS

Além de instalar do zero usando ISOs, existem sites que oferecem
máquinas virtuais já prontas, o que pode economizar tempo em testes e
estudos. Alguns exemplos:

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

💡 **Observação importante**: VMs prontas são práticas, mas podem não
estar configuradas exatamente como você precisa. Para ambientes de
produção ou estudos aprofundados, instalar do zero oferece mais controle
sobre o processo.

[]{#anchor-21}

[]{#anchor-22}4 - CRIANDO E INSTALANDO ORACLE LINUX

**🎯 Objetivo**

Criar a máquina virtual no VirtualBox e realizar a instalação completa
do Oracle Linux 9.

[]{#anchor-23}4.1 - CRIANDO A MÁQUINA VIRTUAL

Com o VirtualBox aberto, vamos criar a VM que hospedará o Oracle Linux:

1.  Clique no botão **Novo**.

2.  Informe o nome da VM (ex: *OracleLinuxServer*).

3.  Tipo: **Linux**.

4.  Versão: **Oracle (64-bit)** --- se essa opção não aparecer,
    verifique se a virtualização por hardware está ativada na BIOS/UEFI.

5.  Defina a **memória RAM**:

    -   Mínimo: 2048 MB (2 GB)

    -   Ideal para servidor web: 4096 MB (4 GB) ou mais.

6.  Crie o **disco rígido virtual**:

    -   Tipo: **VDI** (VirtualBox Disk Image).

    -   Armazenamento: **Dinamicamente alocado**.

    -   Tamanho: mínimo 20 GB (recomendo 30 GB para evitar falta de
        > espaço).

7.  Clique em **Criar**.

💡 **Dica**: Use nomes que facilitem identificar a função da VM,
principalmente se você criar várias no futuro.

[]{#anchor-24}4.2 - CONFIGURANDO A ISO PARA BOOT

Para instalar o Oracle Linux, precisamos carregar a ISO no drive virtual
da VM:

1.  Selecione a VM recém-criada e clique em **Configurações**.
2.  Vá até **Armazenamento**.
3.  No controlador *IDE/SATA*, clique no ícone de disco vazio.
4.  Clique no ícone de disco ao lado de "Atributos" e selecione
    **Escolher um arquivo de disco óptico**.
5.  Localize e selecione a ISO do Oracle Linux baixada no capítulo
    anterior.
6.  Salve as alterações.

[]{#anchor-25}4.3 - AJUSTES RECOMENDADOS NA VM

Antes de iniciar a instalação, vale fazer alguns ajustes para melhor
desempenho e compatibilidade:

-   **Processador**: Em *Sistema → Processador*, aloque pelo menos 2
    CPUs.

-   **Placa de Rede**:

    -   Para este curso, use **Placa em modo Bridge**, assim o servidor
        > poderá ter um IP visível na mesma rede do seu computador
        > hospedeiro.

-   **Vídeo**: Em *Tela*, defina pelo menos 16 MB de memória de vídeo
    (para interface gráfica).

-   **Pasta Compartilhada** (opcional): Configure se quiser trocar
    arquivos facilmente entre host e VM.

💡 **Atenção**: Alocar mais recursos do que o host pode suportar pode
causar lentidão tanto na VM quanto no seu sistema principal.

[]{#anchor-26}4.4 - INICIANDO A INSTALAÇÃO

1.  Com a ISO já configurada, clique em Iniciar para ligar a VM.
2.  O VirtualBox exibirá a tela inicial de boot da instalação do Oracle
    Linux.
3.  Escolha Install Oracle Linux usando as setas e pressione Enter.

[]{#anchor-27}4.5 - PASSOS DA INSTALAÇÃO (GUI)

O instalador do Oracle Linux (baseado no Anaconda) é intuitivo e
funciona por etapas:

1.  **Idioma e Layout do Teclado**

    -   Selecione Português (Brasil) ou English (US), conforme preferir.

2.  **Configuração de Data/Hora**

    -   Ajuste para seu fuso horário.

3.  **Destino de Instalação**

    -   Selecione o disco virtual criado.

    -   Mantenha a opção de particionamento automático (recomendado para
        > iniciantes).

4.  **Rede e Nome do Host**

    -   Ative a interface de rede.

    -   Defina um hostname (ex: oraclelinux.local).

5.  **Software**

    -   Escolha "Servidor com GUI" ou "Servidor Minimal" dependendo da
        > sua preferência.\
        > (Neste curso, usaremos "Servidor Minimal" para aprender a
        > trabalhar via terminal.)

6.  **Senha de Root**

    -   Defina uma senha forte.

7.  **Criação de Usuário**

    -   Opcionalmente, crie um usuário comum com privilégios
        > administrativos.

Após configurar todos os itens, clique em Iniciar Instalação.

[]{#anchor-28}4.6 - AGUARDANDO E FINALIZANDO

O processo de instalação pode levar alguns minutos. Durante esse tempo:

-   O instalador copia arquivos.
-   Configura pacotes básicos.
-   Ajusta o bootloader.

Quando a instalação terminar:

1.  Clique em **Reboot** para reiniciar.

2.  Antes de reiniciar, **remova a ISO** do drive virtual para evitar
    que o sistema inicialize novamente o instalador:

    -   Configurações → Armazenamento → Remover disco da unidade
        > virtual.

[]{#anchor-29}4.7 - PRIMEIRO LOGIN

Com a instalação concluída:

1.  A VM exibirá a tela de login no terminal.
2.  Entre como root usando a senha definida.

Verifique as informações básicas do sistema:\
hostnamectl

Teste a conectividade com a internet:\
ping -c 4 google.com

Atualize o sistema (boa prática inicial):\
\
dnf update -y

A partir daqui, a VM já está pronta para receber as configurações de
rede e a instalação de serviços como o Nginx, que abordaremos nos
próximos capítulos.

[]{#anchor-30}5 - CONFIGURANDO REDE COM IP FIXO

**🎯 Objetivo**

Ensinar como configurar um endereço IP fixo dentro da máquina virtual
com Oracle Linux, para que seja possível acessá-la sempre pelo mesmo IP,
inclusive via navegador no host.

[]{#anchor-31}5.1 - MODOS DE REDE DO VIRTUALBOX

O VirtualBox oferece diferentes modos de rede, cada um com finalidades
específicas. Os principais são:

1.  **NAT (Network Address Translation)**

    -   Mais simples e padrão ao criar uma VM.

    -   Permite que a VM acesse a internet usando o IP do hospedeiro.

    -   Ideal para navegação e downloads, mas não facilita o acesso à VM
        > a partir do host ou de outros dispositivos da rede.

2.  **Bridge (Placa em modo bridge)**

    -   Conecta a VM diretamente à rede física do host.

    -   A VM recebe um IP da mesma faixa que o computador físico.

    -   Facilita o acesso de outros dispositivos da rede local.

3.  **Host-Only**

    -   Cria uma rede isolada entre o host e a VM.

    -   Não tem acesso à internet (a menos que combinada com outra placa
        > de rede).

    -   Excelente para testes locais e simulação de ambientes
        > controlados.

4.  **Rede Interna**

    -   Permite comunicação apenas entre VMs que usam a mesma rede
        > interna.

    -   Sem acesso ao host nem à internet.

💡 **Neste curso**, vamos usar o **Host-Only** para acesso direto do
host ao servidor, garantindo estabilidade de IP.

[]{#anchor-32}5.2 - CRIANDO REDE HOST-ONLY

Para criar uma rede Host-Only no VirtualBox:

1.  No VirtualBox, vá em **Arquivo → Gerenciador de Rede de
    Hospedeiros**.

2.  Clique em **Criar**.

3.  Configure:

    -   **IPv4**: 192.168.56.1 (padrão do VirtualBox, pode ser alterado)

    -   **Máscara de Sub-rede**: 255.255.255.0

4.  (Opcional) Desative o servidor DHCP, pois configuraremos IP fixo
    manualmente na VM.

5.  Salve as configurações.

[]{#anchor-33}5.3 - CONFIGURANDO A VM PARA USAR HOST-ONLY

Agora, vamos conectar nossa VM à rede recém-criada:

1.  Selecione a VM e clique em **Configurações → Rede**.

2.  No **Adaptador 1**:

    -   Marque "Ativar Placa de Rede".

    -   Modo de Conexão: **Rede Apenas do Hospedeiro (Host-Only)**.

    -   Escolha a placa criada no passo anterior.

3.  (Opcional) Para que a VM também tenha internet, adicione um
    **Adaptador 2** configurado como **NAT**.

💡 Essa configuração com dois adaptadores é muito usada em servidores
virtuais:

-   Adaptador 1 (Host-Only) → comunicação direta host ↔ VM
-   Adaptador 2 (NAT) → acesso à internet pela VM

[]{#anchor-34}5.4 - CONFIGURANDO IP FIXO NO ORACLE LINUX

Com a rede Host-Only funcionando, vamos fixar um IP no Oracle Linux:

1.  Entre na VM com usuário root ou use sudo.
2.  Liste as interfaces de rede:

nmcli device status

1.  Localize a interface correspondente ao Host-Only (geralmente enp0s3
    ou enp0s8).
2.  Configure o IP fixo:

nmcli con mod enp0s3 ipv4.addresses 192.168.56.10/24

nmcli con mod enp0s3 ipv4.method manual

nmcli con mod enp0s3 connection.autoconnect yes

nmcli con up enp0s3

1.  -   IP: 192.168.56.10 (na mesma faixa do adaptador Host-Only)

    -   Máscara: /24 equivale a 255.255.255.0

    -   Sem gateway, pois a conexão é apenas entre host e VM.

```{=html}
<!-- -->
```
1.  Para confirmar:\
    ip addr show enp0s3

[]{#anchor-35}5.5 - TESTANDO CONECTIVIDADE

No host (seu computador físico), abra o terminal ou prompt de comando e
teste o acesso à VM:

ping 192.168.56.10

Se a resposta for positiva, a comunicação está funcionando.

💡 Testes adicionais:

Do host, tente acessar via SSH (caso esteja instalado):\
ssh root@192.168.56.10

Na VM, tente pingar o host:\
ping 192.168.56.1

Se tudo estiver certo, sua VM já tem um IP fixo e está acessível
diretamente pelo host, o que será fundamental para instalar e testar o
servidor web.

[]{#anchor-36}6 - INSTALANDO O SERVIÇO NGINX

**🎯 Objetivo**

Instalar e iniciar o serviço nginx dentro da VM Oracle Linux, permitindo
acesso a uma página web de teste a partir do navegador da máquina host.

[]{#anchor-37}6.1 - O QUE É O NGINX ?

O **Nginx** (pronuncia-se "engine-x") é um servidor web de alto
desempenho, amplamente utilizado para hospedar sites, APIs e aplicações
web. Além de servir conteúdo estático, ele também atua como proxy
reverso, balanceador de carga e cache de conteúdo.

Entre suas principais vantagens:

-   Leve e rápido, mesmo com alto volume de conexões.
-   Fácil configuração.
-   Muito utilizado em ambientes corporativos e na nuvem.
-   Excelente integração com aplicações em PHP, Python, Node.js e
    outros.

💡 **Curiosidade**: o Nginx está presente em grandes serviços como
Netflix, Dropbox e WordPress.com.

[]{#anchor-38}6.2 - ATUALIZANDO OS PACOTES

Antes de instalar qualquer software, é recomendável atualizar a lista de
pacotes e aplicar correções de segurança:

dnf update -y

Esse comando garante que você está usando as versões mais recentes dos
pacotes do sistema, evitando incompatibilidades.

[]{#anchor-39}6.3 - INSTALANDO O NGINX

No Oracle Linux, o Nginx está disponível nos repositórios padrão:

dnf install nginx -y

Após a instalação, os arquivos principais do Nginx ficam localizados em:

-   Arquivo de configuração principal: /etc/nginx/nginx.conf
-   Diretório de páginas padrão: /usr/share/nginx/html/
-   Arquivos de log: /var/log/nginx/

[]{#anchor-40}6.4 - INICIANDO O SERVIÇO NGINX

Para iniciar o servidor web:

systemctl start nginx

Se quiser que o Nginx seja iniciado automaticamente junto com o sistema:

systemctl enable nginx

[]{#anchor-41}6.5 - VERIFICANDO O STATUS

Podemos confirmar se o Nginx está rodando com:

systemctl status nginx

O resultado esperado deve indicar active (running).

Outra forma de verificar é testando a porta 80 internamente:

curl <http://localhost>

Se o Nginx estiver ativo, o comando retornará o conteúdo da página
padrão.

[]{#anchor-42}6.6 - AJUSTANDO O FIREWALL

Se o firewall estiver ativo, precisamos liberar a porta 80 (HTTP) para
permitir conexões externas:

firewall-cmd \--permanent \--zone=public \--add-service=http

firewall-cmd \--reload

💡 Nota: Se for usar HTTPS futuramente, também será necessário liberar a
porta 443.

[]{#anchor-43}6.7 - ACESSANDO PELO NAVEGADOR (MÁQUINA HOST)

Com o Nginx rodando e o firewall configurado, já podemos acessar a
página inicial no navegador do host.

1.  Abra seu navegador.\
2.  Digite o IP fixo configurado no capítulo anterior:

[*http://192.168.56.10*](http://192.168.56.10)

1.  Você deverá ver a página padrão do Nginx com a mensagem **\"Welcome
    to Nginx!\"**.\

Se a página aparecer, significa que:

-   O Nginx está instalado e ativo.\
-   A rede Host-Only está configurada corretamente.\
-   O servidor web está acessível pelo host.

[]{#anchor-44}7 - CRIANDO URL AMIGÁVEL NO HOST

**🎯 Objetivo**

Ensinar como configurar uma URL personalizada (como meuservidor.local)
na máquina host, apontando para o IP da VM, facilitando o acesso ao
serviço web no navegador.

[]{#anchor-45}7.1 - O PROBLEMA DE USAR IPS

Até aqui, para acessar nosso servidor web, utilizamos um endereço IP,
por exemplo:

[*http://192.168.56.10*](http://192.168.56.10)

Embora funcional, esse método apresenta alguns inconvenientes:

-   É difícil lembrar endereços numéricos.\
-   Caso o IP seja alterado (em configurações dinâmicas), o link deixará
    de funcionar.\
-   Em ambientes com vários serviços, ter que lembrar cada IP se torna
    confuso.\

Em um ambiente de produção, usuários não acessam sistemas via IP ---
eles usam **nomes de domínio** (URLs), como www.exemplo.com.

[]{#anchor-46}7.2 - SOLUÇÃO: USAR O ARQUIVO hosts

Para simular um nome de domínio no seu computador **sem depender de um
DNS externo**, podemos usar o **arquivo hosts** do sistema operacional.

O **arquivo hosts** funciona como um mini-servidor DNS local:

-   Ele permite mapear um nome de domínio para um endereço IP
    específico.\
-   Esse mapeamento vale apenas para o computador onde o arquivo foi
    modificado.\

No Windows, o arquivo hosts fica em:

C:\\Windows\\System32\\drivers\\etc\\hosts

No Linux e macOS, o caminho é:

/etc/hosts

[]{#anchor-47}7.3 - CRIANDO O MAPEAMENTO

Vamos supor que o IP fixo configurado no capítulo anterior foi
192.168.56.10 e queremos criar a URL amigável meuservidor.local.

1.  Abrir o arquivo hosts como administrador:\

    -   No Windows: abrir o Bloco de Notas como Administrador e carregar
        > o arquivo hosts.\

    -   No Linux/macOS: abrir com sudo nano /etc/hosts.\

2.  Adicionar uma nova linha no final:

192.168.56.10 meuservidor.local

1.  Salvar o arquivo.\

Agora, quando o navegador tentar acessar meuservidor.local, ele será
direcionado automaticamente para o IP 192.168.56.10.

[]{#anchor-48}7.4 - ACESSANDO O SERVIÇO PELO NAVEGADOR

Após salvar a modificação no arquivo hosts:

-   Abra o navegador e digite:

[*http://meuservidor.local*](http://meuservidor.local)

-   A página padrão do Nginx deverá aparecer, assim como aparecia com o
    IP.\

💡 **Nota**: Esse processo só funciona no computador onde você alterou o
arquivo hosts. Se quiser que outros dispositivos da rede também
reconheçam o nome, será necessário alterar o hosts deles ou configurar
um DNS local.

[]{#anchor-49}7.5 - DICAS PARA NOMES MAIS PROFISSIONAIS

Ao escolher um nome para o seu servidor local, considere:

-   Usar um **sufixo não público** para evitar conflitos com sites
    reais. Exemplos: .local, .test, .lab.\

-   Evitar caracteres especiais e acentos.\

-   Criar nomes curtos e objetivos. Exemplos:\

    -   webserver.local\

    -   nginx.lab\

    -   projeto1.test\

Em ambientes profissionais, o uso de **DNS interno** é a prática
recomendada, mas para estudos e testes, o arquivo hosts é suficiente.

[]{#anchor-50}8 - ENCERRAMENTO E PRÓXIMOS PASSOS

**🎯 Finalizando**

Aqui encerramos o mini curso com dicas para aprofundamento, backup da VM
e próximos passos no mundo da virtualização e infraestrutura.

[]{#anchor-51}8.1 - O QUE FOI CONSTRUÍDO

Ao longo deste curso, você saiu do zero e construiu um ambiente
funcional de servidor web dentro do **VirtualBox**, utilizando o
**Oracle Linux** e o **Nginx**.

Relembrando as etapas principais:

-   Compreendeu os conceitos de **virtualização** e os benefícios do
    VirtualBox como ferramenta de laboratório.\
-   Criou e configurou uma **máquina virtual** personalizada para
    hospedar um servidor Linux.\
-   Instalou o **Oracle Linux**, configurou rede **Host-Only** e
    atribuiu **IP fixo** ao servidor.\
-   Instalou e configurou o **Nginx**, garantindo que o serviço
    estivesse acessível pelo navegador do host.\
-   Configurou uma **URL amigável** para substituir o acesso via IP,
    simulando um ambiente mais próximo do mundo real.\

Com isso, você já tem uma base sólida para criar e gerenciar servidores
virtuais.

[]{#anchor-52}8.2 - EXPORTANDO SUA VM

Uma das grandes vantagens de usar o VirtualBox é a possibilidade de
**exportar** suas máquinas virtuais e reutilizá-las ou compartilhá-las.

Para exportar sua VM:

1.  No VirtualBox, selecione a VM.\
2.  Vá em **Arquivo \> Exportar Appliance**.\
3.  Escolha o formato OVF ou OVA (mais comum).\
4.  Salve o arquivo resultante.\

Benefícios:

-   Backup fácil do seu ambiente.\
-   Possibilidade de transportar seu servidor para outro computador.\
-   Criação de **templates** para futuros projetos.

[]{#anchor-53}8.3 - DICAS PARA PRÓXIMOS PROJETOS

Agora que você domina o básico, aqui estão algumas ideias para continuar
aprendendo:

-   **Instalar bancos de dados** como MySQL, PostgreSQL ou MariaDB.\
-   Configurar **PHP** ou **Node.js** e hospedar aplicações dinâmicas.\
-   Criar múltiplas VMs e simular uma rede interna com vários serviços.\
-   Estudar **Docker** e compará-lo com máquinas virtuais.\
-   Implementar HTTPS com **certificados TLS**.\
-   Criar um servidor DNS interno para simular um ambiente corporativo.\

A ideia é que você use essa mesma base para explorar novas tecnologias e
aprofundar seu conhecimento em administração de sistemas.

[]{#anchor-54}8.4 - CONVITE DA IAMANDU TECH ACADEMY

Parabéns por concluir este treinamento!\
Na **IAMANDU Tech Academy**, acreditamos que a prática é o melhor
caminho para dominar a tecnologia. Se este curso foi útil para você,
saiba que temos outros treinamentos voltados para:

-   Administração de servidores Linux.\
-   Segurança da informação.\
-   Redes e serviços corporativos.\
-   Desenvolvimento web e DevOps.\

Continue evoluindo. Cada projeto que você cria é um passo para se tornar
um profissional mais completo e competitivo no mercado de TI.

[]{#anchor-55}

[]{#anchor-56}9 - REFERÊNCIAS

COYLE DANIEL. **Equipes Brilhantes: As três habilidades essenciais para
criar organizações bem-sucedidas **2019

FORSGREN NICOLE, HUMBLE JEZ, KIM GENE. **Accelerate **2018

REDOCLY. Make API docs your superpower. Disponível em:
[*https://redocly.com/*](https://redocly.com/), Acesso em: xx de Abril
de 2023.

DOPPLER. Documentaion Hub. Disponível em:
[*https://docs.doppler.com/docs*](https://docs.doppler.com/docs), Acesso
em: xx de Abril de 2023.
