# Pilar 2 — Pesquisa e orquestração com subagentes

## Três camadas de pesquisa

1. **Stack:** padrões da linguagem, runtime, framework e ecossistema nas versões identificadas.
2. **Harness da stack:** instruções para agentes, documentação versionada, ferramentas oficiais, integração com compilador/testes e limites conhecidos. Não encontrar orientação oficial é um resultado válido.
3. **Cada pilar:** busque padrões específicos da stack para arquitetura, testes, segurança, dados, UI ou processamento assíncrono, operação e manutenção. Produto/features pode usar evidência local e entrevistas em vez de pesquisa externa; padrões técnicos que sustentam a feature continuam exigindo pesquisa.

Use documentação oficial versionada, especificações, advisories e publicações do mantenedor. Material comunitário pode gerar hipóteses, mas não deve sustentar sozinho uma regra técnica. Não use resposta de busca ou resumo do subagente como única prova; confira os trechos decisivos e a versão. Nunca envie código privado, logs pessoais ou segredos nas consultas.

## Divisão do trabalho

O orquestrador primeiro consolida o perfil. Depois delega assuntos independentes, por exemplo: arquitetura/linguagem; qualidade; segurança; banco; contexto específico. Dê a cada subagente escopo e responsabilidade claros; pesquisadores ficam em leitura. Ajuste concorrência ao tamanho do projeto e orçamento. Não repita a mesma pesquisa em vários agentes sem finalidade de revisão.

### Prompt reutilizável

> Pesquise `<pilar>` para `<contexto, linguagem, runtime, framework e versões>`, incluindo `<banco/driver/ORM ou broker quando aplicável>`. Use o perfil fornecido, sem presumir decisões ausentes. Priorize fontes primárias versionadas. Não edite arquivos, instale ferramentas, use dados privados ou altere serviços. Retorne: fontes com URL, data e versão; recomendações e motivo; exigência oficial versus sugestão; compatibilidade e limites; controles verificáveis; alternativas; dúvidas que exigem usuário. Informe ausência de evidência e conflitos.

Cada recomendação deve gerar um registro: `pilar → pergunta → fonte/versão/data → conclusão → aplicabilidade → decisão local → verificação → lacuna`. Guarde a síntese útil, sem copiar manuais inteiros. Revalide links e recomendações quando versões mudarem.

## Síntese e dúvidas

O orquestrador resolve conflitos por contexto, versão e autoridade, não por votação dos agentes. Não conseguir decidir por evidência deve produzir uma pergunta específica, com alternativas, impacto e recomendação. Enquanto aguarda, avance em pilares independentes e não incorpore a opção pendente como regra.

Pergunte sobre produto, tolerância a risco, custo, licença, compartilhamento externo, retenção, acesso e governança. Escolhas mecânicas reversíveis podem seguir convenções existentes, registradas como decisão do agente. Sem subagentes, faça a mesma decomposição sequencial e informe a limitação; sem web, prepare lacunas e não alegue pesquisa atualizada.

Fontes conceituais: [Building effective agents](https://www.anthropic.com/research/building-effective-agents) e [Agent Skills](https://agentskills.io/specification). Os padrões precisam ser adaptados às capacidades da ferramenta escolhida.
