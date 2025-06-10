---

## Capítulo 6: ATDD – Acceptance Test-Driven Development

### ✅ O que é ATDD?

ATDD é uma prática de desenvolvimento baseada na colaboração entre todas as partes interessadas (negócio, QA, desenvolvimento), com foco em:

**Definir os testes de aceitação antes mesmo de o código ser escrito.**

### 🔍 Objetivo:

Garantir que:
- O que será desenvolvido é exatamente o que o cliente espera
- Todos entendem como o sucesso será medido

### 🧠 Como funciona o fluxo de ATDD?

1. **Conversa entre partes** (negócio, QA, dev)
2. **Definição dos critérios de aceitação**
3. **Criação dos testes de aceitação** (em linguagem clara)
4. **Desenvolvimento da funcionalidade**
5. **Execução dos testes de aceitação**
6. **Refinamento se necessário**

### 📌 Exemplo prático: Sistema de reservas online

**🧩 Nova funcionalidade:**
O utilizador pode cancelar reservas com mais de 24 horas de antecedência sem penalização.

#### ✍️ Critérios de aceitação (especificação do negócio)
- Usuário deve ver suas reservas
- Pode cancelar sem penalidade se > 24h antes
- Cancelação com < 24h gera multa
- Usuário recebe e-mail de confirmação

#### 🧪 Testes de aceitação definidos antes do desenvolvimento

| Teste | O que valida |
|-------|--------------|
| T1 | Visualização de reservas |
| T2 | Cancelamento com 25h de antecedência (sem penalidade) |
| T3 | Cancelamento com 23h de antecedência (com penalidade) |
| T4 | Recebimento de e-mail após cancelamento |

### 🧑‍💼 Onde entra o BDD?

BDD (Behavior-Driven Development) é uma forma de escrever os testes de aceitação de forma clara, legível e colaborativa, usando a estrutura:

```scss
Given (contexto)
When (ação)
Then (resultado)
```

#### 🧾 Tradução dos critérios de aceitação em BDD:

**✔️ Cenário 1 – Visualizar reservas**
```gherkin
Scenario: Viewing current bookings
  Given I am a logged-in user
  When I navigate to the "My Bookings" page
  Then I should see a list of my current bookings
```

**✔️ Cenário 2 – Cancelar com mais de 24h**
```gherkin
Scenario: Canceling a booking 25 hours before the scheduled time without a penalty
  Given I have a booking scheduled more than 24 hours from now
  When I cancel this booking
  Then the cancellation should be successful
  And I should not incur any penalty fee
```

**✔️ Cenário 3 – Cancelar com menos de 24h**
```gherkin
Scenario: Canceling a booking 23 hours before the scheduled time triggers a penalty fee
  Given I have a booking scheduled less than 24 hours from now
  When I attempt to cancel this booking
  Then the cancellation should be successful
  And I should incur a penalty fee
```

**✔️ Cenário 4 – Receber e-mail**
```gherkin
Scenario: Receiving a confirmation email upon successful cancellation
  Given I have successfully cancelled a booking
  When the cancellation process is completed
  Then I should receive a confirmation email detailing the cancellation
```

### 💡 Por que ATDD + BDD são tão eficazes?

| Benefício | Resultado |
|-----------|-----------|
| Alinha negócio, QA e dev | Todos sabem o que será entregue e como validar |
| Reduz retrabalho | Funcionalidade já é construída com base em testes de aceitação |
| Facilita automação | Os cenários podem ser automatizados com ferramentas BDD |
| Especifica usando exemplos reais | Ajuda a esclarecer regras ambíguas com base em situações reais |

### 🛠️ Ferramentas que suportam ATDD + BDD:

- **Cucumber** (Java, Ruby, JS, etc.)
- **SpecFlow** (.NET)
- **Behave** (Python)
- **Jest + Gherkin** (JS)
- **Robot Framework**

### 🎯 Conclusão prática

Se você quer:
- Garantir que todos entendam o que será feito
- Evitar retrabalho
- Melhorar a comunicação com stakeholders
- Criar testes automáticos úteis para regressão

**➡️ ATDD + BDD é uma abordagem poderosa e moderna.**

