<div id="top"></div>

<!-- PROJECT -->
<br />
<div align="center">
  <a href="https://laravel.com/img/logomark.min.svg">
    <img src="https://www.docker.com/sites/default/files/d8/2019-07/Moby-logo.png" alt="Logo" width="80" >
    <img src="https://laravel.com/img/logomark.min.svg" alt="Logo" width="70">
  </a>

  <h2 align="center">Laravel Docker Template</h2>

  <p align="center">
    Utilize este repositório para inicial seus projetos laravel com docker e docker-compose
    <br />
  </p>
</div>

<!-- GETTING STARTED -->
## Comece por aqui

Para criar seus projetos basta clonar este repositório e iniciar e começar a usar o laravel a partir da pasta src/ na raíz do projeto.

## Pré requisitos

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)


## Como usar


1. Clone este repositório
```sh
git clone https://github.com/emersonfidelon/laravel-docker-base.git
```
2. Entre na pasta baixada
```sh
cd laravel-docker-base
```
3. Dê permissão em todas as pastas e sub-pastas do Laravel
```sh
chmod -R 777 src/
```
4. Gere as imagens do docker
```sh
docker-compose --env-file .env.dev up -d --build
```
5. Instale as dependências do projeto
```sh
docker-compose --env-file .env.dev run composer install
```
6. Copie o arquivo .env.example para .env
```sh
cp src/.env.example src/.env
```
7. Verificando se todos os containers subiram corretamente
```sh
docker ps
```
8. Abra o navegador e digite http://localhost:8000

<img src="https://therichpost.com/wp-content/uploads/2020/09/Laravel-8-FullCalendar-Working-Example.png" width="100%" />

## Vale lembrar

Para alterar as configurações do docker-compose basta alterar o arquivo .env.dev

Caso a alteração seja da network, a mesma deve ser alterada no arquivo .env.dev e no docker-compose.yml