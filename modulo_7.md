[Voltar para o início](./README.md)

## Módulo 7 - Criando Url Amigável no Host

**🎯 Objetivo**

<p align="justify">Ensinar como configurar uma URL personalizada (como meuservidor.local) na máquina host, apontando para o IP da VM, facilitando o acesso ao serviço web no navegador.</p>

### 7.1 - O Problema de Usar IP's

<p align="justify">Até aqui, para acessar nosso servidor web, utilizamos um endereço IP, por exemplo:</p>

[*http://192.168.56.10*](http://192.168.56.10)

<p align="justify">Embora funcional, esse método apresenta alguns inconvenientes:</p>

-   É difícil lembrar endereços numéricos.
-   Caso o IP seja alterado (em configurações dinâmicas), o link deixará de funcionar.
-   Em ambientes com vários serviços, ter que lembrar cada IP se torna confuso.

<p align="justify">Em um ambiente de produção, usuários não acessam sistemas via IP eles usam <strong>nomes de domínio</strong> (URLs), como www.exemplo.com.</p>

### 7.2 - Solução: Usar o Arquivo Hosts

<p align="justify">Para simular um nome de domínio no seu computador <strong>sem depender de um DNS externo</strong>, podemos usar o <strong>arquivo hosts</strong> do sistema operacional.</p>

O **arquivo hosts** funciona como um mini-servidor DNS local:

-   Ele permite mapear um nome de domínio para um endereço IP específico.
-   Esse mapeamento vale apenas para o computador onde o arquivo foi modificado.

No Windows, o arquivo hosts fica em:

```
C:\\Windows\\System32\\drivers\\etc\\hosts
```

No Linux e macOS, o caminho é:

```
/etc/hosts
```

### 7.3 - Criando o Mapeamento

<p align="justify">Vamos supor que o IP fixo configurado no capítulo anterior foi 192.168.56.10 e queremos criar a URL amigável meuservidor.local.</p>

1.  Abrir o arquivo hosts como administrador:
    -   No Windows: abrir o Bloco de Notas como Administrador e carregar o arquivo hosts.
    -   No Linux/macOS: abrir com 
    ```
    sudo nano /etc/hosts.
    ```
2.  Adicionar uma nova linha no final:

```
192.168.56.10 meuservidor.local
```

1.  Salvar o arquivo.

<p align="justify">Agora, quando o navegador tentar acessar meuservidor.local, ele será direcionado automaticamente para o IP 192.168.56.10.</p>

### 7.4 - Acessando o Serviço pelo Navegador

Após salvar a modificação no arquivo hosts:

-   Abra o navegador e digite:

[*http://meuservidor.local*](http://meuservidor.local)

-   A página padrão do Nginx deverá aparecer, assim como aparecia com o IP.

💡 **Nota**: Esse processo só funciona no computador onde você alterou o arquivo hosts. Se quiser que outros dispositivos da rede também reconheçam o nome, será necessário alterar o hosts deles ou configurar um DNS local.

### 7.5 - Dicas para Nomes mais Profissionais

Ao escolher um nome para o seu servidor local, considere:

-   Usar um **sufixo não público** para evitar conflitos com sites reais. Exemplos: .local, .test, .lab.
-   Evitar caracteres especiais e acentos.
-   Criar nomes curtos e objetivos. Exemplos:
    -   webserver.local
    -   nginx.lab
    -   projeto1.test

Em ambientes profissionais, o uso de **DNS interno** é a prática recomendada, mas para estudos e testes, o arquivo hosts é suficiente.

[Voltar para o início](./README.md)

[Próximo 8 - ENCERRAMENTO E PRÓXIMOS PASSOS](./modulo_8.md)
