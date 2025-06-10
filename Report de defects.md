## Capítulo 7: Defect Report

### 🎯 Objetivo do Capítulo

Ensinar como criar relatórios de defeitos eficazes, comunicando problemas encontrados durante os testes de forma clara e completa para facilitar a correção pela equipa de desenvolvimento.

### 🧱 Estrutura de um Relatório de Defeito

#### 1. Defect Identification (Identificação do Defeito)

**🔍 O que é?**
Reconhecer corretamente um comportamento anômalo no software, baseado no comportamento esperado.

**✅ Exemplo prático:**
O botão "Salvar" não faz nada quando clicado, mesmo com campos preenchidos corretamente.

#### 2. Severity and Priority (Severidade e Prioridade)

**🔥 Severidade:** Impacto funcional do defeito.
**🚨 Prioridade:** Urgência para corrigir o defeito.

**🪧 Exemplo:**
- **Crítico (Critical):** A app crasha ao iniciar. (Alta severidade e prioridade)
- **Baixa (Low):** Texto desalinhado. (Baixa severidade, baixa prioridade)

#### 3. Reproducibility (Reprodutibilidade)

**🔁 Passos claros e detalhados** para que qualquer membro da equipa consiga reproduzir o problema.

**✍️ Exemplo de passos:**
1. Abrir app
2. Preencher login com dados válidos
3. Clicar em "Entrar"
4. Erro aparece sem efetuar login

#### 4. Expected vs Actual Results (Resultado Esperado vs Real)

**⚖️ Comparação clara** entre o que deveria acontecer e o que de facto aconteceu.

**📌 Exemplo:**
- **Esperado:** O utilizador é redirecionado para o dashboard.
- **Real:** Mensagem de erro "Login inválido", mesmo com dados corretos.

#### 5. Environment Details (Detalhes do Ambiente)

**🖥️ Detalhes técnicos** do ambiente de teste: versão da aplicação, SO, navegador, dispositivo.

**🧪 Exemplo:**
- App v1.5
- iPhone 12, iOS 14.4
- Rede Wi-Fi

#### 6. Evidence (Evidência)

**📸 Provas visuais ou técnicas** que reforcem o defeito: print screens, logs, vídeos.

**📂 Exemplo:**
- Vídeo a mostrar a tentativa de login com falha
- Captura de ecrã do erro

### 📘 Exemplos Práticos do Capítulo

#### 📍 Exemplo 1: Problema no Carrinho de Compras

- **Descrição:** Itens desaparecem do carrinho ao sair da página
- **Severidade:** Alta (afeta vendas)
- **Prioridade:** Alta
- **Passos:** login → adicionar ao carrinho → ir à homepage → voltar → carrinho vazio
- **Ambiente:** Web v2.1, Chrome 90, Windows 10
- **Evidência:** Screenshot do carrinho vazio

#### 📍 Exemplo 2: Falha no Login Mobile

- **Descrição:** Não é possível entrar com credenciais válidas
- **Severidade:** Crítica
- **Prioridade:** Alta
- **Ambiente:** App mobile v1.5, iPhone 12, iOS 14.4
- **Evidência:** Vídeo da falha

