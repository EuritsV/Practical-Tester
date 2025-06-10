## Capítulo 5: Test Case Prioritization

### ✅ O que é Test Case Prioritization?

É uma técnica usada para organizar a ordem de execução dos testes, com o objetivo de:

- **Detectar falhas críticas mais cedo**
- **Ganhar eficiência quando o tempo é limitado**
- **Reduzir custos de teste**
- **Focar nos testes que agregam mais valor ao negócio ou sistema**

### 🎯 Quando usar?

- Quando o tempo de execução é curto
- Em ciclos de teste contínuos (como em CI/CD)
- Quando há muitos testes automatizados
- Em sistemas complexos com funcionalidades críticas ou encadeadas

### 📊 Tipos de Prioritização

#### 1. Risk-Based Prioritization
Foca em testar primeiro os componentes com maior risco.

**✅ Considera:**
- Probabilidade de falha
- Impacto da falha

**🧾 Exemplo:** Num app bancário, teste do processamento de pagamento vem antes de "alterar tema do app".

#### 2. Coverage-Based Prioritization
Prioriza os testes que garantem maior cobertura de código, funcionalidades ou requisitos.

**✅ Útil em:**
- Funcionalidades novas ou alteradas
- Partes críticas com baixa cobertura anterior

**🧾 Exemplo:** Uma nova interface gráfica → priorizar testes sobre os elementos novos do UI.

#### 3. Requirements-Based Prioritization
Baseia-se na importância dos requisitos para o cliente/usuário final.

**✅ Pergunta:** "O que é mais essencial para o cliente funcionar com a aplicação?"

**🧾 Exemplo:** Para um app de streaming, login, busca e reprodução têm prioridade maior que personalização do avatar.

#### 4. Dependency-Based Prioritization
Prioriza os testes de funcionalidades que são pré-requisitos para outras.

**✅ Evita que testes falhem porque partes anteriores não funcionam**

**🧾 Exemplo real (e-commerce):**
- Precisas de registo antes de login
- Precisas de login antes de comprar

**🎯 Ordem correta:**
1. Cadastro
2. Login
3. Navegar
4. Adicionar ao carrinho
5. Checkout
6. Pagamento

### 🧪 Exemplo completo: E-commerce

| Test Case | Prioridade | Motivo |
|-----------|------------|--------|
| TC1: Registo do utilizador | Alta | É a base para todas as ações seguintes |
| TC2: Login | Alta | Necessário para acessar funcionalidades |
| TC3: Navegar entre produtos | Média | Depende do login |
| TC4: Adicionar item ao carrinho | Média | Depende da navegação |
| TC5: Checkout | Alta | Processo vital para completar a compra |
| TC6: Pagamento | Alta | Fim do fluxo de compra, altamente crítico |

**📌 Ordem de execução:** TC1 → TC2 → TC3 → TC4 → TC5 → TC6

### 🔁 Exemplo abstrato

| Teste | Prioridade | Depende de | Descrição curta |
|-------|-----------|------------|-----------------|
| TCX | Alta | Nenhum | Inicializa o componente |
| TCZ | Alta | TCX | Configura serviços externos |
| TCY | Média | TCX, TCZ | Testa a comunicação |
| TCW | Baixa | TCY | Executa função secundária |
| TCV | Alta | TCW, TCZ | Valida o resultado final |

**📌 Ordem final:** TCX → TCZ → TCY → TCW → TCV

### 🛠️ Como aplicar Test Case Prioritization no mundo real

1. **Liste todos os testes**
2. **Avalie cada um com base em:**
   - Risco (impacto x probabilidade)
   - Relevância para o cliente
   - Cobertura do sistema
   - Dependência de outros testes
3. **Classifique-os como:** Alta, Média ou Baixa prioridade
4. **Reordene sua suíte de testes**
5. **Execute em ordem ou por grupo de prioridade**

### 📌 Dica prática

**Se quiser automatizar, pode usar ferramentas como:**
- **TestRail, Xray, Zephyr** → Suporte para priorização manual ou automática
- **CI/CD pipelines** → Priorize testes críticos antes dos testes de regressão

