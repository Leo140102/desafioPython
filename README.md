# Integração com a API da Marvel

Este código integra com a API da Marvel para obter dados sobre personagens, quadrinhos e eventos, e armazena as informações em um banco de dados SQLite. Os dados extraídos são apresentados em formato de tabelas utilizando a biblioteca `pandas`.

## Funcionalidades

1. **Obtenção de Chaves de API**  
   Obtém as chaves públicas e privadas do usuário no ambiente do Google Colab.

2. **Geração do Hash MD5**  
   Cria um hash MD5 necessário para autenticação na API da Marvel.

3. **Requisição à API da Marvel**  
   Realiza requisições GET aos endpoints de personagens, quadrinhos e eventos da API da Marvel.

4. **Criação de Tabelas no Banco de Dados SQLite**  
   Cria as tabelas necessárias (`characters`, `comics`, `events`) no banco de dados SQLite, se não existirem.

5. **Inserção de Dados no Banco de Dados**  
   Insere os dados extraídos da API nas tabelas correspondentes no banco de dados.

6. **Exibição dos Dados com `pandas`**  
   Lê os dados do banco de dados e exibe as informações extraídas em formato de tabelas.

## Fluxo do Código

1. **Obtenção das Chaves de API**: As chaves são extraídas da configuração do Google Colab.
2. **Geração do Hash MD5**: Geração do hash MD5 para autenticação na API.
3. **Requisição à API**: Requisições GET são feitas para obter dados de personagens, quadrinhos e eventos.
4. **Criação de Tabelas**: Conexão ao banco SQLite e criação das tabelas necessárias.
5. **Inserção de Dados**: Os dados obtidos são inseridos nas tabelas correspondentes.
6. **Exibição dos Dados**: Os dados são lidos usando `pandas` e exibidos em formato de tabela.

## Exemplo de Saída

Após a execução, as tabelas com os dados extraídos serão exibidas. Exemplo:

### Tabela de Personagens:

| id  | name         | description      |
| --- | ------------ | ---------------- |
| 1   | Spider-Man   | A hero           |
| 2   | Iron Man     | A billionaire    |

### Tabela de Quadrinhos:

| id  | comic_title              |
| --- | ------------------------ |
| 1   | Amazing Spider-Man       |
| 2   | Iron Man #1              |

### Tabela de Eventos:

| id  | title        | description | start       | end         |
| --- | ------------ | ----------- | ----------- | ----------- |
| 1   | Secret Wars | Big battle  | 2015-05-01  | 2015-10-01  |

## Dependências

- `hashlib`: Para gerar o hash MD5.
- `requests`: Para realizar as requisições HTTP.
- `pandas`: Para trabalhar com tabelas e exibir os dados.
- `sqlite3`: Para interagir com o banco de dados SQLite.
- `google.colab.userdata`: Para obter as chaves de API no Google Colab.
