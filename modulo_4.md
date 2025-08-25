[Voltar para o início](./README.md)

## Módulo 4 - Criando e Instalando Oracle Linux

**🎯 Objetivo**

<p align="justify">Criar a máquina virtual no VirtualBox e realizar a instalação completa do Oracle Linux 9.</p>

### 4.1 - Criando A Máquina Virtual

<p align="justify">Com o VirtualBox aberto, vamos criar a VM que hospedará o Oracle Linux:</p>

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

> [!TIP]
> 💡 **Dica**: Use nomes que facilitem identificar a função da VM,
principalmente se você criar várias no futuro.

### 4.2 - Configurando a ISO para Boot

<p align="justify">Para instalar o Oracle Linux, precisamos carregar a ISO no drive virtual da VM:</p>

1.  Selecione a VM recém-criada e clique em **Configurações**.
2.  Vá até **Armazenamento**.
3.  No controlador *IDE/SATA*, clique no ícone de disco vazio.
4.  Clique no ícone de disco ao lado de "Atributos" e selecione **Escolher um arquivo de disco óptico**.
5.  Localize e selecione a ISO do Oracle Linux baixada no capítulo anterior.
6.  Salve as alterações.

### 4.3 - Ajustes Recomendados na VM

<p align="justify">Antes de iniciar a instalação, vale fazer alguns ajustes para melhor desempenho e compatibilidade:</p>

-   **Processador**: Em *Sistema → Processador*, aloque pelo menos 2
    CPUs.

-   **Placa de Rede**:

    -   Para este curso, use **Placa em modo Bridge**, assim o servidor poderá ter um IP visível na mesma rede do seu computador hospedeiro.

-   **Vídeo**: Em *Tela*, defina pelo menos 16 MB de memória de vídeo
    (para interface gráfica).

-   **Pasta Compartilhada** (opcional): Configure se quiser trocar
    arquivos facilmente entre host e VM.

> [!WARNING]
> 💡 **Atenção**: Alocar mais recursos do que o host pode suportar pode causar lentidão tanto na VM quanto no seu sistema principal.

### 4.4 - Iniciando a Instalação

1.  Com a ISO já configurada, clique em Iniciar para ligar a VM.
2.  O VirtualBox exibirá a tela inicial de boot da instalação do Oracle Linux.
3.  Escolha Install Oracle Linux usando as setas e pressione Enter.

### 4.5 - Passos da Instalação (GUI)

<p align="justify">O instalador do Oracle Linux (baseado no Anaconda) é intuitivo e funciona por etapas:</p>

1.  **Idioma e Layout do Teclado**

    -   Selecione Português (Brasil) ou English (US), conforme preferir.

2.  **Configuração de Data/Hora**

    -   Ajuste para seu fuso horário.

3.  **Destino de Instalação**

    -   Selecione o disco virtual criado.
    -   Mantenha a opção de particionamento automático (recomendado para iniciantes).

4.  **Rede e Nome do Host**

    -   Ative a interface de rede.
    -   Defina um hostname (ex: oraclelinux.local).

5.  **Software**

    -   Escolha "Servidor com GUI" ou "Servidor Minimal" dependendo da sua preferência.\
        (Neste curso, usaremos "Servidor Minimal" para aprender a trabalhar via terminal.)

6.  **Senha de Root**

    -   Defina uma senha forte.

7.  **Criação de Usuário**

    -   Opcionalmente, crie um usuário comum com privilégios administrativos.

<p align="justify">Após configurar todos os itens, clique em Iniciar Instalação.</p>

### 4.6 - Aguardando e Finalizando

<p align="justify">O processo de instalação pode levar alguns minutos. Durante esse tempo:</p>

-   O instalador copia arquivos.
-   Configura pacotes básicos.
-   Ajusta o bootloader.

Quando a instalação terminar:

1.  Clique em **Reboot** para reiniciar.

2.  Antes de reiniciar, **remova a ISO** do drive virtual para evitar que o sistema inicialize novamente o instalador:

    -   Configurações → Armazenamento → Remover disco da unidade virtual.

### 4.7 - Primeiro Login

<p align="justify">Com a instalação concluída:</p>

1.  A VM exibirá a tela de login no terminal.
2.  Entre como root usando a senha definida.

<p align="justify">Verifique as informações básicas do sistema:</p>

```
hostnamectl
```

<p align="justify">Teste a conectividade com a internet:</p>

```
ping -c 4 google.com
```

<p align="justify">Atualize o sistema (boa prática inicial):</p>

```
dnf update -y
```

<p align="justify">A partir daqui, a VM já está pronta para receber as configurações de rede e a instalação de serviços como o Nginx, que abordaremos nos próximos capítulos.</p>

[Voltar para o início](./README.md)

[Próximo 5 - CONFIGURANDO REDE COM IP FIXO](./modulo_5.md)
