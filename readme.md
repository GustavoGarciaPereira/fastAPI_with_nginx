# Template FastAPI com Nginx

Este projeto é uma aplicação web simples utilizando FastAPI, conteinerizada com Docker, e usando Nginx como servidor web proxy reverso. A aplicação é ideal para ambientes de desenvolvimento e testes, podendo também ser adaptada para produção.

## Características

-   **FastAPI**: Framework moderno e rápido para construir APIs com Python 3.7+.
-   **Docker**: Contêinerização para garantir facilidade de implantação e consistência entre ambientes.
-   **Nginx**: Configurado como proxy reverso, melhorando a segurança e o desempenho.
-   **nip.io**: Utilizado para testes locais que simulam domínios reais.

## Pré-requisitos

-   Python 3.7+
-   Docker e Docker Compose
-   (Opcional) Ferramenta `ngrok` ou `nip.io` para testes com domínios.

## Configuração e Instalação

1.  **Clone o Repositório:**
    
    bashCopy code
    
    `git clone https://github.com/GustavoGarciaPereira/fastAPI_with_nginx.git
    cd fastAPI_with_nginx` 
    
2.  **Construir e Rodar com Docker:**
    `docker-compose up --build` 
    

## Usando `nip.io` para Testes Locais

-   Para testar subdomínios e funcionalidades de domínio específicas localmente, use `nip.io`.
-   Exemplo: `http://app1.127.0.0.1.nip.io:8001/` apontará para `http://app1.127.0.0.1.nip.io:8002/` (seu localhost).

## Estrutura do Projeto
```bash
 gustavo  ~  projeto_ngnix_fastAPI  nginx_test2  tree -L 2                                                                                                                                             main  
.
├── app1
│   ├── dockerfile
│   ├── main.py
│   └── requirements.txt
├── app2
│   ├── dockerfile
│   ├── main.py
│   └── requirements.txt
├── docker-compose.yml
├── nginx.conf
└── readme.md
2 directories, 9 files
```