# Projeto LocalStack com docker-compose

Este projeto utiliza o LocalStack para simular serviços AWS localmente, como o S3. Abaixo estão as instruções para clonar, configurar e executar o projeto localmente.

## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes itens instalados:

- [Docker Desktop](https://www.docker.com/get-started) (necessário para executar o LocalStack)
- [Git](https://git-scm.com/)

## Passos para clonar e usar o projeto

### 1. Clonar o Repositório

Execute o seguinte comando no terminal para clonar o repositório:

```bash
git clone https://github.com/inoccard/my-docker-hub.git
 ```
### 2. Navegar para o Diretório do Projeto
Após clonar o repositório, navegue para o diretório desejado:

Exemplo:
```bash
cd localstack
```

### 3. Configurar e Iniciar o LocalStack
Este projeto utiliza o LocalStack para simular serviços AWS localmente. Para configurar e iniciar o LocalStack, siga as instruções abaixo.

Passos:
1. Certifique-se de que o Docker Desktop está rodando em sua máquina.
2. Execute o comando para iniciar o LocalStack utilizando o docker-compose:

```bash
docker-compose up
```
Isso iniciará o LocalStack no docker e criará as pastas necessárias para sua execução (como cache, lib, logs, tmp).

Os mesmos passo funcionam para os demais diretórios

Agora, se preferir executar mais de um arquivos em diretórios diferentes:
1. Volte para o diretório principal (docker-hub-comercial)
```bash
docker-compose -f localstack/docker-compose.yml -f elasticsearch/docker-compose.yml up
```
### 4. Configurar o SQL Server
Coloque este código no seu arquivo appSetting

```bash
Server=localhost,1433;Database=master;User Id=SA;Password=123456```