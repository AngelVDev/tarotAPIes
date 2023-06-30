# tarotAPIes

tarotAPIes provee información sobre los arcanos descritos en el sitio [Tarot de Tiziana](https://tarotdetiziana.com/). La versión original está en inglés, fue creada por [ekelen](https://github.com/ekelen)

### Pequeña documentación

| GET path                      | Resultado                                  | Params                                                                                                          |
| :---------------------------- | --------------------------------------- | :-------------------------------------------------------------------------------------------------------------- |
| `/api/v1/` or `/api/v1/cards` | Devuelve todas las cartas                       |                                                                                                                 |
| `/api/v1/cards/:name_short`   | Devuelve una carta específica con `name_short` | **menores:** `/swac`, `/wa02`, ..., `/cupa`, `/pequ`, `/waqu`, `/swki`, **mayores** `/ar01`, `/ar02`, ...`/ar[n]` |
| `/api/v1/cards/search`        | Busca entre todas las cartas (query, significado y significado al revés.)                       | `q={texto}`, `meaning={texto}`, `meaning_rev={texto}`                                                              |
| `/api/v1/cards/random`        | Devuelve cartas aleatorias                      | _opcional_ `n={número <= 78}`                                                                                  |

### Ejemplos:

##### Devuelve todas las cartas con "fiel" en el significado (al derecho o al revés):

/api/v1/cards/search?meaning=fiel

##### 3 cartas al azar:

/api/v1/cards/random?n=3

##### Obtener el Caballero de Bastos:

/api/v1/cards/wakn

---
## 💻 En referencia al desarrollo local

1. Se puede [agarrar el archivo JSON](./static/card_data.json) que sirve como fuente de información, con total confianza para tus propios proyectos. (Es una política del autor original, a la cuál adhiero).

2. Clona o forkea este repositorio e instala las dependencias. Requiere Node 10.0.0 o mayor, y npm 6.0.0 o mayor.

```sh
git clone https://github.com/AngelVDev/tarotAPIes.git
# o git@github.com:AngelVDev/tarotAPIes.git
# -OR- click fork en la página de éste proyecto de Github, y entonces:
git clone https://github.com/YOUR-USERNAME/tarotAPIes.git
```

Luego:

```sh
cd tarotAPIes
npm install
npm run dev
```
