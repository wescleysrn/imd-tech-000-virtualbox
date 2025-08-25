# Iamandu Tech - VirtualBox do Zero ao Web Server

**SUMÁRIO**

[]{#anchor}

[]{#anchor-1}1 - INTRODUÇÃO AO VIRTUALBOX

## Módulo 1 – Introdução ao VirtualBox

**🎯 Objetivo**
<p align="justify">Apresentar o VirtualBox, seus principais casos de uso e diferenciais para quem deseja criar ambientes virtuais para testes, desenvolvimento ou aprendizado.</p> 

### 1.1 O que é o VirtualBox ?

<p align="justify">O VirtualBox é um software de virtualização de código aberto, desenvolvido e mantido pela Oracle, que permite criar e gerenciar máquinas virtuais em seu computador. Em outras palavras, ele possibilita executar sistemas operacionais adicionais – chamados de convidados – dentro de um sistema operacional principal – chamado de hospedeiro.</p>
<p align="justify">Imagine que você tenha um computador rodando Windows, mas precisa trabalhar com Linux ou até mesmo com outra versão do próprio Windows. Com o VirtualBox, você pode criar um ambiente virtual onde esse sistema extra rodará de forma isolada, sem alterar a configuração principal do seu computador.</p>
<p align="justify">Uma das grandes vantagens do VirtualBox é que ele é multiplataforma: funciona no Windows, Linux, macOS e até em algumas distribuições Solaris. Além disso, suporta uma ampla variedade de sistemas operacionais como convidados, incluindo várias distribuições Linux, versões do Windows, BSD, e outros sistemas menos comuns.</p>

### 1.2 Por que usar o VirtualBox ?

<p align="justify">Existem diversos motivos para escolher o VirtualBox como ferramenta de virtualização, entre eles:</p>

- **Custo Zero:** <p align="justify">Ele é totalmente gratuito para uso pessoal e educacional, com licença GPL (na versão de código aberto).</p>

- **Versatilidade:** <p align="justify">Permite criar máquinas virtuais para os mais variados fins, desde testes de software até simulação de ambientes de produção.</p>

- **Isolamento e Segurança:** <p align="justify">O sistema virtual não interfere diretamente no sistema hospedeiro, minimizando riscos de instabilidade ou infecção por malware.</p>

- **Facilidade de Uso:** <p align="justify">Interface intuitiva e recursos que facilitam a criação, configuração e gerenciamento de máquinas virtuais.</p>

- **Compatibilidade Ampla:** <p align="justify">Suporte para vários sistemas operacionais, além de recursos como USB pass-through, snapshots e compartilhamento de pastas.</p>

<p align="justify">Na prática, usar o VirtualBox significa poder experimentar, testar e aprender sem comprometer a estabilidade do seu sistema principal. É como ter vários computadores dentro de um só.</p>

### 1.3 Casos de uso comuns

<p align="justify">O VirtualBox é uma ferramenta versátil, utilizada em diferentes contextos. Alguns exemplos práticos incluem:</p>

**1 - Ambientes de Desenvolvimento**
<p align="justify">Desenvolvedores podem criar ambientes controlados para testar aplicativos em diferentes sistemas operacionais sem precisar de múltiplos computadores físicos.</p>

**2 - Laboratórios de Teste e Aprendizado**
<p align="justify">Estudantes e profissionais de TI utilizam o VirtualBox para estudar redes, servidores e sistemas operacionais, simulando cenários reais de forma segura.</p>

**3 - Testes de Segurança e Pentest**
<p align="justify">É possível criar máquinas virtuais para testar ferramentas de segurança e realizar auditorias sem colocar em risco o ambiente real.</p>

**4 - Compatibilidade de Software**
<p align="justify">Softwares antigos ou legados podem ser executados em sistemas antigos instalados virtualmente, mesmo que o hardware físico seja moderno.</p>

**5 - Simulação de Ambientes Corporativos**
<p align="justify">Administradores podem criar múltiplas máquinas virtuais para simular servidores e estações de trabalho, facilitando treinamentos e testes.</p>

### 1.4 Alternativas ao VirtualBox

<p align="justify">Embora o VirtualBox seja uma solução muito popular, existem outras ferramentas de virtualização que podem ser usadas em diferentes cenários. Entre as principais:</p>

- **VMware Workstation / VMware Player**
  <p align="justify">Ferramenta robusta e com mais recursos avançados em algumas áreas, muito utilizada por profissionais. Possui versão gratuita (Player) e versão paga (Workstation Pro).</p>
- **Microsoft Hyper-V**
  <p align="justify">Integrado ao Windows 10/11 Pro e Windows Server, é uma solução de virtualização da própria Microsoft, focada em ambientes corporativos.</p>
- **Proxmox VE**
  <p align="justify">Plataforma de virtualização e gerenciamento de contêineres baseada em Linux, muito utilizada em servidores.</p>
- **KVM (Kernel-based Virtual Machine)**
  <p align="justify">Tecnologia nativa do Linux para virtualização, indicada para usuários avançados e ambientes de produção.</p>
- **Parallels Desktop**
  <p align="justify">Voltada principalmente para usuários de macOS, permitindo rodar Windows e Linux com integração otimizada.</p>

<p align="justify">Cada alternativa tem seus pontos fortes e fracos. O VirtualBox se destaca pela facilidade de uso, compatibilidade, custo zero e grande comunidade de suporte.</p>

## Módulo 2 – Instalação e Configuração Inicial

🎯 Objetivo
<p align="justify">Guiar o aluno na instalação do VirtualBox e na criação do ambiente básico para executar máquinas virtuais.</p>

### 2.1 Requisitos

<p align="justify">Antes de instalar o VirtualBox, é importante verificar se seu computador atende aos requisitos mínimos para executar máquinas virtuais de forma satisfatória:</p>

- **Sistema Operacional Hospedeiro:** <p align="justify">Windows 8 ou superior, macOS 10.13 ou superior, distribuições Linux modernas ou Solaris.</p>
- **Processador:** <p align="justify">Arquitetura x86 de 64 bits, com suporte a virtualização por hardware (Intel VT-x ou AMD-V) ativada na BIOS/UEFI.</p>
- **Memória RAM:** <p align="justify">Mínimo de 4 GB (o ideal é ter 8 GB ou mais para trabalhar com várias VMs).</p>
- **Armazenamento:** <p align="justify">Espaço livre suficiente para armazenar discos virtuais e snapshots (mínimo recomendado: 20 GB livres).</p>
- **Conexão com a Internet:** <p align="justify">Necessária para baixar o instalador e eventuais pacotes de extensão.</p>

> <p align="justify">💡Dica: Caso sua CPU tenha suporte a virtualização, mas ela esteja desativada, será necessário habilitar a função na BIOS/UEFI antes de prosseguir.</p>

### 2.2 Baixando o VirtualBox

<p align="justify">O VirtualBox pode ser baixado diretamente do site oficial da Oracle:</p>

Acesse: https://www.virtualbox.org
No menu lateral, clique em Downloads.
Escolha o pacote adequado ao seu sistema operacional hospedeiro:
Windows hosts
macOS hosts
Linux distributions
(Opcional) Baixe também o Extension Pack, que adiciona recursos como suporte a USB 2.0/3.0, inicialização via PXE e criptografia de disco.
💡 Importante: Sempre utilize a versão mais recente, pois ela contém correções de segurança e melhorias de desempenho.

### 2.3 Instalando o VirtualBox


### 2.4 Primeiros Passos


### 2.5 Criando sua Primeira VM (sem instalar ainda)


### 2.6 Configurações adicionais (antes da instalação)


### 2.7 Snapshots


### 🔚 Conclusão dos Módulos 1 e 2

