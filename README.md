# Cidades de Portugal

### Índice
* [O que é?](#o-que-é)
* [Ficheiros](#ficheiros)
* [Formato JSON](#formato-json)
* [Base de Dados](#base-de-dados)
* [Como contribuir?](#como-contribuir)
* [Contribuidores](#contribuidores)
* [Histórico](#histórico)

## O que é?

Este repositório disponibiliza uma lista completa de cidades de Portugal em formato **JSON**, com os respetivos nomes corretamente acentuados e pontuados. É o recurso principal deste projeto, focado na comunidade portuguesa.

## Ficheiros

| Ficheiro | Descrição |
|---|---|
| [`pt_cities.json`](pt_cities.json) | Lista de cidades portuguesas em formato JSON ✅ |
| [`pt_cities_MySql.sql`](pt_cities_MySql.sql) | SQL de inserção das cidades em base de dados MySQL |

## Formato JSON

O ficheiro [`pt_cities.json`](pt_cities.json) contém um array de objetos com os seguintes campos:

```json
[
  {
    "id": 2267057,
    "nome": "Lisboa",
    "lat": 38.716671,
    "lon": -9.13333,
    "pais": "PT"
  }
]
```

* **id** — Identificador único da cidade
* **nome** — Nome da cidade (corretamente acentuado)
* **lat** — Latitude
* **lon** — Longitude
* **pais** — Código do país (ISO 3166-1 alpha-2)

## Base de Dados

O ficheiro [`pt_cities_MySql.sql`](pt_cities_MySql.sql) contém o SQL de inserção das cidades numa tabela MySQL com a seguinte estrutura:

```sql
INSERT INTO `cities` (`id`, `name`, `latitude`, `longitude`, `country_code`) VALUES
(2267057, 'Lisboa', 38.716671, -9.13333, 'PT'),
...
```

## Como contribuir?

A contribuição para este repositório é livre, tal como a sua utilização. Melhorias e deteção de erros são muito bem-vindas!

Para contribuir, basta fazer *fork* deste repositório, fazer as alterações desejadas e criar uma *pull request* que, se a contribuição for benéfica para este projeto, será imediatamente aceite.

Pode ser feita a contribuição de:
* Correção de nomes de cidades (acentuação, grafia)
* Adição de cidades em falta
* Exemplos de utilização em novas linguagens de programação

## Contribuidores

Um muito obrigado aos contribuidores deste projeto.
* Exemplo [JavaScript](pt_example.js): [@alpha-oliveira](https://github.com/alpha-oliveira)

## Histórico

Este repositório foi originalmente criado para disponibilizar a lista de cidades portuguesas para a API [OpenWeatherMap](http://openweathermap.org/). Os ficheiros originais são mantidos por razões históricas:

* [`pt_cities.txt`](pt_cities.txt) — Lista original no formato da API OpenWeatherMap
* [`world_cities.txt`](world_cities.txt) — Lista original de cidades do mundo (OpenWeatherMap)
* [`pt_example.cs`](pt_example.cs) — Exemplo de leitura do ficheiro `.txt` em C#
* [`pt_example.java`](pt_example.java) — Exemplo de leitura do ficheiro `.txt` em Java
* [`pt_example.js`](pt_example.js) — Exemplo de leitura do ficheiro `.txt` em JavaScript

> **Nota:** O link oficial da lista de cidades da OpenWeatherMap (`http://openweathermap.org/help/city_list.txt`) já não se encontra disponível.
