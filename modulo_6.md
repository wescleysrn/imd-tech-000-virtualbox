[Voltar para o início](./README.md)

## Módulo 6 - Instalando O Serviço Nginx

**🎯 Objetivo**

<p align="justify">Instalar e iniciar o serviço nginx dentro da VM Oracle Linux, permitindo acesso a uma página web de teste a partir do navegador da máquina host.</p>

### 6.1 - O Que é o Nginx ?

<p align="justify">O **Nginx** (pronuncia-se "engine-x") é um servidor web de alto desempenho, amplamente utilizado para hospedar sites, APIs e aplicações web. Além de servir conteúdo estático, ele também atua como proxy reverso, balanceador de carga e cache de conteúdo.</p>

Entre suas principais vantagens:

-   Leve e rápido, mesmo com alto volume de conexões.
-   Fácil configuração.
-   Muito utilizado em ambientes corporativos e na nuvem.
-   Excelente integração com aplicações em PHP, Python, Node.js e
    outros.

💡 **Curiosidade**: o Nginx está presente em grandes serviços como Netflix, Dropbox e WordPress.com.

### 6.2 - Atualizando os Pacotes

<p align="justify">Antes de instalar qualquer software, é recomendável atualizar a lista de pacotes e aplicar correções de segurança:</p>

```
dnf update -y
```

<p align="justify">Esse comando garante que você está usando as versões mais recentes dos pacotes do sistema, evitando incompatibilidades.</p>

### 6.3 - Instalando o Nginx

<p align="justify">No Oracle Linux, o Nginx está disponível nos repositórios padrão:</p>

```
dnf install nginx -y
```

<p align="justify">Após a instalação, os arquivos principais do Nginx ficam localizados em:</p>

-   Arquivo de configuração principal: /etc/nginx/nginx.conf
-   Diretório de páginas padrão: /usr/share/nginx/html/
-   Arquivos de log: /var/log/nginx/

### 6.4 - Iniciando o Serviço Nginx

Para iniciar o servidor web:

```
systemctl start nginx
```

Se quiser que o Nginx seja iniciado automaticamente junto com o sistema:

```
systemctl enable nginx
```

### 6.5 - Verificando o Status

Podemos confirmar se o Nginx está rodando com:

```
systemctl status nginx
```

O resultado esperado deve indicar active (running).

Outra forma de verificar é testando a porta 80 internamente:

```
curl <http://localhost>
```

Se o Nginx estiver ativo, o comando retornará o conteúdo da página padrão.

### 6.6 - Ajustando o Firewall

Se o firewall estiver ativo, precisamos liberar a porta 80 (HTTP) para permitir conexões externas:

```
firewall-cmd --permanent --zone=public --add-service=http
firewall-cmd --reload
```

💡 Nota: Se for usar HTTPS futuramente, também será necessário liberar a porta 443.

### 6.7 - Acessando pelo Navegador (Máquina Host)

Com o Nginx rodando e o firewall configurado, já podemos acessar a página inicial no navegador do host.

1.  Abra seu navegador.
2.  Digite o IP fixo configurado no capítulo anterior:

[*http://192.168.56.10*](http://192.168.56.10)

1.  Você deverá ver a página padrão do Nginx com a mensagem **"Welcome to Nginx!"**.

Se a página aparecer, significa que:
-   O Nginx está instalado e ativo.
-   A rede Host-Only está configurada corretamente.
-   O servidor web está acessível pelo host.

[Voltar para o início](./README.md)

[Próximo 7 - CRIANDO URL AMIGÁVEL NO HOST](./modulo_7.md)
