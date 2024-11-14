# RabbitMQ com Docker - Projeto Base

Este projeto fornece um ambiente básico para executar o RabbitMQ em contêiner com Docker e Docker Compose. A configuração permite iniciar o RabbitMQ rapidamente com um painel de gerenciamento acessível via navegador.

## Pré-requisitos

    Docker e Docker Compose instalados em sua máquina.

## Configuração

1. Configuração do arquivo .env:

   - Renomeie o arquivo .env.example para .env.
   - Ajuste as variáveis conforme necessário. Em especial:
     RABBITMQ_USER: define o usuário do RabbitMQ.
     RABBITMQ_PASS: define a senha do RabbitMQ.
     RABBITMQ_MANAGEMENT_PORT: define a porta de gerenciamento do RabbitMQ (ex: 15672).

2. Construção e execução do contêiner:

   - Execute o comando abaixo para iniciar o RabbitMQ em segundo plano:

   ```
   docker-compose up -d --build

   ```

## Acesso ao Painel de Gerenciamento

- Após a execução, acesse o painel de gerenciamento do RabbitMQ no navegador:

```
http://127.0.0.1:{RABBITMQ_MANAGEMENT_PORT}
```

Substitua {RABBITMQ_MANAGEMENT_PORT} pela porta definida no arquivo .env.

- Credenciais de Acesso: Use o nome de usuário e a senha configurados no arquivo .env para login no painel de gerenciamento.

## Comandos Úteis

- Iniciar container:

```
docker-compose start
```

- Parar container:

```
docker-compose stop
```

- Ver logs do RabbitMQ:

```
docker-compose logs -f
```
