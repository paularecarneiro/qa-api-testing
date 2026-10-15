# Resultados dos Testes de API

## 1. Ambiente

- **API:** DummyJSON
- **URL base:** https://dummyjson.com
- **Ferramenta:** Postman Lightweight API Client
- **Data das execuções:** outubro de 2026

## 2. Resumo das execuções

| ID | Cenário | Status HTTP observado | Verificações aprovadas | Resultado |
|---|---|---|---|---|
| API-001 | Consultar lista de produtos | 200 OK | 4/4 | Aprovado |
| API-002 | Consultar produto por ID | 200 OK | 4/4 | Aprovado |
| API-003 | Consultar produto inexistente | 404 Not Found | 3/3 | Aprovado |

## 3. Evidências e validações

### API-001 — Listar produtos

- Verificação do status HTTP 200.
- Verificação do formato JSON.
- Verificação da existência e do tipo da lista `products`.
- Verificação dos campos numéricos `total`, `skip` e `limit`.
- Resultado observado: 4 de 4 verificações aprovadas.

### API-002 — Consultar produto por ID

- Verificação do status HTTP 200.
- Validação de que o ID retornado é 1.
- Validação de que o título é um texto não vazio.
- Validação de que o preço é numérico.
- Resultado observado: 4 de 4 verificações aprovadas.

### API-003 — Consultar produto inexistente

- Verificação do status HTTP 404.
- Verificação da existência de uma mensagem de erro.
- Validação de que a mensagem é um texto não vazio.
- Resultado observado: 3 de 3 verificações aprovadas.

## 4. Conclusão

Os três cenários executados atenderam às respectivas verificações automatizadas.

Os resultados se referem às execuções registradas no Postman e não representam uma garantia de comportamento em todas as condições ou ambientes.

## 5. Próximas etapas

- Executar testes adicionais de contrato e tipos de dados.
- Organizar as requisições e os scripts em uma coleção Postman.
- Registrar evidências das execuções.
- Avaliar cenários adicionais de tratamento de erros.
