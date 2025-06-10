# Capítulo 11: Application of Testing Techniques (PO-9)

## 🎯 Objetivo Principal
O objetivo do PO-9 é integrar as técnicas de teste aprendidas desde PO-1 até PO-8, equipando-o para aplicar estas técnicas de forma abrangente e simultânea a um Sistema em Teste (SUT), melhorando a capacidade de descobrir uma maior variedade de defeitos e garantir a confiabilidade do sistema.

## 🧱 Revisão das Técnicas de Teste (PO-1 a PO-8)

| Técnica | Descrição | Quando é Mais Eficaz |
|---------|-----------|---------------------|
| **Equivalence Partitioning (PO-1)** | Divide os dados de entrada em partições que devem exibir comportamento similar. Apenas um valor representativo de cada partição é testado. | Quando se pode categorizar dados de entrada em conjuntos que devem comportar-se identicamente, reduzindo o número de casos de teste mantendo a cobertura. |
| **Boundary Value Analysis (PO-2)** | Foca nos valores nas bordas de cada partição de equivalência. Como erros são frequentemente encontrados nas bordas dos intervalos de entrada, esta técnica testa estes valores limite. | Para identificar erros nos limites entre partições, que são locais comuns para bugs. |
| **Decision Tables (PO-3)** | Método usado para funções que respondem a uma combinação de entradas ou eventos. Envolve criar uma tabela que cobre todas as combinações possíveis de condições e ações correspondentes. | Especialmente útil quando se lida com regras de negócio complexas ou relações lógicas que afetam decisões da aplicação. |
| **State Transition (PO-4)** | Testa as transições entre diferentes estados numa aplicação, usando um diagrama de transição de estados para modelar os vários estados e os triggers que resultam em transições. | Melhor para aplicações onde é necessário verificar respostas adequadas a sequências de eventos, especialmente em sistemas como processos de login ou qualquer máquina baseada em estados. |
| **Test Case Prioritization (PO-5)** | Envolve ordenar casos de teste de modo que aqueles com maior impacto ou probabilidade de encontrar defeitos sejam executados primeiro. | Útil para reduzir tempo de testes de regressão ou quando os testes estão sob restrições de tempo, garantindo que funcionalidades críticas sejam testadas primeiro. |
| **ATDD (PO-6)** | Envolve membros de várias disciplinas (desenvolvimento, teste, stakeholders de negócio) definindo critérios de aceitação e criando testes de aceitação antes do desenvolvimento começar. | Altamente eficaz para alinhar o trabalho de desenvolvimento com necessidades de negócio e garantir que todos os stakeholders tenham uma compreensão clara dos requisitos. |
| **Defect Report (PO-7)** | Foca nas competências necessárias para reportar defeitos encontrados durante os testes de forma precisa e eficaz. | Essencial para garantir que defeitos sejam comunicados às equipas de desenvolvimento de forma a acelerar correções, melhorando a qualidade e confiabilidade da aplicação. |
| **Estimation Techniques (PO-8)** | Técnicas usadas para estimar o esforço e recursos necessários para atividades de teste. | Crítico para planeamento e alocação de recursos, ajudando a gerir tempo e expectativas ao longo do ciclo de vida dos testes. |

## 🧭 Seleção de Técnicas

### Processo de Análise do SUT
1. **Análise das Características**
   - Revisar funcionalidade, complexidade e tipos de interações do utilizador
   - Considerar o domínio da aplicação (financeiro, saúde, software de consumo)
   - Diferentes domínios podem favorecer certas técnicas devido a cenários regulamentares ou casos de uso típicos

2. **Correlação com Técnicas**
   - **Regras de negócio complexas** → **Decision Tables** são particularmente eficazes
   - **Aplicações web com várias entradas de utilizador** → **Equivalence Partitioning** e **Boundary Value Analysis**
   - **Sistemas com sequências de eventos ou mudanças de estado** → **State Transition** testing
   - **Projetos com restrições de tempo** → **Test Case Prioritization**

## 🏦 Exemplo Prático: Sistema Bancário Online

### Descrição do Sistema em Teste (SUT)

#### Visão Geral da Funcionalidade:
- **Autenticação de Utilizador**: Permite aos utilizadores fazer login com username e password
- **Gestão de Conta**: Utilizadores podem ver saldo da conta, transações recentes e gerir definições da conta
- **Transferência de Fundos**: Utilizadores podem transferir fundos entre as suas próprias contas ou para contas de outros utilizadores dentro do mesmo banco
- **Pagamento de Contas**: Utilizadores podem pagar contas diretamente das suas contas para beneficiários registados

#### Tipos de Utilizador:
- **Utilizador Regular**: Tem acesso a funcionalidades básicas como ver detalhes da conta e transferir fundos
- **Utilizador Admin**: Além das capacidades de utilizador regular, pode gerir contas de utilizador e ajustar definições do sistema

#### Funcionalidades Especiais:
- **Autenticação Multi-Factor (MFA)**: Obrigatória para completar transações financeiras
- **Limites de Transação**: Existem limites diários e transacionais baseados no tipo de conta e definições do utilizador

### Aplicação Combinada das Técnicas

#### **Passo 1: Revisão das Técnicas de Teste**
Começamos por revisar técnicas como Equivalence Partitioning, Boundary Value Analysis, Decision Table Testing, State Transition e Test Case Prioritization dos PO-1 a PO-8.

#### **Passo 2: Seleção de Técnicas**
- **Equivalence Partitioning**: Útil para testar funcionalidade de login particionando dados de entrada em credenciais válidas e inválidas
- **Boundary Value Analysis**: Eficaz para testar casos extremos de limites de transação
- **Decision Table Testing**: Ideal para testar várias combinações de definições de conta e tipos de transação
- **State Transition**: Crucial para testar mudanças no estado da conta após várias tentativas de transação, tanto falhadas como bem-sucedidas

#### **Passo 3: Desenvolvimento de Casos de Teste Integrados**

##### **Caso de Teste 1: Funcionalidade de Login**
- Usar **Equivalence Partitioning** para criar casos de teste para diferentes tipos de utilizador com cenários de entrada válidos e inválidos
- Aplicar **Boundary Value Analysis** para testar a resposta a comprimentos mínimos e máximos de entrada para username e password

##### **Caso de Teste 2: Transferência de Fundos**
- Usar **Decision Table Testing** para avaliar diferentes cenários de transferência: dentro das contas do utilizador, para contas externas, com ou sem exceder limites diários
- **State Transition** testing para verificar estado da conta após transferências bem-sucedidas e mal-sucedidas, incluindo testar o passo MFA

##### **Caso de Teste 3: Pagamento de Contas**
- Combinação de **Equivalence Partitioning** (para diferentes contas de beneficiários) e **Boundary Value Analysis** (para campos de montante perto dos limites superiores e inferiores)

#### **Passo 4: Implementação de Cenários de Teste**
Executar os casos de teste desenhados, focando nos pontos de integração entre funcionalidades, como a ligação entre login e autorização de transação.

## 🔄 Execução e Monitorização

### Estratégia de Execução
1. **Priorização** usando Test Case Prioritization para casos críticos
2. **Foco em pontos de integração** entre diferentes funcionalidades
3. **Monitorização contínua** dos resultados e ajuste da estratégia conforme necessário
4. **Documentação** de defeitos usando técnicas do PO-7

### Benefícios da Abordagem Combinada
- **Cobertura Abrangente**: Diferentes técnicas cobrem diferentes aspectos do sistema
- **Eficiência Melhorada**: Redução de redundância através da seleção estratégica de técnicas
- **Deteção de Defeitos Aumentada**: Maior probabilidade de encontrar defeitos através de múltiplas perspectivas
- **Confiabilidade do Sistema**: Teste mais robusto resulta em maior confiança na qualidade do software

