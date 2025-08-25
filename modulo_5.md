[Voltar para o início](./README.md)

## Módulo 5 - Configurando Rede com IP Fixo

**🎯 Objetivo**

<p align="justify">Ensinar como configurar um endereço IP fixo dentro da máquina virtual com Oracle Linux, para que seja possível acessá-la sempre pelo mesmo IP, inclusive via navegador no host.</p>

### 5.1 - Modos de Rede do Virtualbox

<p align="justify">O VirtualBox oferece diferentes modos de rede, cada um com finalidades específicas. Os principais são:</p>

1.  **NAT (Network Address Translation)**
    -   Mais simples e padrão ao criar uma VM.
    -   Permite que a VM acesse a internet usando o IP do hospedeiro.
    -   Ideal para navegação e downloads, mas não facilita o acesso à VM a partir do host ou de outros dispositivos da rede.

2.  **Bridge (Placa em modo bridge)**
    -   Conecta a VM diretamente à rede física do host.
    -   A VM recebe um IP da mesma faixa que o computador físico.
    -   Facilita o acesso de outros dispositivos da rede local.

3.  **Host-Only**
    -   Cria uma rede isolada entre o host e a VM.
    -   Não tem acesso à internet (a menos que combinada com outra placa de rede).
    -   Excelente para testes locais e simulação de ambientes controlados.

4.  **Rede Interna**
    -   Permite comunicação apenas entre VMs que usam a mesma rede interna.
    -   Sem acesso ao host nem à internet.

> [!NOTE]
> 💡 **Neste curso**, vamos usar o **Host-Only** para acesso direto do host ao servidor, garantindo estabilidade de IP.

### 5.2 - Criando Rede Host-only

<p align="justify">Para criar uma rede Host-Only no VirtualBox:</p>

1.  No VirtualBox, vá em **Arquivo → Gerenciador de Rede de Hospedeiros**.
2.  Clique em **Criar**.
3.  Configure:
    -   **IPv4**: 192.168.56.1 (padrão do VirtualBox, pode ser alterado)
    -   **Máscara de Sub-rede**: 255.255.255.0
4.  (Opcional) Desative o servidor DHCP, pois configuraremos IP fixo manualmente na VM.
5.  Salve as configurações.

### 5.3 - Configurando a VM para usar Host-only

<p align="justify">Agora, vamos conectar nossa VM à rede recém-criada:</p>

1.  Selecione a VM e clique em **Configurações → Rede**.
2.  No **Adaptador 1**:
    -   Marque "Ativar Placa de Rede".
    -   Modo de Conexão: **Rede Apenas do Hospedeiro (Host-Only)**.
    -   Escolha a placa criada no passo anterior.
3.  (Opcional) Para que a VM também tenha internet, adicione um **Adaptador 2** configurado como **NAT**.

💡 Essa configuração com dois adaptadores é muito usada em servidores virtuais:

-   Adaptador 1 (Host-Only) → comunicação direta host ↔ VM
-   Adaptador 2 (NAT) → acesso à internet pela VM

### 5.4 - Configurando IP Fixo no Oracle Linux

<p align="justify">Com a rede Host-Only funcionando, vamos fixar um IP no Oracle Linux:</p>

1.  Entre na VM com usuário root ou use sudo.
2.  Liste as interfaces de rede:

```
nmcli device status
```

1.  Localize a interface correspondente ao Host-Only (geralmente enp0s3 ou enp0s8).
2.  Configure o IP fixo:

```
nmcli con mod enp0s3 ipv4.addresses 192.168.56.10/24
nmcli con mod enp0s3 ipv4.method manual
nmcli con mod enp0s3 connection.autoconnect yes
nmcli con up enp0s3
```

3.  -   IP: 192.168.56.10 (na mesma faixa do adaptador Host-Only)
    -   Máscara: /24 equivale a 255.255.255.0
    -   Sem gateway, pois a conexão é apenas entre host e VM.

4.  Para confirmar:

```
ip addr show enp0s3
```

### 5.5 - Testando Conectividade

<p align="justify">No host (seu computador físico), abra o terminal ou prompt de comando e teste o acesso à VM:</p>

```
ping 192.168.56.10
```

Se a resposta for positiva, a comunicação está funcionando.

💡 Testes adicionais:

Do host, tente acessar via SSH (caso esteja instalado):

```
ssh root@192.168.56.10
```

Na VM, tente pingar o host:

```
ping 192.168.56.1
```

Se tudo estiver certo, sua VM já tem um IP fixo e está acessível diretamente pelo host, o que será fundamental para instalar e testar o servidor web.

[Voltar para o início](./README.md)

[Próximo 6 - INSTALANDO O SERVIÇO NGINX](./modulo_6.md)
