# Boas-vindas ao repositório do projeto Shopping Cart!

<details>
  <summary><strong>👨‍💻 O que deverá ser desenvolvido</strong></summary><br />

Esse é um projeto desenvolvido para simular um **carrinho de compras** totalmente dinâmico! 🛒

Para isso, vai consumir dados diretamente de uma **API!** 🤩

O que é API? Da sigla em inglês _Application Programming Interface_, uma API é um ponto de contato na internet com determinado serviço e nesse projeto foi utilizada a API do Mercado Livre para buscar produtos à venda. 🏷

Nesse projeto foi utilizada a prática do desenvolvimento orientado a testes, o TDD (Test Driven Development)! Que ajuda a garantir um código de qualidade, percebendo os casos de uso da aplicação e garantindo que ela esteja funcionando corretamente!

Ao finalizar o projeto, ele deve ter o comportamento parecido com o gif abaixo:

![Project Gif](./prototipo.gif)

</details>

# Orientações

<details>
  <summary><strong>‼️ Para executar o projeto siga as seguintes orientações</strong></summary><br />

1. Clone o repositório executando o seguinte comando no terminal:
  * `git clone git@github.com:matheusqueiroz92/shopping-cart.git`.
  * Entre na pasta do repositório que você acabou de clonar executando o próximo comando:
    * `cd shopping-cart`

2. Instale as dependências e inicialize o projeto executando o comando a seguir
  * Instale as dependências:
    * `npm install`

3. Após seguir os passos anteriores, abra o projeto com o seu editor de código
  * Este projeto foi desenvolvido utilizando o Visual Studio Code. Caso utilize este editor, basta entrar na pasta em que o projeto foi salvo e digitar o seguinte comando em seu terminal para abri-lo:
    * `code .`
  * Para executar este projeto, foi utilizada a extensão LiveShare do Visual Studio Code.
</details>

<details>
  <summary><strong>⌨️ Durante o desenvolvimento</strong></summary><br />

  * Durante o desenvolvimento deste projeto foram feitos `commits` das alterações realizadas no código;

  * Os comandos utilizados com mais frequência foram:

    1. `git status` _(para verificar o que está em vermelho - fora do stage - e o que está em verde - no stage)_;

    2. `git add` _(para adicionar arquivos ao stage do Git)_;

    3. `git commit` _(para criar um commit com os arquivos que estão no stage do Git)_;

    4. `git push -u origin nome-da-branch` _(para enviar o commit para o repositório remoto na primeira vez que fizer o `push` de uma nova branch)_;

    5. `git push` _(para enviar o commit para o repositório remoto após o passo anterior)_.

</details>

<details>
  <summary><strong>🎛 Linter</strong></summary><br />

### ESLint e Stylelint

Para garantir a qualidade do código, foi utilizado neste projeto os linters `ESLint` e `Stylelint`, para manter o código alinhado com as boas práticas de desenvolvimento, sendo mais legível e de fácil manutenção!

Para poder rodar o `ESLint` e o `Stylelint` certifique-se de ter executado o comando `npm install` dentro do projeto.

Para rodá-los localmente no projeto, execute os comandos abaixo:

```bash
  npm run lint
  npm run lint:styles
```

Se a análise do `ESLint` e do `Stylelint` encontrarem problemas no código, tais problemas serão mostrados no terminal. Se não houver problema no código, nada será impresso no terminal.

É possível também instalar o plugin do `ESLint` no Visual Studio Code. Para isso, basta fazer o download do plugin `ESLint` e instalá-lo.

⚠️ **PULL REQUESTS COM ISSUES NO LINTER NÃO SERÃO AVALIADAS. ATENTE-SE PARA RESOLVÊ-LAS ANTES DE FINALIZAR O DESENVOLVIMENTO!** ⚠️

</details>

<details>
  <summary><strong>🛠 Testes</strong></summary><br />

Nesse projeto foi implementado o TDD (Test Driven Development) também conhecido como _desenvolvimento orientado a testes_, que é uma prática muito utilizada no mercado de trabalho para garantir que o código será implementado da maneira correta. Ou seja, primeiro você vai escrever o teste para uma função e depois vai implementar a lógica para que a função execute.

Foi implementado testes para quatro funções: `fetchProducts`, `fetchItem`, `saveCartItems` e `getSavedCartItems`. 

### Cobertura de testes

Para avaliar se os testes estão cobrindo toda a função, será utilizado a **cobertura de testes**, que avalia a eficácia dos testes implementados de acordo com os requisitos, determinando se cobrem o que foi pedido ou não.

⚠️ **Será testado apenas as quatros funções citadas e não toda a aplicação!**

Conforme foi realizado os testes do projeto, a porcentagem da cobertura total foi aumentando. Para a cobertura total será avaliado 25%, 50%, 75%, e, por fim, 100% dos testes. Para cada função solicitada a cobertura de testes irá avaliar 100% das linhas da mesma.

Para rodar os testes, deve-se executar comando abaixo:

```bash
npm test
```

Para executar e acompanhar a implementação da sua cobertura de testes, deve-se rodar o comando abaixo:

```bash
npm run test:coverage
```

Ao realizar o comando de cobertura de testes terá um resultado similar a este:

![Cobertura de Testes](cobertura.png)

Os destaques em amarelo fazem referência à cobertura total e os em verde do requisito desejado.

Para verificar se todos os itens da cobertura dos testes estão passando corretamente basta executar o comando `npm test`.


### Pontos importantes para a implementação dos testes

A API foi simulada para a implementação dos testes. Isso significa que será possível simular o consumo de todos os dados da API dentro do ambiente de testes, de forma segura e independente de fatores externos que possam ocorrer.

- Os retornos esperados das funções estão importados nos arquivos de teste e estão especificados nos requisitos;

- O `window.fetch` está definido em todos os testes, ou seja, será possível usar a função `fetch` dentro do ambiente de testes sem precisar importar ou instalar bibliotecas;

- O `localStorage.getItem` e o `localStorage.setItem` podem ser utilizados normalmente no ambiente de teste, pois a simulação dele está pronta para ser chamada quando necessário;

- Para o ambiente de testes, o `fetch` está limitado a atender somente a configuração da API referente ao projeto;

Para avaliar o projeto como um todo, será utilizado o _Cypress_.

### Cypress

Cypress é uma ferramenta de teste de front-end desenvolvida para a web.

Antes de utilizá-lo, certifique-se de ter executado o comando `npm install` dentro do projeto.

O cypress pode ser rodado localmente para verificar se os requisitos estão passando, para isso basta executar um dos seguintes comandos:

Para executar os testes e vê-los rodando em uma janela de navegador:

```bash
npm run cypress:open
```

ou

```bash
npx cypress open
```

Após executar um dos comandos acima, será aberta uma janela de navegador e então basta clicar no nome do arquivo de teste que quiser executar (project.spec.js), ou para executar todos os testes clique em _Run all specs_.

</details>

<details>
<summary><strong>🏗 Estrutura do projeto</strong></summary><br />

O projeto contém os arquivos `index.html`, `style.css` e `script.js`, que conterão seu código HTML, CSS e JavaScript, respectivamente. 

O arquivo `scripts.js` contém uma estrutura de código inicial, que cria alguns elementos HTML. Cada função do código é especificada nos requistos. 

É no `script.js` que foi implementada a lógica para desenvolver o projeto.

<details>
  <summary>
    Clique aqui para saber um pouco mais sobre o que cada função faz
  </summary> <br />

  - `createProductImageElement`: Cria um elemento de imagem;
  - `createCustomElement`: Estrutura para criar um elemento;
  - `createProductItemElement`: Cria a lista de produtos;
  - `getSkuFromProductItem`: Pega o `id` de um produto;
  - `cartItemClickListener`: Escuta a ação de clicar em um item no carrinho;
  - `createCartItemElement`: Cria os elementos do carrinho.

</details>

A pasta `helpers` contém os arquivos `fetchItem.js`, `fetchProducts.js`, `getSavedCartItems.js` e `saveCartItems.js` e cada um possui uma estrutura para implementar cada uma das funções que serão utilizadas seu código JavaScript.

A pasta `tests`, contém os arquivos `fetchItem.test.js`, `fetchProducts.test.js`, `getSavedCartItems.test.js` e `saveCartItems.test.js`, onde foram implementados os testes para cada uma das funções de mesmo nome.

</details>

<details>
<summary><strong>⚙️ API do Mercado Livre</strong></summary><br />

O [manual da API do Mercado Livre](https://developers.mercadolivre.com.br/pt_br/itens-e-buscas) contém todas as informações acerca da API (retorno, estrutura). Nesse projeto foram utilizados apenas alguns dos seus _endpoints_, sendo eles:

- `https://api.mercadolibre.com/sites/MLB/search?q=$QUERY`: traz uma lista de produtos, onde `$QUERY` é o termo a ser buscado. Por exemplo, se o termo for `computador`, o retorno será parecido com esse:

  <details>
    <summary>Retorno da requisição de listagem de produtos</summary>

    Esse retorno possui várias informações acerca da lista de produtos. Dento do array `results` é onde você vai encontrar a lista de produtos.

  ```json
  {
      "site_id": "MLB",
      "query": "computador",
      "paging": {
          "total": 406861,
          "offset": 0,
          "limit": 50,
          "primary_results": 1001
      },
      "results": [
          {
              "id": "MLB1341925291",
              "site_id": "MLB",
              "title": "Processador Intel Core I5-9400f 6 Núcleos 128 Gb",
              "seller": {
                  "id": 385471334,
                  "permalink": null,
                  "power_seller_status": null,
                  "car_dealer": false,
                  "real_estate_agency": false,
                  "tags": []
              },
              "price": 899,
              "currency_id": "BRL",
              "available_quantity": 1,
              "sold_quantity": 0,
              "buying_mode": "buy_it_now",
              "listing_type_id": "gold_pro",
              "stop_time": "2039-10-10T04:00:00.000Z",
              "condition": "new",
              "permalink": "https://www.mercadolivre.com.br/processador-intel-core-i5-9400f-6-nucleos-128-gb/p/MLB13953199",
              "thumbnail": "http://mlb-s2-p.mlstatic.com/813265-MLA32241773956_092019-I.jpg",
              "accepts_mercadopago": true,
              "installments": {
                  "quantity": 12,
                  "amount": 74.92,
                  "rate": 0,
                  "currency_id": "BRL"
              },
              "address": {
                  "state_id": "BR-SP",
                  "state_name": "São Paulo",
                  "city_id": "BR-SP-27",
                  "city_name": "São José dos Campos"
              },
              "shipping": {
                  "free_shipping": true,
                  "mode": "me2",
                  "tags": [
                      "fulfillment",
                      "mandatory_free_shipping"
                  ],
                  "logistic_type": "fulfillment",
                  "store_pick_up": false
              },
              "seller_address": {
                  "id": "",
                  "comment": "",
                  "address_line": "",
                  "zip_code": "",
                  "country": {
                      "id": "BR",
                      "name": "Brasil"
                  },
                  "state": {
                      "id": "BR-SP",
                      "name": "São Paulo"
                  },
                  "city": {
                      "id": "BR-SP-27",
                      "name": "São José dos Campos"
                  },
                  "latitude": "",
                  "longitude": ""
              },
              "attributes": [
                  {
                      "source": 1,
                      "id": "ALPHANUMERIC_MODEL",
                      "value_id": "6382478",
                      "value_struct": null,
                      "values": [
                          {
                              "name": "BX80684I59400F",
                              "struct": null,
                              "source": 1,
                              "id": "6382478"
                          }
                      ],
                      "attribute_group_id": "OTHERS",
                      "name": "Modelo alfanumérico",
                      "value_name": "BX80684I59400F",
                      "attribute_group_name": "Outros"
                  },
                  {
                      "id": "BRAND",
                      "value_struct": null,
                      "attribute_group_name": "Outros",
                      "attribute_group_id": "OTHERS",
                      "source": 1,
                      "name": "Marca",
                      "value_id": "15617",
                      "value_name": "Intel",
                      "values": [
                          {
                              "id": "15617",
                              "name": "Intel",
                              "struct": null,
                              "source": 1
                          }
                      ]
                  },
                  {
                      "name": "Condição do item",
                      "value_id": "2230284",
                      "attribute_group_id": "OTHERS",
                      "attribute_group_name": "Outros",
                      "source": 1,
                      "id": "ITEM_CONDITION",
                      "value_name": "Novo",
                      "value_struct": null,
                      "values": [
                          {
                              "id": "2230284",
                              "name": "Novo",
                              "struct": null,
                              "source": 1
                          }
                      ]
                  },
                  {
                      "id": "LINE",
                      "value_name": "Core i5",
                      "attribute_group_id": "OTHERS",
                      "attribute_group_name": "Outros",
                      "name": "Linha",
                      "value_id": "7769178",
                      "value_struct": null,
                      "values": [
                          {
                              "id": "7769178",
                              "name": "Core i5",
                              "struct": null,
                              "source": 1
                          }
                      ],
                      "source": 1
                  },
                  {
                      "id": "MODEL",
                      "value_struct": null,
                      "values": [
                          {
                              "id": "6637008",
                              "name": "i5-9400F",
                              "struct": null,
                              "source": 1
                          }
                      ],
                      "attribute_group_id": "OTHERS",
                      "name": "Modelo",
                      "value_id": "6637008",
                      "value_name": "i5-9400F",
                      "attribute_group_name": "Outros",
                      "source": 1
                  }
              ],
              "differential_pricing": {
                  "id": 33580182
              },
              "original_price": null,
              "category_id": "MLB1693",
              "official_store_id": null,
              "catalog_product_id": "MLB13953199",
              "tags": [
                  "brand_verified",
                  "good_quality_picture",
                  "good_quality_thumbnail",
                  "immediate_payment",
                  "cart_eligible"
              ],
              "catalog_listing": true
          },
      ]
  }
  ```
  </details>

- `https://api.mercadolibre.com/items/$ItemID`: traz detalhes de um determinado produto, onde `$ItemID` é o `id` do produto a ser buscado. Por exemplo, se o `id` do produto for `MLB1341706310`, o retorno será parecido com esse:

  <details>
    <summary>Retorno da requisição de detalhes de um produto</summary>

    Esse retorno traz informações detalhadas sobre cada um dos produtos. Por exemplo, o `id` desse produto, o `title`, que o título do produto, `price`, que é o preço e assim por diante.


  ```json
  {
    "id": "MLB1341706310",
    "site_id": "MLB",
    "title": "Processador Gamer Amd Ryzen 5 2600 Yd2600bbafbox De 6 Núcleos E 3.9ghz De Frequência",
    "subtitle": null,
    "seller_id": 245718870,
    "category_id": "MLB1693",
    "official_store_id": 1929,
    "price": 1068,
    "base_price": 1068,
    "original_price": null,
    "currency_id": "BRL",
    "initial_quantity": 93,
    "available_quantity": 0,
    "sold_quantity": 50,
    "sale_terms": [],
    "buying_mode": "buy_it_now",
    "listing_type_id": "gold_special",
    "start_time": "2019-10-15T18:13:00.000Z",
    "stop_time": "2040-01-27T00:26:51.000Z",
    "condition": "new",
    "permalink": "https://produto.mercadolivre.com.br/MLB-1341706310-processador-gamer-amd-ryzen-5-2600-yd2600bbafbox-de-6-nucleos-e-39ghz-de-frequncia-_JM",
    "thumbnail_id": "852106-MLA42157659481_062020",
    "thumbnail": "http://http2.mlstatic.com/D_852106-MLA42157659481_062020-I.jpg",
    "secure_thumbnail": "https://http2.mlstatic.com/D_852106-MLA42157659481_062020-I.jpg",
    "pictures": [],
    "video_id": null,
    "descriptions": [
    ],
    "accepts_mercadopago": true,
    "non_mercado_pago_payment_methods": [
    ],
    "shipping": {},
    "international_delivery_mode": "none",
    "seller_address": {},
    "seller_contact": null,
    "location": {
    },
    "coverage_areas": [
    ],
    "attributes": [],
    "warnings": [
    ],
    "listing_source": "",
    "variations": [
    ],
    "status": "paused",
    "sub_status": [],
    "tags": [],
    "warranty": "Garantia de fábrica: 3 anos",
    "catalog_product_id": "MLB9196241",
    "domain_id": "MLB-COMPUTER_PROCESSORS",
    "parent_item_id": null,
    "differential_pricing": null,
    "deal_ids": [
    ],
    "automatic_relist": false,
    "date_created": "2019-10-15T18:13:00.000Z",
    "last_updated": "2022-02-05T06:46:48.434Z",
    "health": null,
    "catalog_listing": true,
    "channels": []
  }
  ```

  </details>

  </details>

# Requisitos do Projeto

## 1. (TDD) Desenvolvimento dos testes de no mínimo 25% de cobertura total e 100% da função `fetchProducts`

<details>
  <summary>
    Implementar os testes necessários na função <code>fetchProducts</code>
  </summary> <br />

O arquivo para implementação do teste se chama `fetchProducts.test.js` e se encontra dentro da pasta `tests`.

**O que você deve testar:**

- Testa se `fetchProducts` é uma função;

- Executa a função `fetchProducts` com o argumento `'computador'` e testa se `fetch` foi chamada;

- Testa se, ao chamar a função `fetchProducts` com o argumento `'computador'`, a função `fetch` utiliza o endpoint `'https://api.mercadolibre.com/sites/MLB/search?q=computador'`;

- Testa se o retorno da função `fetchProducts` com o argumento `'computador'` é uma estrutura de dados igual ao objeto `computadorSearch`, que já está importado no arquivo.

- Testa se, ao chamar a função `fetchProducts` sem argumento, retorna um erro com a mensagem: `'You must provide an url'`.

**O que será testado:**

- Será avaliado se os testes implementados atingem no mínimo 25% da cobertura total e 100% da função `fetchProducts`.

</details>

## 2. Criação de uma listagem de produtos

<details>
  <summary>
    Utilizar a função <code>fetchProducts</code> para criar uma listagem de produtos através da API do Mercado Livre.
  </summary> <br />

O arquivo da função `fetchProducts` se encontra dentro da pasta `helpers` e está importado dentro do arquivo HTML.

- Implementa a função `fetchProducts` para retornar a listagem de produtos;

- Utiliza o _endpoint_ `https://api.mercadolibre.com/sites/MLB/search?q=$QUERY`, onde:

  - O valor de `$QUERY` deve ser **obrigatoriamente** o termo `computador`;

  - O retorno de produtos se encontra no array `results`;

- Utiliza a função `createProductItemElement()` para criar os componentes _HTML_ referentes a um produto:

  - Adiciona cada elemento retornado da função `createProductItemElement(product)` como filho do elemento `<section class="items">`.

**Obs:** Foram utilzadas as variáveis fornecidas no código, elas devem se referir aos seguintes campos:

- `sku`: é o campo `id` retornado pela API;
- `name`: é o campo `title` retornado pela API;
- `image`: é o campo `thumbnail` retornado pela API.

Para executar sua função `fetchProducts` basta chamar no arquivo `script.js`;

<details>
<summary>Clique aqui para ver o retorno da API</summary>

```json
{
  "site_id": "MLB",
  "country_default_time_zone": "GMT-03:00",
  "query": "$computador",
  "paging": {...},
  "results": [
    {
      "id": "MLB2025368730",
      "site_id": "MLB",
      "title": "Computador Completo Fácil Intel Core I3 8gb Ssd 240gb ",
      "seller": {},
      "price": 1859.07,
      "prices": {},
      "sale_price": null,
      "currency_id": "BRL",
      "available_quantity": 100,
      "sold_quantity": 500,
      "buying_mode": "buy_it_now",
      "listing_type_id": "gold_pro",
      "stop_time": "2041-09-12T04:00:00.000Z",
      "condition": "new",
      "permalink": "https://produto.mercadolivre.com.br/MLB-2025368730-computador-completo-facil-intel-core-i3-8gb-ssd-240gb-_JM",
      "thumbnail": "http://http2.mlstatic.com/D_704139-MLB47542929423_092021-I.jpg",
      "thumbnail_id": "704139-MLB47542929423_092021",
      "accepts_mercadopago": true,
      "installments": {},
      "address": {},
      "shipping": {},
      "seller_address": {},
      "attributes": [],
      "differential_pricing": {},
      "original_price": 1999,
      "category_id": "MLB1649",
      "official_store_id": 3807,
      "domain_id": "MLB-DESKTOP_COMPUTERS",
      "catalog_product_id": null,
      "tags": [],
      "order_backend": 1,
      "use_thumbnail_id": true,
      "offer_score": null,
      "offer_share": null,
      "match_score": null,
      "winner_item_id": null,
      "melicoin": null,
      "discounts": null
    },
    // {...} restante da lista de produtos
  ],
  "sort": {...},
  "available_sorts": {...},
  "filters": {...},
  "available_filters": {...}
}

```
</details>

**O que será testado:**

- O elemento com classe `.item` deve ser cada item da lista de produtos.

</details>

## 3. (TDD) Desenvolvimento dos testes de no mínimo 50% de cobertura total e 100% da função `fetchItem`

<details>
  <summary>
    Implementa os testes necessários na função <code>fetchItem</code>
  </summary> <br />

**O que você deve testar:**

- Testa se `fetchItem` é uma função;

- Executa a função `fetchItem` com o argumento do item "MLB1615760527" e testa se `fetch` foi chamada;

- Testa se, ao chamar a função `fetchItem` com o argumento do item "MLB1615760527", a função `fetch` utiliza o endpoint "https://api.mercadolibre.com/items/MLB1615760527";

- Testa se o retorno da função `fetchItem` com o argumento do item "MLB1615760527" é uma estrutura de dados igual ao objeto `item` que já está importado no arquivo.

- Testa se, ao chamar a função `fetchItem` sem argumento, retorna um erro com a mensagem: `'You must provide an url'`.

**O que será testado:**

- Será avaliado se os testes implementados atingem no mínimo 50% da cobertura total e 100% da função `fetchItem`.

</details>

## 4. Adicionar o produto ao carrinho de compras

<details>
  <summary>
    Implementa a função <code>fetchItems</code> para retornar dados de um produto e adicioná-lo ao carrinho.
  </summary> <br />

Cada produto na página _HTML_ possui um botão com o nome `Adicionar ao carrinho` e, ao clicar nesse botão, deve realizar uma requisição que vai retornar todos os detalhes de um produto.

- Implementa a função `fetchItems` para fazer a requisição dos detalhes de apenas **um** produto;

- Utiliza o _endpoint_ `https://api.mercadolibre.com/items/$ItemID`, onde `$ItemID` é o `id` do produto a ser buscado;

- Utiliza a função `createCartItemElement()` para criar os componentes _HTML_ referentes a um item do carrinho;

**Obs:** `salePrice` é o campo `price` retornado pela API.

- Adiciona o elemento retornado da função `createCartItemElement(product)` como filho do elemento `<ol class="cart__items">`.

Por exemplo, se o `id` do produto for `MLB1341706310`, o retorno do _endpoint_ será algo no formato:

<details>
<summary><strong>Clique aqui para ver o retorno da API</strong></summary>

```json
{
    "id": "MLB1341706310",
    "site_id": "MLB",
    "title": "Processador Amd Ryzen 5 2600 6 Núcleos 64 Gb",
    "subtitle": null,
    "seller_id": 245718870,
    "category_id": "MLB1693",
    "official_store_id": 1929,
    "price": 879,
    "base_price": 879,
    "original_price": null,
    "currency_id": "BRL",
    "initial_quantity": 0,
    "available_quantity": 0,
    "sold_quantity": 0,
    //[...]
    "warranty": "Garantia de fábrica: 3 anos",
    "catalog_product_id": "MLB9196241",
    "domain_id": "MLB-COMPUTER_PROCESSORS",
    "parent_item_id": null,
    "differential_pricing": null,
    "deal_ids": [],
    "automatic_relist": false,
    "date_created": "2019-10-15T18:13:00.000Z",
    "last_updated": "2019-12-20T18:06:54.000Z",
    "health": null,
    "catalog_listing": true
}
```
</details>

**O que será testado:**

- O elemento com classe `.cart__items` deve adicionar o item escolhido, apresentando corretamente suas informações de id, título e preço.

</details>

## 5. Remover o item do carrinho de compras ao clicar nele

<details>
  <summary>
    Ao clicar no <strong>produto no carrinho de compra</strong>, ele deve ser removido da lista.
  </summary> <br />

Ao clicar em um dos itens do carrinho de compras, esse item deve ser removido da lista. Para isso:

- Utiliza a função `cartItemClickListener(event)` para implementar a lógica necessária para remover o item do carrinho.

**O que será testado:**

- Remove o item do carrinho de compras ao clicar nele;

</details>

## 6. (TDD) Desenvolvimento dos testes de no mínimo 75% de cobertura total e 100% da função `saveCartItems`

<details>
  <summary>
    Implementa os testes necessários na função <code>saveCartItems</code>
  </summary> <br />

O arquivo de teste se chama `saveCartItems.test.js` e se encontra dentro da pasta `tests`.

**O que você deve testar:**

- Testa se, ao executar `saveCartItems` com o argumento `<ol><li>Item</li></ol>`, o método `localStorage.setItem` é chamado;

- Testa se, ao executar `saveCartItems` com o argumento `<ol><li>Item</li></ol>`, o método `localStorage.setItem` é chamado com dois parâmetros, sendo o primeiro 'cartItems' e o segundo sendo o valor passado como argumento para `saveCartItems`.

**O que será testado:**

- Será avaliado se os testes implementados atingem no mínimo 75% da cobertura total e 100% da função `saveCartItems`.

</details>

## 7. (TDD) Desenvolvimento dos testes para atingir 100% de cobertura total e 100% da função `getSavedCartItems`

<details>
  <summary>
    Implementa os testes necessários na função <code>getSavedCartItems</code>
  </summary> <br />

O arquivo de teste se chama `getSavedCartItems.test.js` e se encontra dentro da pasta `tests`.

**O que você testar:**

- Testa se, ao executar `getSavedCartItems`, o método `localStorage.getItem` é chamado;

- Testa se, ao executar `getSavedCartItems`, o método `localStorage.getItem` é chamado com o 'cartItems' como parâmetro.

**O que será testado:**

- Será avaliado se os testes implementados atingem 100% da cobertura total e 100% da função `getSavedCartItems`.

</details>

## 8. Carregar o carrinho de compras ao iniciar a página

<details>
  <summary>
    Salva os itens adicionados no carrinho de compras no <code>localStorage</code>
  </summary> <br />

Ao carregar a página, o estado atual do carrinho de compras deve ser carregado do **LocalStorage**. Para que isso funcione, os itens do carrinho de compras devem ser salvos no **LocalStorage**, ou seja, a **adição** e **remoção** de um produto devem ser abordadas para que a lista esteja sempre atualizada.

Para isso, foram implementadas as funções `saveCartItems` e `getSavedCartItems` dentro da pasta `helpers`.

- Implementa a função `saveCartItems` que deve possuir a lógica para apenas **adicionar** o item no `localStorage` em uma chave chamada `cartItems`;

- Implementa a função `getSavedCartItems` que deve possuir a lógica para apenas **retornar** o item do `localStorage`.

⚠️ A função `saveCartItems` **não** deve recuperar os itens do `localStorage`. A função `getSavedCartItems` **não** deve adicionar um item no `localStorage`.

**O que será testado:**

- A página ao ser atualizada deve permanecer com todos os itens do carrinho adicionados anteriomente.

</details>

## 9. Calcular o valor total dos itens do carrinho de compras

<details>
  <summary>
    O elemento com o valor <strong>total</strong> dos produtos deve possuir a classe <code>total-price</code>
  </summary> <br />

Cada vez que o carrinho de compras é modificado, será necessário calcular o valor total dos produtos e apresentá-los na página principal do projeto.

- Implementa uma lógica para somar todos os produtos do carrinho;

- Cria um elemento com a classe `total-price` e adiciona o texto com o valor total dos produtos;

**O que será testado:**

- Calcula o valor total dos itens do carrinho de compras de forma assíncrona;

</details>

## 10. Limpar o carrinho de compras

<details>
  <summary>
    Implementa a lógica no botão <code>Esvaziar carrinho</code> para limpar o carrinho de compras
  </summary> <br />

- Certifica que o botão possui **obrigatoriamente** a classe `empty-cart`;

- Implementa a lógica para remover **todos** os itens do carrinho de compras;

**O que será testado:**

- Verifica o botão para limpar carrinho de compras;

</details>

## 11. Adicionar um texto de `carregando` durante uma requisição à API

<details>
  <summary>
    Adiciona um elemento com o texto <code>carregando...</code> durante a requisição à API
  </summary> <br />

Uma requisição à API gasta um certo tempo e durante esse processo a pessoa que está utilizando a página não tem como saber se a requisição deu certo ou não. Por isso, normalmente é utilizada alguma forma para mostrar que a requisição ainda está em andamento. Para isso:

- Cria um elemento que contenha o texto `carregando...`, que deve ser exibido em algum lugar da página;

- Adiciona a classe `loading` ao elemento que possui o texto `carregando...`;

- Exibe esse elemento apenas **durante** a requisição à API.

**O que será testado:**

- Verifica se adiciona um texto de "carregando" durante uma requisição à API.

</details>