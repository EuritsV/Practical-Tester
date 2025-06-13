# Practical-Tester

# 📘 Estudo de Técnicas Avançadas de Teste de Software (PO-5 a PO-10)

Este repositório reúne resumos e exemplos práticos sobre técnicas avançadas de teste de software, com base nos objetivos práticos PO-5 a PO-10. Os conteúdos seguem boas práticas do ISTQB e da norma IEEE 29119-3:2021.

---

## ✅ PO-5: Test Case Prioritization

### 📌 Descrição
Ordena os casos de teste de forma a executar primeiro os mais importantes — aqueles que têm maior impacto no sistema ou maior probabilidade de encontrar defeitos.

### 🎯 Quando usar
- Em ciclos de regressão
- Sob restrições de tempo
- Para focar em funcionalidades críticas

### 💡 Benefícios
- Garante cobertura dos pontos mais importantes
- Aumenta a eficiência da execução de testes

---

## ✅ PO-6: Acceptance Test-Driven Development (ATDD)

### 📌 Descrição
Técnica onde os testes de aceitação são definidos antes do desenvolvimento, com colaboração entre programadores, testadores e stakeholders.

### 🎯 Quando usar
- Em ambientes ágeis
- Quando é necessário alinhar as funcionalidades aos requisitos de negócio

### 🤝 Participantes
- QA
- Devs
- Product Owner/Negócio

---

## ✅ PO-7: Preparing a Defect Report

### 📌 Descrição
Criação de relatórios claros e completos para comunicar defeitos encontrados.

### 🧱 Componentes
- Identificação do defeito
- Severidade e prioridade
- Passos para reproduzir
- Resultado esperado vs real
- Ambiente de teste
- Evidências (screenshot, logs, etc.)

### 🎯 Objetivo
Facilitar a correção eficaz e rápida pelo time de desenvolvimento.

---

## ✅ PO-8: Estimation Techniques

### 📌 Descrição
Técnicas usadas para estimar o esforço e duração das atividades de teste.

### 🔧 Técnica principal: Three Point Estimation (PERT)
\[
E = \frac{O + 4M + P}{6}
\]

- **O** = Otimista
- **M** = Mais provável
- **P** = Pessimista

### 🎯 Objetivo
Apoiar no planeamento, alocação de recursos e cronogramas realistas.

---

## ✅ PO-9: Application of Testing Techniques

### 📌 Descrição
Combinação de múltiplas técnicas aprendidas anteriormente para testar um sistema de forma integrada.

### 🧪 Técnicas combinadas:
- Equivalence Partitioning
- Boundary Value Analysis
- Decision Tables
- State Transition
- Test Case Prioritization

### 🏦 Exemplo prático
Sistema de banco online com:
- Login e MFA
- Transferência de fundos
- Pagamento de contas

Testes devem considerar diferentes estados, regras de negócio e limites numéricos, priorizando cenários críticos.

---

## ✅ PO-10: Create a Test Plan

### 📌 Descrição
Criação de um plano de testes completo conforme o padrão IEEE 29119-3:2021.

### 📄 Seções principais
- Introdução
- Visão Geral
- Itens de Teste
- Entregáveis
- Estratégia de Teste
- Cronograma
- Recursos
- Critérios de Entrada/Saída

### 🧭 Exemplo prático
Plano de teste para uma aplicação de lista de tarefas (To-Do App), incluindo registo, login, gestão e visualização de tarefas.

---

## 📎 Referências

- IEEE 29119-3:2021 – Software and Systems Engineering — Software Testing — Part 3: Test Documentation
- ISTQB Foundation Level Syllabus
- A4Q Practical Tester
- Princípios de Testes Ágeis e TDD/ATDD
- Técnicas de Estimativa PERT / Three-Point Estimation



