# Iamandu Tech - VirtualBox do Zero ao Web Server

## Módulo 1 – Introdução ao VirtualBox

🎯 Objetivo
Apresentar o VirtualBox, seus principais casos de uso e diferenciais para quem deseja criar ambientes virtuais para testes, desenvolvimento ou aprendizado.

### 1.1 O que é o VirtualBox ?

O VirtualBox é um hipervisor de código aberto mantido pela Oracle. Ele permite criar e executar máquinas virtuais (VMs) em diferentes sistemas operacionais (Windows, Linux e macOS), simulando computadores completos dentro de um único computador físico.

### 1.2 Por que usar o VirtualBox ?

Ambientes isolados: Ideal para testar software ou sistemas operacionais sem impactar seu sistema principal.

Simulação de servidores: Criação de servidores Linux para estudos de DevOps, redes, infraestrutura.

Portabilidade: Máquinas virtuais podem ser exportadas e reutilizadas em outros computadores.

Gratuito e multiplataforma.

### 1.3 Casos de uso comuns

Teste de aplicações em diferentes SOs

Treinamento técnico e aulas práticas

Prototipagem de infraestruturas DevOps (com ferramentas como Ansible, Docker)

Criação de laboratórios simulados de rede ou segurança

### 1.4 Alternativas ao VirtualBox

FerramentaTipoLicençaObservaçõesVMware WorkstationHipervisorProprietáriaRecurso mais robusto, mas pagoHyper-V (Windows)HipervisorGratuito (Windows Pro)Integração com WindowsKVM + virt-managerHipervisor LinuxLivreAlta performance, uso profissional

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

