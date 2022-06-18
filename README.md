<h1 align="center">  API SpringTestsDIO </h1>




## Tecnologias

 * Java 11
 * SpringFramework 2.5.4
 *  Banco de dados H2

## Features

 * Adicionar (nome do cliente e cep)
 * Listar do Endereço, Nome e ID
 * Buscar por ID
 * Remover endereço por ID

 ## Como utilizar


### Adicionando nome do clientes com cep na base de dados

**POST** `http://127.0.0.1:8080/clientes`

```json
// request
{
  "nome": "Marlos Igor",
  "endereco": {
    "cep": "01311000"
  }
}
```

```json
// response
{
  "id": 1,
  "nome": "Marlos Igor",
  "endereco": {
    "cep": "01311-000",
    "logradouro": "Avenida Paulista",
    "complemento": "até 609 - lado ímpar",
    "bairro": "Bela Vista",
    "localidade": "São Paulo",
    "uf": "SP",
    "ibge": "3550308",
    "gia": "1004",
    "ddd": "11",
    "siafi": "7107"
  }
}

```

### Listando endereço de clientes na base de dados

**GET** `http://127.0.0.1:8080/swagger-ui/index.html#/cliente-rest-controller/buscarTodos`

```json
// response
[
  {
    "id": 1,
    "nome": "Marlos Igor",
    "endereco": {
      "cep": "01311-000",
      "logradouro": "Avenida Paulista",
      "complemento": "até 609 - lado ímpar",
      "bairro": "Bela Vista",
      "localidade": "São Paulo",
      "uf": "SP",
      "ibge": "3550308",
      "gia": "1004",
      "ddd": "11",
      "siafi": "7107"
    }
  },
  {
    "id": 2,
    "nome": "Rita de Kassia",
    "endereco": {
      "cep": "20020-050",
      "logradouro": "Avenida Churchill",
      "complemento": "",
      "bairro": "Centro",
      "localidade": "Rio de Janeiro",
      "uf": "RJ",
      "ibge": "3304557",
      "gia": "",
      "ddd": "21",
      "siafi": "6001"
    }
  }
]
```

### Buscando endereço de clientes na base de dados por meio do ID

**GET** `http://127.0.0.1:8080/swagger-ui/index.html#/cliente-rest-controller/buscarPorId`

```json
// response 
{
  "id": 1,
  "nome": "Marlos Igor",
  "endereco": {
    "cep": "01311-000",
    "logradouro": "Avenida Paulista",
    "complemento": "até 609 - lado ímpar",
    "bairro": "Bela Vista",
    "localidade": "São Paulo",
    "uf": "SP",
    "ibge": "3550308",
    "gia": "1004",
    "ddd": "11",
    "siafi": "7107"
  }
}
```

### Excluindo endereço do clientes na base de dados por meio do ID

**DELETE** `http://127.0.0.1:8080/swagger-ui/index.html#/cliente-rest-controller/deletar`

![image](https://user-images.githubusercontent.com/18476294/174451990-0f099c53-9b6f-4836-9924-9b3586a880f3.png)


