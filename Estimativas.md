## Capítulo 8: Estimation Techniques

### 🧭 Objetivo do Capítulo

Aprender a estimar tempo, esforço e recursos necessários para as atividades de testes, permitindo melhor planeamento, gestão de recursos e entregas pontuais.

### 🎯 Por que Estimar?

- Evita subestimar ou superestimar esforço
- Ajuda a planear sprints, marcos e entregas
- Permite alocar testadores de forma inteligente
- Garante visibilidade ao time e aos stakeholders

### 🧠 Three Point Estimation (Técnica dos Três Pontos)

É baseada na técnica PERT, usando 3 cenários:

| Tipo de Estimativa | Significado | Símbolo |
|-------------------|-------------|---------|
| Optimistic | Cenário ideal (menos esforço ou duração) | O |
| Most Likely | Cenário mais realista | M |
| Pessimistic | Cenário mais difícil (mais esforço ou duração) | P |

**A fórmula é:**
```
E = (O + 4M + P) / 6
```

Ou seja, damos mais peso ao cenário mais provável (M).

### 🔍 Exemplo 1 – Estimativa de Esforço para Testes de Regressão Automatizados

**Valores:**
- O (Otimista) = 120 horas
- M (Mais provável) = 200 horas
- P (Pessimista) = 320 horas

**Aplicando a fórmula:**
```
E = (120 + 4(200) + 320) / 6 = 1240 / 6 = 206.67 horas
```

**🔵 Interpretação:**
Mesmo que o mais provável seja 200h, considerando incertezas, o esforço estimado realista é 206.67h.

### 🔍 Exemplo 2 – Estimativa de Duração para Testes de Performance

**Valores:**
- O (Otimista) = 15 dias
- M (Mais provável) = 25 dias
- P (Pessimista) = 40 dias

**Aplicando a fórmula:**
```
E = (15 + 4(25) + 40) / 6 = 155 / 6 = 25.83 dias
```

**🔵 Interpretação:**
Mesmo que o cenário provável seja 25 dias, a estimativa considerando riscos é 25.83 dias.

### ✍️ Como Aplicar na Prática (Passo a Passo)

1. **Levanta os 3 cenários** com base na tua experiência e input da equipa
2. **Aplica a fórmula:** E = (O + 4M + P) / 6
3. **Documenta as estimativas** num plano de testes, backlog ou ferramenta (como JIRA)
4. **Usa o valor E** como referência para o cronograma
5. **Acompanha a execução** para ajustar estimativas futuras com base na realidade

### 🧪 Exercício Rápido

**Cenário:** Estimar esforço de testes manuais num novo módulo.
- O = 40 horas
- M = 65 horas
- P = 90 horas

**Qual o esforço estimado?**
```
E = (40 + 4(65) + 90) / 6 = (40 + 260 + 90) / 6 = 390 / 6 = 65 horas
```

**🔵** A média ponderada coincide com o valor mais provável neste caso.

### ✅ Resumo

| Técnica | Fórmula | Utilidade Prática |
|---------|---------|-------------------|
| Three Point Estimation | (O + 4M + P) / 6 | Estimar esforço/duração com base em incertezas |

