# Iamandu Tech - VirtualBox do Zero ao Web Server

## Módulo 1 – Introdução ao VirtualBox

🎯 Objetivo
Apresentar o VirtualBox, seus principais casos de uso e diferenciais para quem deseja criar ambientes virtuais para testes, desenvolvimento ou aprendizado. 

### 1.1 O que é o VirtualBox ?

O VirtualBox é um software de virtualização de código aberto, desenvolvido e mantido pela Oracle, que permite criar e gerenciar máquinas virtuais em seu computador. Em outras palavras, ele possibilita executar sistemas operacionais adicionais – chamados de convidados – dentro de um sistema operacional principal – chamado de hospedeiro.
Imagine que você tenha um computador rodando Windows, mas precisa trabalhar com Linux ou até mesmo com outra versão do próprio Windows. Com o VirtualBox, você pode criar um ambiente virtual onde esse sistema extra rodará de forma isolada, sem alterar a configuração principal do seu computador.
Uma das grandes vantagens do VirtualBox é que ele é multiplataforma: funciona no Windows, Linux, macOS e até em algumas distribuições Solaris. Além disso, suporta uma ampla variedade de sistemas operacionais como convidados, incluindo várias distribuições Linux, versões do Windows, BSD, e outros sistemas menos comuns.

### 1.2 Por que usar o VirtualBox ?

Existem diversos motivos para escolher o VirtualBox como ferramenta de virtualização, entre eles:

- Custo Zero: Ele é totalmente gratuito para uso pessoal e educacional, com licença GPL (na versão de código aberto).

- Versatilidade: Permite criar máquinas virtuais para os mais variados fins, desde testes de software até simulação de ambientes de produção.

- Isolamento e Segurança: O sistema virtual não interfere diretamente no sistema hospedeiro, minimizando riscos de instabilidade ou infecção por malware.

- Facilidade de Uso: Interface intuitiva e recursos que facilitam a criação, configuração e gerenciamento de máquinas virtuais.

- Compatibilidade Ampla: Suporte para vários sistemas operacionais, além de recursos como USB pass-through, snapshots e compartilhamento de pastas.

Na prática, usar o VirtualBox significa poder experimentar, testar e aprender sem comprometer a estabilidade do seu sistema principal. É como ter vários computadores dentro de um só.

### 1.3 Casos de uso comuns

O VirtualBox é uma ferramenta versátil, utilizada em diferentes contextos. Alguns exemplos práticos incluem:

1 - Ambientes de Desenvolvimento
Desenvolvedores podem criar ambientes controlados para testar aplicativos em diferentes sistemas operacionais sem precisar de múltiplos computadores físicos.

2 - Laboratórios de Teste e Aprendizado
Estudantes e profissionais de TI utilizam o VirtualBox para estudar redes, servidores e sistemas operacionais, simulando cenários reais de forma segura.

3 - Testes de Segurança e Pentest
É possível criar máquinas virtuais para testar ferramentas de segurança e realizar auditorias sem colocar em risco o ambiente real.

4 - Compatibilidade de Software
Softwares antigos ou legados podem ser executados em sistemas antigos instalados virtualmente, mesmo que o hardware físico seja moderno.

5 - Simulação de Ambientes Corporativos
Administradores podem criar múltiplas máquinas virtuais para simular servidores e estações de trabalho, facilitando treinamentos e testes.

### 1.4 Alternativas ao VirtualBox

Embora o VirtualBox seja uma solução muito popular, existem outras ferramentas de virtualização que podem ser usadas em diferentes cenários. Entre as principais:
- VMware Workstation / VMware Player
  Ferramenta robusta e com mais recursos avançados em algumas áreas, muito utilizada por profissionais. Possui versão gratuita (Player) e versão paga (Workstation Pro).
- Microsoft Hyper-V
  Integrado ao Windows 10/11 Pro e Windows Server, é uma solução de virtualização da própria Microsoft, focada em ambientes corporativos.
- Proxmox VE
  Plataforma de virtualização e gerenciamento de contêineres baseada em Linux, muito utilizada em servidores.
- KVM (Kernel-based Virtual Machine)
  Tecnologia nativa do Linux para virtualização, indicada para usuários avançados e ambientes de produção.
- Parallels Desktop
  Voltada principalmente para usuários de macOS, permitindo rodar Windows e Linux com integração otimizada.
Cada alternativa tem seus pontos fortes e fracos. O VirtualBox se destaca pela facilidade de uso, compatibilidade, custo zero e grande comunidade de suporte.

## Módulo 2 – Instalação e Configuração Inicial

🎯 Objetivo
Guiar o aluno na instalação do VirtualBox e na criação do ambiente básico para executar máquinas virtuais.

### 2.1 Requisitos

Sistema Operacional Host: Windows 10/11, macOS ou qualquer distribuição Linux

Requisitos mínimos:

4 GB de RAM (recomendado 8 GB+)

20 GB de espaço em disco livre

Processador com suporte a virtualização (VT-x ou AMD-V)

### 2.2 Baixando o VirtualBox

Acesse o site oficial:
🔗 https://www.virtualbox.org

Clique em “Download VirtualBox”

Selecione o instalador de acordo com seu sistema operacional:

Windows Hosts

OS X Hosts

Linux Distributions

### 2.3 Instalando o VirtualBox

💻 Windows
Execute o instalador baixado (VirtualBox-*.exe)

Avance com as opções padrão

Permita a instalação dos drivers de rede e USB

Finalize e execute o VirtualBox

🐧 Linux (Ubuntu/Debian)

```
sudo apt update sudo apt install virtualbox -y 
```

🍎 macOS
Abra o .dmg e siga as instruções

Permita a execução do software em Segurança e Privacidade, se necessário

### 2.4 Primeiros Passos

Ao abrir o VirtualBox, você verá a tela principal, onde poderá:

Criar novas VMs

Iniciar, pausar ou excluir VMs existentes

Acessar as configurações globais do ambiente

### 2.5 Criando sua Primeira VM (sem instalar ainda)

Clique em “Novo” e preencha:

CampoValor RecomendadoNomeOracleLinux9TipoLinuxVersãoOracle (64-bit)Memória RAM2048 MB (mínimo recomendado)Disco RígidoCriar novo disco virtual VDITamanho do disco20 GB

### 2.6 Configurações adicionais (antes da instalação)

Sistema > Processador: 2 CPUs, se disponíveis

Armazenamento: selecione a ISO do Oracle Linux (no próximo módulo)

Rede: Modo NAT (por padrão) ou Bridge (para acessar via rede local)

Tela: Aumente memória de vídeo para 16–32 MB, se desejar

### 2.7 Snapshots

Antes de instalar ou testar algo mais avançado, crie um snapshot para poder voltar ao estado anterior da VM.

🧠 Dica: Snapshots são como “checkpoints” – úteis antes de atualizações, testes ou alterações arriscadas.

### 🔚 Conclusão dos Módulos 1 e 2
Você agora entende:

O que é o VirtualBox e por que ele é uma ferramenta essencial para qualquer profissional de tecnologia

Como instalar e configurar o VirtualBox no seu sistema

Como criar uma máquina virtual com configurações básicas

Nos próximos módulos, vamos:

👉 Baixar e instalar o Oracle Linux
👉 Configurar o IP fixo da VM
👉 Instalar e expor um serviço nginx para acesso via navegador

