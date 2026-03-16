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
| [`pt_cities.json`](pt_cities.json) | Lista de cidades portuguesas em formato JSON |
| [`pt_cities_MySql.sql`](pt_cities_MySql.sql) | SQL de inserção das cidades em base de dados MySQL |

## Formato JSON

O ficheiro [`pt_cities.json`](pt_cities.json) contém um array de objetos com os seguintes campos:

```json
[
  {
    "id": 2267057,
    "name": "Lisboa",
    "lat": 38.716671,
    "lon": -9.13333,
    "country_code": "PT",
    "district": "Lisboa",
    "province": "Estremadura",
    "region": "Lisboa e Vale do Tejo"
  }
]
```

* **id** — Identificador único da cidade
* **name** — Nome da cidade (corretamente acentuado)
* **lat** — Latitude
* **lon** — Longitude
* **country_code** — Código do país (ISO 3166-1 alpha-2)
* **district** — Distrito (ex: Lisboa, Porto, Faro)
* **province** — Província histórica (ex: Estremadura, Minho, Algarve)
* **region** — Região (ex: Norte, Centro, Lisboa e Vale do Tejo, Alentejo, Algarve, Região Autónoma dos Açores, Região Autónoma da Madeira)

## Base de Dados

O ficheiro [`pt_cities_MySql.sql`](pt_cities_MySql.sql) contém o SQL de criação e inserção das cidades numa tabela MySQL com a seguinte estrutura:

```sql
CREATE TABLE IF NOT EXISTS `cities` (
  `id` INT NOT NULL,
  `name` VARCHAR(100) NOT NULL,
  `latitude` DECIMAL(10,6) NOT NULL,
  `longitude` DECIMAL(10,6) NOT NULL,
  `country_code` VARCHAR(2) NOT NULL,
  `district` VARCHAR(100) NOT NULL,
  `province` VARCHAR(100) NOT NULL,
  `region` VARCHAR(100) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

INSERT INTO `cities` (`id`, `name`, `latitude`, `longitude`, `country_code`, `district`, `province`, `region`) VALUES
(2267057, 'Lisboa', 38.716671, -9.13333, 'PT', 'Lisboa', 'Estremadura', 'Lisboa e Vale do Tejo'),
...
```

## Como contribuir?

A contribuição para este repositório é livre, tal como a sua utilização. Melhorias e deteção de erros são muito bem-vindas!

Para contribuir, basta fazer *fork* deste repositório, fazer as alterações desejadas e criar uma *pull request* que, se a contribuição for benéfica para este projeto, será imediatamente aceite.

Pode ser feita a contribuição de:
* Correção de nomes de cidades (acentuação, grafia)
* Adição de cidades em falta
* Correção da região, província ou distrito de cada cidade

## Contribuidores

Um muito obrigado aos contribuidores deste projeto.

## Histórico

Este repositório foi originalmente criado para disponibilizar a lista de cidades portuguesas para a API [OpenWeatherMap](http://openweathermap.org/). Os ficheiros originais são mantidos por razões históricas:

* [`pt_cities.txt`](pt_cities.txt) — Lista original no formato da API OpenWeatherMap
* [`world_cities.txt`](world_cities.txt) — Lista original de cidades do mundo (OpenWeatherMap)

> **Nota:** O link oficial da lista de cidades da OpenWeatherMap (`http://openweathermap.org/help/city_list.txt`) já não se encontra disponível.
