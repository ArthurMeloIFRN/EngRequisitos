# Relatório de Validação de Requisitos  
**Projeto:** Sistema de Movimentações Financeiras  
**Técnica:** Revisão de Requisitos / Inspeção com Checklist  
**Data:** 21/07/2025

---

## 1. Checklist de Validação

| #  | Item do Checklist | Check? | Observações |
|----|-------------------|-----|-------------|
| 1  | Todos os requisitos necessários estão especificados? | ✅ | Há cobertura das principais funções do fluxo financeiro, porém faltam requisitos não-funcionais. |
| 2  | Os requisitos possuem identificadores únicos e padrão consistente? | ❌ | O RF003 está sem hífen, deveria ser RF-003 para padronização. |
| 3  | Os requisitos estão escritos de forma clara e sem ambiguidades? | ✅ | Em geral, os requisitos são claros, mas há margem para detalhar melhor "devolver para correção" no RF-003. |
| 4  | Os critérios de aceitação são suficientes para validar o requisito? | ❌ | Faltam critérios de aceitação mais detalhados no RF-003. |
| 5  | Existe conflito ou sobreposição entre requisitos? | ✅ | Nenhum conflito identificado entre os requisitos. |
| 6  | Os requisitos estão consistentes com os casos de uso? | ✅ | As origens dos requisitos estão devidamente indicadas (UC-001, UC-002, etc.). |
| 7  | Existem requisitos técnicos e restrições documentadas? | ❌ | Não foram definidos requisitos técnicos, ex: compatibilidade com sistemas legados, segurança, etc. |
| 8  | Os requisitos permitem rastreabilidade? | ✅ | Cada requisito possui origem associada ao caso de uso. |
| 9  | Os requisitos são testáveis? | ✅ | Os requisitos RF-001, RF-002 e RF-004 têm critérios testáveis. RF-003 precisa melhorar. |
| 10 | Há cobertura de exceções e fluxos alternativos? | ❌ | Exemplo: o que acontece se o arquivo CSV não puder ser gerado? Ou se houver falha no cálculo? |
| 11 | As prioridades estão atribuídas? | ✅ | As prioridades estão definidas (Alta / Média). |
| 12 | Existe preocupação com a usabilidade e interação? | ❌ | Não há requisitos sobre interface, tempo de resposta ou acessibilidade. |

---

## 2. Problemas Encontrados e Ações Corretivas

| Problema | Descrição | Impacto | Ação Corretiva | Responsável | Prazo |
|----------|-----------|----------|----------------|-------------|-------|
| Padrão inconsistente no ID do requisito | O requisito RF003 está sem o hífen usado nos demais IDs (RF-003). | Baixo | Corrigir para RF-003 para manter a padronização. | Equipe de Requisitos | 1 dia |
| Falta de detalhes no RF-003 | "Devolver despesa para correção" é vago – não há definição do que acontece após a devolução, nem quem corrige. | Médio | Especificar se o sistema envia notificação, se há histórico de devoluções, etc. | PO e Equipe de Requisitos | 2 dias |
| Critérios de aceitação insuficientes no RF-003 | Apenas diz "atualizar para devolvido", não define como isso será validado na interface ou relatórios. | Médio | Incluir critérios como: "A despesa devolvida deve aparecer em relatório com status atualizado e gerar log do evento". | Equipe de QA | 2 dias |
| Ausência de requisitos não-funcionais | Não há especificações sobre desempenho, segurança, integridade dos dados ou requisitos tecnológicos. | Alto | Criar requisitos não-funcionais mínimos (ex: tempo de resposta, segurança, compatibilidade com antena Incontrol). | Equipe técnica e de requisitos | 3 dias |
| Falta de cobertura de exceções | Não está previsto o que fazer em caso de erro na geração do CSV ou falha na integração com o sistema financeiro. | Médio | Adicionar requisitos de tratamento de exceções e mensagens de erro. | Equipe de Requisitos | 2 dias |
| Interface e usabilidade não especificadas | Não há requisitos sobre como os dados são exibidos (ex: grid responsivo, exportação direta do grid, validação de campos de filtro). | Baixo | Especificar requisitos de interface e usabilidade básicos. | Equipe de UX / PO | 3 dias |

---

## 3. Resumo da Validação

- **Completude:** Parcial (faltam requisitos não-funcionais e exceções)  
- **Consistência:** OK (poucas inconsistências)  
- **Clareza:** Boa, com pontos de melhoria no RF-003  
- **Padrões:** Pequena falha no padrão de IDs (RF003)  
- **Conflitos:** Nenhum identificado  
- **Erros técnicos:** Nenhum identificado, mas falta prever falhas operacionais  
- **Ambiguidade:** Detectada apenas no RF-003

---

## 4. Próximos Passos

- Atualizar o documento de requisitos com as correções listadas
- Realizar nova revisão após ajustes
- Incluir requisitos não-funcionais e exceções no próximo ciclo de documentação

---

## 5. Anexos

**Checklist Utilizado**  

| #  | Item do Checklist |
|----|-------------------|
| 1  | Todos os requisitos necessários estão especificados? |
| 2  | Os requisitos possuem identificadores únicos e padrão consistente? |
| 3  | Os requisitos estão escritos de forma clara e sem ambiguidades? |
| 4  | Os critérios de aceitação são suficientes para validar o requisito? |
| 5  | Existe conflito ou sobreposição entre requisitos? |
| 6  | Os requisitos estão consistentes com os casos de uso? |
| 7  | Existem requisitos técnicos e restrições documentadas? |
| 8  | Os requisitos permitem rastreabilidade? |
| 9  | Os requisitos são testáveis? |
| 10 | Há cobertura de exceções e fluxos alternativos? |
| 11 | As prioridades estão atribuídas? |
| 12 | Existe preocupação com a usabilidade e interação? |

---
