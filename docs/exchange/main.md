# Exchange API

A Exchange API é uma API REST desenvolvida em **Python** utilizando o framework **FastAPI**. A API permite ao usuário realizar a conversão entre diferentes moedas. 

Afim de realizar o câmbio entre moedas, a API utiliza uma API de terceiros. Você pode conferir a API utilizada aqui: [AwesomeAPI](https://github.com/awesomeapibrasil/economy-api){target="_blank"};.

A API possuí o seguinte endpoint:

!!! info "GET /exchange/{from}/{to}"

    Obtenha a cotação atual de uma moeda para outra. Ex: `GET /coin/USD/EUR`.

    === "Response"

        ``` { .json .copy .select linenums='1' }
        {
            "sell": 0.82,
            "buy": 0.80,
            "date": "2021-09-01 14:23:42",
            "id-account": "0195ae95-5be7-7dd3-b35d-7a7d87c404fb"
        }
        ```
        ```bash
        Response code: 200 (ok)
        ```

A API está disponível no seguinte repositório: [ExchangeAPI](https://github.com/giuvallente/exchange){target="_blank"};.

Segue abaixo o código-fonte da ExchangeAPI:

``` tree
app/
    main.py/
    requirements.txt/
Dockerfile
```

=== "main.py"
    ``` { .yaml .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/exchange/blob/main/app/main.py"
    ```

=== "requirements.txt"
    ``` { .sh .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/exchange/blob/main/app/requirements.txt"
    ```

=== "Dockerfile"
    ``` { .sh .copy .select linenums="1" }
    --8<-- "https://raw.githubusercontent.com/giuvallente/exchange/blob/main/Dockerfile"
    ```

