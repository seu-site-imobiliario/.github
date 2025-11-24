# Seu Site Imobiliário
Este projeto propõe o desenvolvimento de uma solução digital que possibilita a corretores de imóveis obterem um site personalizado no estilo de uma imobiliária, sem a necessidade de conhecimentos técnicos em programação ou design. A iniciativa surge da constatação da dificuldade que muitos profissionais autônomos enfrentam para manter uma presença digital profissional, organizada e constantemente atualizada.

### Tecnologias

- Containerização: Docker e Docker Compose
- Back-End: Laravel, Redis
- Front-End: Next Js
- Banco de Dados: MySQL
---
### 1. Como Executar (Ambiente Local com Docker)

#### A. Clone os repositórios (painel, site, api)
Primeiro, clone os repositórios e acesse as branchs corretas para desenvolvimento (develop).

#### B. Pré-requisitos
Antes de começar, certifique-se de que você tem o Docker e o Docker Compose instalados:
- Instalar Docker + Docker Compose

#### C. Variáveis de Ambiente
Os repositórios precisam de algumas variáveis de ambiente. Os arquivos .env.example estão configurados com valores de exemplo.

- Api
```bash
docker compose up -d --build
docker compose exec api bash
php artisan key:generate
php artisan migrate --seed

```

- Painel
```bash 
docker-compose up --build
```

- Site
```bash 
docker-compose up --build
```

#### D. Acessando a Aplicação Local
Após a conclusão dos comandos, os serviços estarão disponíveis nos seguintes endereços:

- Front-End (Site): http://localhost:3000
- Front-End (Painel): http://localhost:3002
- Back-End (API): http://localhost:8000
- Banco de Dados (Mysql): Acessível em localhost:8080
