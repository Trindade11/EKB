# Project Constitution

**Version**: 1.0.0 | **Ratified**: [DATE] | **Last Amended**: [DATE]

## Core Principles

### I. Visual Modeling First

Toda especificação e plano deve incluir diagramas visuais (Mermaid) para:
- Facilitar o entendimento por todos os stakeholders
- Identificar gaps, riscos e oportunidades antes da implementação
- Servir como documentação viva do sistema

**Regras**:
- Specification: deve incluir fluxo de processo/jornada do usuário
- Plan: deve incluir diagrama de arquitetura técnica e interações
- Fluxos entre agentes/componentes devem ser explicitamente mapeados

### II. User-Centric Communication

O usuário principal pode não ser desenvolvedor. Toda comunicação deve:
- Usar linguagem clara e acessível
- Explicar o propósito de cada ação/comando
- Evitar jargão técnico desnecessário sem explicação
- Fornecer passos completos e comandos prontos para executar

### III. Established Components Only

Preferir componentes, bibliotecas e padrões amplamente adotados:
- Usar drivers/SDKs oficiais sempre que disponíveis
- Evitar bibliotecas experimentais ou pouco mantidas
- Justificar explicitamente qualquer escolha fora do mainstream
- Priorizar soluções com documentação abundante e comunidade ativa

### IV. Stack Consistency

A stack tecnológica definida no Plan deve ser respeitada em toda implementação:
- Não sugerir tecnologias alternativas sem solicitação explícita
- Manter consistência com dependências já configuradas no projeto
- Respeitar configurações de ambiente (.env, MCP, etc.) já existentes

### V. Test-First Development

Testes são parte integral do desenvolvimento:
- Testes devem ser escritos/planejados antes da implementação
- Cada requisito funcional deve ter critério de aceitação testável
- Cobertura de testes deve ser considerada desde a especificação

### VI. Simplicity & YAGNI

Começar simples e adicionar complexidade apenas quando necessário:
- Evitar over-engineering e abstrações prematuras
- Implementar apenas o que foi especificado
- Refatorar quando a complexidade se justificar, não antes

### VII. Traceability & Auditability

Todo artefato deve ser rastreável:
- Especificações vinculadas a features
- Planos vinculados a especificações
- Tarefas vinculadas a planos
- Mudanças documentadas com motivo e data

## Quality Gates

### Gate 1: Specification Ready

- [ ] Fluxo de processo visualizado em Mermaid
- [ ] User stories priorizadas e independentemente testáveis
- [ ] Requisitos funcionais claros e sem ambiguidade
- [ ] Critérios de sucesso mensuráveis e technology-agnostic
- [ ] Máximo 3 itens marcados como [NEEDS CLARIFICATION]

### Gate 2: Plan Ready

- [ ] Diagrama de arquitetura técnica em Mermaid
- [ ] Stack tecnológica explicitamente definida
- [ ] Contratos/interfaces entre componentes documentados
- [ ] Estrutura de diretórios definida
- [ ] Constitution Check passou

### Gate 3: Implementation Ready

- [ ] Tarefas quebradas e priorizadas
- [ ] Cada tarefa vinculada a um requisito
- [ ] Critérios de aceitação definidos por tarefa
- [ ] Dependências entre tarefas mapeadas

## Governance

- Esta Constituição tem precedência sobre práticas ad-hoc
- Alterações requerem documentação, justificativa e atualização de versão
- Violações devem ser justificadas explicitamente no artefato relevante
- Revisões periódicas da Constituição são encorajadas conforme o projeto evolui
