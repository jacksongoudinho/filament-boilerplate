
# Setup Docker Laravel 11 com PHP 8.3

### Passo a passo

Clone Repositório
```sh
git clone git@github.com:jacksongoudinho/docker-laravel.git nome-do-projeto
```

Acessar a pasta do projeto criado
```sh
cd nome-do-projeto
```

Crie o Arquivo .env
```sh
cp .env.example .env
```

Alterar a .env do projeto
```sh
DB_CONNECTION=mysql # Banco de dados
DB_HOST=mysql # Nome do container do banco
DB_PORT=3306 # Porta de conexão
DB_DATABASE=laravel # Nome do banco
DB_USERNAME=username # User para conectar ao banco
DB_PASSWORD=userpass # Senha para conectar ao banco
```

Suba os containers do projeto
```sh
docker-compose up -d
```

Acesse o container app
```sh
docker-compose exec app bash
```

Instalar as dependências do projeto
```sh
composer install
```

Gere a key do projeto Laravel
```sh
php artisan key:generate
```

Rodar as migrations
```sh
php artisan migrate
```

Acesse o projeto
[http://localhost:80](http://localhost:80)
