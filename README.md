# 💸 App Finanças Inteligentes com Vibe Coding
Projeto feito por meio do lovable e copilot com o intuito de fazer um app de finanças pra DIO.



'''markdown
# PRD REFINADO
## PRD — App de Finanças Conversacional com Design Universal e Integração Completa da IA

## Contexto
Criar um aplicativo de Organização de Finanças Pessoais que funcione por meio de conversas naturais com o usuário.  
A proposta é simplificar o controle financeiro, eliminando planilhas e formulários complexos, com um design universal que ofereça boa experiência para o máximo de pessoas possíveis.  
A IA deve estar totalmente integrada ao núcleo do aplicativo, garantindo que cada interação do usuário seja refletida em metas, relatórios e dashboards.

## Problema
Muitos usuários abandonam apps de finanças por exigirem entradas manuais e oferecerem pouca personalização.  
A solução é uma experiência conversacional com recomendações automáticas e personalizadas, acessível e inclusiva para diferentes perfis de usuários.  
É essencial que a IA interaja constantemente tanto com as ações desejadas pelo usuário quanto com a inserção de informações no aplicativo, persistindo os dados no backend.  
Outro ponto crítico: não devem existir informações predefinidas no sistema. Cada pessoa deve inserir seus próprios gastos e receitas, garantindo personalização e relevância.

## Público-Alvo
Pessoas que desejam começar a organizar suas finanças de forma prática e sem complicações — especialmente iniciantes e jovens adultos.  
O design universal garante que o app seja útil também para pessoas com diferentes níveis de habilidade digital, idades e necessidades específicas.

## Funcionalidades-Chave
1. Registro de gastos via chat em linguagem natural.  
2. Classificação automática das transações por categoria.  
3. Definição e acompanhamento de metas financeiras.  
4. Dicas personalizadas de economia fornecidas por um “Agente Financeiro” virtual.  
5. Relatórios simples e visuais, com insights sobre hábitos de consumo.  
6. Design universal e inclusivo, garantindo acessibilidade (ex: contraste adequado, navegação intuitiva, suporte a leitores de tela).  
7. Interação constante da IA com o usuário, transformando comandos em ações persistentes no backend.  
8. Ausência de dados predefinidos: cada usuário deve inserir suas próprias receitas e despesas.  
9. Feedback imediato da IA confirmando quando uma ação foi aplicada com sucesso (ex: “Meta de R$500/mês criada. Você pode acompanhar no dashboard.”).

## MVP — Plano Inicial

### Telas Essenciais
- Chat Financeiro: interface principal para registrar gastos e receber dicas.  
- Resumo Mensal: visão geral dos gastos, metas e saldo.  
- Metas: definir e acompanhar objetivos financeiros.  
- Relatórios: gráficos simples com categorias de gastos.  
- Configurações: preferências de idioma, notificações e perfil.  

### Recursos Técnicos
- NLP (Processamento de Linguagem Natural) para entender o chat  
- Classificador de transações por texto  
- Motor de metas e alertas  
- Sistema de recomendações financeiras  
- Backend com banco de dados seguro  
- Frontend mobile-first com padrões de acessibilidade (WCAG)  
- Mecanismo de integração contínua da IA com o backend (cada comando gera uma ação persistente)  
- Estrutura de dados totalmente personalizada pelo usuário (sem valores predefinidos)  
- Sistema de feedback imediato da IA para confirmar ações aplicadas  

### Validação Inicial
- Teste com 10–20 usuários reais  
- Métricas:
  - % de usuários que registram gastos por 7 dias
  - Feedback sobre clareza das dicas
  - Taxa de retorno ao app após 1 semana  
- Ferramentas:
  - Formulário de feedback
  - Entrevistas curtas
  - Analytics básico  

## Conceito de Design Universal
Design Universal é uma abordagem de design que busca criar produtos, serviços e ambientes que possam ser usados pelo maior número possível de pessoas, sem necessidade de adaptação ou design especial.

Princípios básicos:
- Equidade: todos devem conseguir usar, independentemente de idade ou habilidade.  
- Flexibilidade: oferecer diferentes formas de interação (ex: texto, voz).  
- Simplicidade: interfaces claras e intuitivas.  
- Perceptibilidade: informações acessíveis mesmo para quem tem limitações visuais ou auditivas.  
- Tolerância ao erro: reduzir riscos e permitir correções fáceis.  
- Baixo esforço físico/cognitivo: não exigir muito esforço para usar.  
- Espaço adequado: considerar diferentes dispositivos e contextos de uso.  

Aplicar design universal no app significa que qualquer pessoa, desde um jovem acostumado com tecnologia até alguém com pouca familiaridade digital ou com necessidades especiais, terá uma boa experiência.
'''

## CORREÇÕES NECESSÁRIAS NO LOVABLE:
'''
requirements:
  integration_ai:
    objective: "Garantir que a IA se comunique corretamente com todos os componentes do sistema."
    functional:
      - "IA deve consumir dados dinâmicos fornecidos pelo usuário, sem valores fixos/hardcoded."
      - "Comunicação via endpoints documentados (REST/GraphQL) com formatos de dados definidos (JSON/XML)."
      - "Mecanismo de fallback para falhas de integração, retornando mensagens claras ao usuário."
    acceptance_criteria:
      - "Testes unitários e de integração validam cada fluxo de comunicação."
      - "Logs registram erros de integração com detalhes suficientes para diagnóstico."

  personalization_data:
    objective: "Garantir que cada usuário insira e visualize apenas suas próprias informações."
    functional:
      - "Sistema não deve carregar informações default fixas na interface."
      - "Cada usuário deve ser identificado por autenticação (login/cadastro)."
      - "Dados inseridos devem ser persistidos em banco de dados e recuperados apenas para o respectivo usuário."
      - "Campos obrigatórios devem ser validados no momento da inserção."
    acceptance_criteria:
      - "Usuário visualiza apenas suas informações previamente cadastradas."
      - "Dados de um usuário não aparecem para outro."
      - "Não deve existir nenhum dado hardcoded visível em produção."
      '''

### RESULTADO FINAL NO LOVABLE: https://talk-finance-buddy.lovable.app

<img width="1271" height="872" alt="image" src="https://github.com/user-attachments/assets/05f1b73a-3ca3-4d28-89cf-bb55ccfad8c6" />

# 💬 Finanças Inteligentes — App de Organização Financeira com IA Conversacional

## 🎯 Propósito
Simplificar a organização das finanças pessoais por meio de uma **experiência conversacional com IA integrada**, eliminando planilhas e interfaces complexas. O app é acessível, inclusivo e altamente personalizado, ideal para iniciantes e pessoas com diferentes níveis de habilidade digital.

## 👥 Público-Alvo
- Jovens adultos e iniciantes em finanças
- Pessoas com pouca familiaridade digital
- Usuários com necessidades específicas de acessibilidade

## 🧠 Como Funciona
- Interface principal via **chat em linguagem natural**
- IA interpreta comandos, classifica transações e atualiza dados em tempo real
- Design universal com navegação intuitiva e suporte a leitores de tela

## 📊 Funcionalidades Visíveis no Dashboard
Exemplo de visão mensal para o usuário Andrew Henriques Moncrieff:

| Seção                     | Descrição                                                                 |
|--------------------------|---------------------------------------------------------------------------|
| **Saldo do Mês**         | R$ 1234.00 — valor restante após receitas e despesas                      |
| **Receitas do Mês**      | R$ 2700.00 — total de entradas cadastradas pelo usuário                   |
| **Despesas do Mês**      | R$ 1466.00 — total de gastos, classificados automaticamente               |
| **Meta de Economia**     | R$ 1234.00 economizados de uma meta de R$ 3000.00 (41% concluído)         |
| **Gastos por Categoria** | Alimentação (R$ 1200.00) e Outros (R$ 266.00) — visualizados em gráfico    |

## 🔧 Funcionalidades-Chave
- Registro de gastos via chat
- Classificação automática por categoria
- Definição e acompanhamento de metas
- Dicas personalizadas de economia via agente virtual
- Relatórios visuais com insights de consumo
- Design universal e acessível (WCAG)
- IA integrada com backend persistente
- Dados 100% personalizados pelo usuário
- Feedback imediato da IA confirmando ações

## 🛠️ Recursos Técnicos
- NLP para entender linguagem natural
- Classificador de transações
- Motor de metas e alertas
- Sistema de recomendações financeiras
- Backend seguro com dados isolados por usuário
- Frontend mobile-first com acessibilidade
- Integração contínua da IA via APIs (REST/GraphQL)
- Logs e testes de integração para confiabilidade

## ✅ Garantias Técnicas

### `integration_ai`
- IA consome dados dinâmicos do usuário (sem valores fixos)
- Comunicação via endpoints documentados (REST/GraphQL)
- Fallback para falhas com mensagens claras
- Testes e logs para validação e diagnóstico

### `personalization_data`
- Sem dados default visíveis na interface
- Autenticação obrigatória por usuário
- Dados persistidos e isolados por conta
- Validação de campos obrigatórios
- Garantia de privacidade e personalização

## 🧪 MVP — Validação Inicial
- Testes com 10–20 usuários reais
- Métricas:
  - % de usuários que registram gastos por 7 dias
  - Clareza das dicas personalizadas
  - Taxa de retorno após 1 semana
- Ferramentas:
  - Formulário de feedback
  - Entrevistas curtas
  - Analytics básico

## 🧩 Design Universal
Princípios aplicados:
- Equidade e flexibilidade de uso
- Interfaces simples e perceptíveis
- Tolerância ao erro e baixo esforço cognitivo
- Espaço adequado para diferentes dispositivos

---

> Este app transforma o controle financeiro em uma conversa inteligente, acessível e personalizada.

# REFLEXÃO:
- O design e a criação das paginas foram bem acessiveis e faceis, principalmente pela ajuda do copilot. As maiores dificuldades foram encontradas na falta de recursos do lovable já que possui uma quantidade de uso limitada, dificultando assim o ponto mais dificel que foi a integração da IA com os elementos do site. As IAs são humanos só que mais práticos e prestativos te dando aconselhamentos e se adaptando por meio da comunicação que se dirije a ela. 




