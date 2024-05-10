<p align="center"><a href="https://laravel.com" target="_blank"><img src="resources/images/logo.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

# Documentação do Sistema ALLMP

## Introdução

Este documento serve como guia para a instalação e configuração do Sistema ALLMP. O Sistema ALLMP é uma aplicação web desenvolvida utilizando o framework Laravel, e utiliza o banco de dados MySQL (MariaDB) para armazenamento de dados. O objetivo deste sistema é auxiliar na gestão e controle de processos de manufatura em uma empresa.

## Tecnologias Utilizadas

- Laravel
- MySQL (MariaDB)
- PHP

## Instalação do Laravel

Para instalar o Laravel, é necessário ter o Composer instalado. Utilize o seguinte comando para criar um novo projeto Laravel:

```bash
composer create-project --prefer-dist laravel/laravel app-ALLMP
```

## Inicialização do Laravel

Após a instalação do Laravel, é necessário configurar o ambiente. Navegue até o diretório do projeto e execute os seguintes comandos:

```bash
cp .env.example .env
php artisan key:generate
```

Edite o arquivo `.env` com as configurações do banco de dados.

Após configurar o banco de dados, execute as migrações para criar as tabelas necessárias:

```bash
php artisan migrate
```

Finalmente, inicie o servidor embutido do PHP:

```bash
php artisan serve
```
O servidor estará acessível através de `http://localhost:8000` ou pelo DNS que você configurou.

## Estrutura de Arquivos

A estrutura de arquivos do Laravel segue o padrão MVC (Model-View-Controller). Aqui está uma visão geral dos principais diretórios e arquivos:

```
nome-do-projeto/
├── app/
│   ├── Console/
│   ├── Exceptions/
│   ├── Http/
│   │   ├── Controllers/
│   │   ├── Middleware/
│   │   └── Kernel.php
│   ├── Models/
│   │   ├── System.php
│   │   └── User.php
│   └── Providers/
├── bootstrap/
├── config/
├── database/
│   ├── migrations/
│   ├── seeders/
│   └── ...
├── public/
├── resources/
│   ├── css/
│   ├── images/
│   ├── js/
│   ├── lang/
│   └── views/
├── routes/
├── storage/
├── tests/
├── vendor/
├── .env
├── .gitignore
├── artisan
└── composer.json
```

- `app/`: Contém os modelos, controladores, middleware e outros componentes da aplicação.
- `config/`: Configurações da aplicação.
- `database/`: Migrations e seeders para o banco de dados.
- `public/`: Arquivos acessíveis publicamente, como CSS, JavaScript e imagens.
- `resources/`: Contém as views, arquivos de linguagem e ativos front-end.
- `routes/`: Define as rotas da aplicação.
- `storage/`: Arquivos gerados pela aplicação, como logs e uploads de arquivos.
- `tests/`: Testes automatizados.
- `.env`: Arquivo de configuração do ambiente.
- `artisan`: Interface de linha de comando do Laravel.
- `composer.json`: Arquivo de configuração do Composer.

Esta é uma visão geral da estrutura de arquivos padrão do ALLMP.