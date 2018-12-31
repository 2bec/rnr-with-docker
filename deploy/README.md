# Guia para início rápido com Ruby on Rails
Para ter uma aplicação Rails rodando dentro do docker siga os passos abaixo:

1) Copie os arquivos `Gemfile` e `Gemfile.lock` para a raíz;
2) Execute o comando `docker-compose run web rails new . --force --database=postgresql` para gerar um skeleton Rails para sua aplicação;
3) Os arquivos gerados pelo `Docker` no linux são de propriedade `root`, então execute `sudo chown -R $USER:$USER .` para corrigir (toda vez que for necessário buildar);
4) Build a docker novamente, pois o comando run do passo 2 alterou a `Gemfile`;
5) Agora só falta configurar o banco de dados, insira as seguintes linhas ao arquivo `config/database.yml`:
```
host: db
username: postgres
password:
```
6) E agora start seu app `docker-compose up`

# Todo
- [] Usar reactjs no frontend
- [] Usar nginx
- [] Variáveis de ambiente
- [] Deploy na AWS

# Referências
- [Docker docs](https://docs.docker.com/compose/rails/)