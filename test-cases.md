# Casos de Teste — API de Produtos

## 1. Objetivo

Validar o comportamento de uma API REST de produtos por meio de cenários positivos e negativos.

## 2. Ambiente de teste

- **API:** DummyJSON
- **URL base:** https://dummyjson.com
- **Recurso:** `/products`
- **Documentação:** https://dummyjson.com/docs/products
- **Ferramenta de execução:** Postman

## 3. Casos de teste

| ID | Cenário | Requisição | Resultado esperado |
|---|---|---|---|
| API-001 | Consultar lista de produtos | GET `/products` | HTTP 200; lista de produtos e campos de paginação presentes |
| API-002 | Consultar produto existente | GET `/products/1` | HTTP 200; produto retornado com ID 1 |
| API-003 | Consultar produto inexistente | GET `/products/999999` | HTTP 404 e resposta de erro |
| API-004 | Validar tipos de dados | GET `/products/1` | ID numérico, título textual e preço numérico |
| API-005 | Buscar produtos por termo | GET `/products/search?q=phone` | HTTP 200 e estrutura de resposta válida |

## 4. Critérios de validação

- Código de status HTTP.
- Estrutura e conteúdo do JSON.
- Presença dos campos esperados.
- Tipos de dados.
- Mensagens de erro e tratamento de recursos inexistentes.

## 5. Execução e evidências

Os casos serão executados no Postman. Os resultados reais, incluindo aprovações, falhas e eventuais divergências, serão registrados após a execução.

**Observação:** os resultados esperados devem ser confirmados na documentação e na execução da API. A DummyJSON é uma API de demonstração; operações de escrita podem ser simuladas.

## 6. Status

Em desenvolvimento.
