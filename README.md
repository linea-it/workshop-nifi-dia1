#  Workshop Apache NiFi: Desvendando o Poder do Fluxo de Dados (dia 1)

Este projeto tem o intuito de facilitar a instalação e execução do Apache NiFi versão 2.0.0-M4 utilizando Docker, conforme apresentado no [Workshop Apache NiFi: Desvendando o Poder do Fluxo de Dados (dia 1)](https://www.youtube.com/watch?v=cT20l3MDOZY&t=6808s).
Ele oferece uma maneira rápida e reproduzível de configurar um ambiente NiFi para aprendizado, testes e desenvolvimento para reproduzir o que foi visto no workshop.


## 🚀 Começando

Faça um clone desse projeto em sua máquina.


### 📋 Pré-requisitos

Necessário que o [Docker](https://www.docker.com/) esteja instalado na máquina.


### 🛠️ Configuração

Altere os parâmetros do JVM no arquivo docker-compose.yaml conforme capacidade de máquina:

```
NIFI_JVM_HEAP_INIT=4g
NIFI_JVM_HEAP_MAX=8g
```

>⚠️ **Atenção:** Os parâmetros NIFI_JVM_HEAP_INIT e NIFI_JVM_HEAP_MAX são usados para configurar a alocação de memória heap da JVM (Java Virtual Machine) sendo o primeiro o tamanho inicial da heap da JVM ao iniciar e o segundo até quanto ele pode crescer. 

Crie as credenciais username e password na variável de ambiente:

```
SINGLE_USER_CREDENTIALS_USERNAME=${SINGLE_USER_CREDENTIALS_USERNAME}
SINGLE_USER_CREDENTIALS_PASSWORD=${SINGLE_USER_CREDENTIALS_PASSWORD}
```

### 🔧 Instalação

Na pasta raiz execute o comando

```
docker compose up -d
```


### 🖥️ Execução

- Acesse o Apache NiFi através do endereço https://localhost:8443/login e faça o login.
- Realize a importação do template `workshop-nifi-dia1` localizado na pasta nifi\templates.
- Habilite no `Controller Services` os serviços `CSVReader` e `JsonRecordSetWriter`.
- Preencha no `Parameter Contexts` as informações conforme sua necessidade.


😁 Bons estudos!!!



