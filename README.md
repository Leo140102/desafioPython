# Marvel API Integration with SQLite and Pandas

Este código integra a API pública da Marvel para obter dados sobre personagens, quadrinhos e eventos. Os dados são armazenados em um banco de dados SQLite e manipulados utilizando a biblioteca Pandas para exibição em DataFrames.

## Dependências

- `hashlib`: Gera o hash MD5 necessário para autenticação na API.
- `requests`: Realiza requisições HTTP à API da Marvel.
- `pandas`: Manipula os dados e exibe como DataFrames.
- `sqlite3`: Interage com o banco de dados SQLite.
- `google.colab`: Obtém as chaves de API do ambiente do Google Colab.

## Funcionalidades

1. **Obtenção de chaves de API**: A função `get_api_keys()` recupera as chaves pública e privada do Google Colab.
2. **Geração de Hash MD5**: A função `generate_md5_hash()` cria um hash MD5 para autenticação.
3. **Requisição à API**: A função `fetch_data_from_api()` obtém dados sobre personagens, quadrinhos e eventos da API da Marvel.
4. **Criação de Banco de Dados**: A função `create_tables()` cria as tabelas no banco de dados SQLite.
5. **Inserção de Dados**: A função `insert_data_into_db()` insere os dados na tabela correspondente.
6. **Exibição dos Dados**: A função `main()` realiza todo o processo e exibe os dados utilizando Pandas.

## Exemplo de Execução

1. Obtenção das chaves de API.
2. Geração do hash MD5 para autenticação.
3. Requisição à API da Marvel para buscar dados de personagens, quadrinhos e eventos.
4. Criação do banco de dados e inserção dos dados.
5. Exibição dos dados utilizando Pandas.

## Exemplo de Saída

- **Tabela de Personagens**:
    | id  | name         | description | comics_returned | stories_returned | events_returned |
    | --- | ------------ | ----------- | --------------- | ---------------- | --------------- |
    | 1   | Spider-Man   | Hero        | 100             | 50               | 10              |

- **Tabela de Quadrinhos**:
    | id  | comic_title        | characters_returned | events_returned |
    | --- | ------------------ | ------------------- | --------------- |
    | 1   | Amazing Spider-Man | 10                  | 5               |

- **Tabela de Eventos**:
    | id  | title          | description     | start       | end         | characters_returned | comics_returned |
    | --- | -------------- | --------------- | ----------- | ----------- | ------------------- | --------------- |
    | 1   | Spider-Verse   | Multiverse event | 2023-01-01  | 2023-01-10  | 50                  | 20              |

## Conclusão

Este código realiza a integração com a API da Marvel, armazena os dados no banco de dados SQLite e os manipula usando Pandas para facilitar a análise e visualização.
