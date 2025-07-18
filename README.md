# rinha-de-backend-rb

# ✅ Rinha de Backend 2025 – Task List

Este arquivo organiza as tarefas para o desenvolvimento da API conforme os requisitos do desafio oficial.

---

## 📦 1. Preparação inicial

- [ ] Ler o `INSTRUCOES.md` do [repositório oficial](https://github.com/zanfranceschi/rinha-de-backend-2025/blob/main/INSTRUCOES.md)
- [ ] Escolher a stack principal (ex: Ruby on Rails)
- [ ] Criar o repositório do projeto
- [ ] Inicializar o projeto com a estrutura base
- [ ] Configurar o banco de dados PostgreSQL
- [ ] Configurar Docker (opcional, mas recomendado)

---

## 🧩 2. Modelagem e banco de dados

- [ ] Criar tabela `clientes` com saldo e limite
- [ ] Inserir os 5 clientes iniciais no banco (migrados via script ou seeds)
- [ ] Criar tabela `transacoes` com colunas necessárias
- [ ] Garantir integridade e performance com constraints e índices

---

## 📡 3. Endpoints da API

### `POST /clientes/:id/transacoes`

- [ ] Criar rota e controller
- [ ] Validar tipo da transação (`c` ou `d`)
- [ ] Verificar saldo antes de debitar
- [ ] Atualizar saldo do cliente com segurança (evitar race condition)
- [ ] Criar testes com RSpec para casos de sucesso e erro
- [ ] Retornar status e payload conforme especificação

### `GET /clientes/:id/extrato`

- [ ] Criar rota e controller
- [ ] Recuperar os últimos 10 lançamentos
- [ ] Incluir saldo total, data e limite na resposta
- [ ] Criar testes com RSpec para esse endpoint

---

## ⚙️ 4. Carga inicial

- [ ] Criar script ou seed para inserir os 5 clientes
- [ ] Garantir que clientes não sejam duplicados ao reiniciar

---

## 🚀 5. Performance e concorrência

- [ ] Configurar conexão pool adequada no banco
- [ ] Evitar N+1 queries
- [ ] Garantir atomicidade das transações
- [ ] Fazer testes de carga com `k6` ou `wrk`
- [ ] Testar múltiplas requisições concorrentes no mesmo cliente

---

## 🐳 6. Docker e Deploy

- [ ] Criar `Dockerfile` eficiente para produção
- [ ] Criar `docker-compose.yml` com PostgreSQL configurado
- [ ] Garantir que o app sobe com `docker-compose up`
- [ ] Permitir testes via `curl` ou Postman com contêiner rodando

---

## 🧪 7. Testes automatizados

- [ ] Escrever testes de unidade e integração com RSpec
- [ ] Incluir testes para limites, saldo negativo, tipos inválidos
- [ ] Rodar testes com cobertura mínima aceitável

---

## 📝 8. Documentação

- [ ] Escrever `README.md` com:
  - Stack utilizada
  - Como subir o projeto
  - Como rodar os testes
  - Como simular requisições
  - Como rodar com Docker
- [ ] Gerar documentação da API com `rswag` (opcional)

---

## 🔁 9. Testes e ajustes finais

- [ ] Rodar todos os testes
- [ ] Verificar mensagens de erro e status HTTP
- [ ] Ajustar possíveis problemas de concorrência
- [ ] Otimizar uso de memória e banco, se necessário
