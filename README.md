## Projeto "API REST" com JavaScript e Node.js, utilizando Supertest e Jest

Autor Moisés Ademir Chiaretto

Descrição das explicações de cada item da estrutura do projeto "API REST  com JavaScript e Node.js, utilizando Supertest e Jest desenvolvido.

O objetivo é desenvolver cenários de testes em JavaScript com Supertest e Jest, e a API REST utilizando os métodos / verbos HTTP (Get, Post, Put, Patch, Delete).

### Consultar no final desta documentação o _tópico_ "Configuração do Ambiente de Trabalho" e o _subtópico_ "Pré-requisitos".
<br>

|JavaScript		  |Node.js      	|Supertest  		|Jest          |API Rest  	|JSON    		|IDE VSCode     |
|---------------|---------------|---------------|--------------|------------|-----------|---------------|
| <img width="137" alt="00_JavaScript" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/16ff69d9-e76b-4fd6-8555-9685cbe99331"> | <img width="93" alt="00_Node_JS" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/f7db03c8-4d5b-4a98-852d-da955e1537f7"> | <img width="208" alt="00_SUPERTEST" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/aba922e2-e78a-4eea-94a6-f59e7b16b11b"> | <img width="70" alt="00_JEST" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/78f1a971-4cb5-4e13-9e62-f246308d3f62"> | ![10_API_REST](https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/4f125042-9982-4700-85fb-e7fc6c596b11) | <img width="164" alt="00_JSON" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/a2457247-4df1-4a66-9930-82690dcccc83"> | ![VS_CODE](https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/b39cdb57-4f18-4f8b-be33-8749f23b1e0b) |
<br>

## Estrutura do Projeto "API REST" JavaScript e Node.js, utilizando Supertest e Jest
<br>

<img width="236" alt="00_ESTRUTURA_PROJETO_SUPERTEST_JEST" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/5d51f00d-1456-474e-9c52-2361faf8dd1d">
<br>


## Cenários de Testes de API REST

CRUD com os verbos HTTP, métodos GetAll, GetId, Post, Put, Patch, Delete.
<br>

|Endpoint      	|Método		|Ação                                          		|
|---------------|---------|-------------------------------------------------|
|/users	  	    |GET		  |Retorna a lista de usuários			              	|
|/users	  	    |POST		  |Insere um novo usuário					                  |
|/users{id}    	|GET		  |Retorna o usuário com id = {id}			            |
|/users{id}	    |PUT	  	|Substitui os dados do usuário com id = {id}		  |
|/users{id}	    |PATCH		|Altera itens dos dados do usuário com id = {id}	|
|/users{id}	    |DELETE		|Remove o usuário com id = {id}				            |

<br>

![05_Piramide_Testes](https://github.com/moiseschiaretto/Java_API_Rest_Assured/assets/84775466/9b2a370b-1b74-458e-b158-b281456d6055)

<br>

## Script simples do Supertest
<br>

```

const request = require('supertest');

// Collection
describe('Request User - Method: ', () => {

  // Request GET ALL
    it('GET ALL - deve listar todos os usuários e o Status Code = ' + statusCodeGET, async () => {
      try{
          // Captura o tempo inicial
          const start = Date.now();
          const res = await request(baseUrl)
              .get(endPoint)
              .set('Accept', contentType)
              .expect('Content-Type', accept)
              .expect(statusCodeGET)
              // Imprime o JSON no console
              console.log('JSON:');
              console.log(res.body);
              // Captura o tempo final após a resposta ser recebida
              const end = Date.now();
              // Supertest não retorna responseTime diretamente, é necessário calcular responseTime manualmente
              verifyResponseTime(start, end); 
              // Utiliza as funções de assert separadas
              verifyStatusCodeGet(res.status);          
      } catch (error) {
          // Reportar o erro
          console.error('Erro na execução do teste:', error);
          throw error;
      }
  });
});

```

<br>

### Sintaxe da API Rest com Supertest
<br>

### _Em construção ..._


## Relatórios gerados da suíte de testes executada da "api_reqres.in"** 
<br>

**Jest HTML Reporter é um plugin para Jest** que gera relatórios de resultados de testes em formato HTML, oferecendo uma visualização detalhada e personalizável dos resultados dos testes JavaScript da API REST.

<br>

|Report com os Testes = PASSED	|Report com Error = ASYNC / AWAIT |Report com Error = Response Time |
|-------------------------------|---------------------------------|---------------------------------|
| <img width="525" alt="01_REPORT_JEST_OK" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/b9bf7c5f-d7c8-43eb-9aaf-e0393807bbc9"> | <img width="463" alt="02_REPORT_JEST_ERROR_ASYNC_AWAIT" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/7832fdea-4d7e-4c0b-a599-68e1b772a64b"> | <img width="459" alt="03_REPORT_JEST_ERROR_RESPONSE_TIME" src="https://github.com/moiseschiaretto/Supertest_Jest_API_REST/assets/84775466/480f5557-18e2-4c80-b73b-98add0b867cb"> |
<br>

