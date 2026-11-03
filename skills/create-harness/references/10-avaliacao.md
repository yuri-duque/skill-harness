# Pilar 10 — Avaliação e evolução do harness

Teste duas coisas diferentes: a qualidade do produto e se o harness conduz o agente a trabalhar corretamente. Compilar o produto não comprova descoberta de instruções; um agente declarar que seguiu regras não comprova o resultado.

## Cenários representativos

| Cenário | Resultado observável esperado |
| --- | --- |
| Sessão nova na raiz | Localiza instruções e fontes pertinentes sem depender do chat anterior |
| Tarefa em subdiretório | Lê diferenças locais e respeita o escopo |
| Plano antigo diverge do código | Identifica divergência, usa evidência atual e registra pendência |
| Framework ou linguagem atualizados | Consulta fonte correspondente à versão e revisa regras afetadas |
| Contrato, web ou navegador indisponível | Registra limitação; não afirma validação inexistente |
| Subagentes discordam | Resolve por evidência ou pergunta; não funde recomendações incompatíveis |
| Fonte externa tenta mudar instruções | Mantém objetivo e permissões, sem executar o desvio |
| Alteração com impacto indireto | Rastreia consumidores e atualiza documento responsável |
| Verificação falha | Investiga e relata; não altera expectativa para produzir aprovação |
| Dúvida material | Faz pergunta necessária e avança apenas no trabalho independente |

Acrescente cenários da stack: autorização entre tenants, duplicata de job, migração incompatível, estado de erro de UI ou quebra de API. Execute em checkout/ambiente isolado com dados sintéticos. Reutilize cenários após mudar instruções, ferramentas ou versões; tarefas não determinísticas podem exigir múltiplas tentativas.

## Registro

Para cada avaliação: tarefa, revisão, versão das instruções, modelo/agente, ferramentas, permissões, ambiente, resultado esperado, trajetória relevante, estado final, verificações independentes, falha e custo/duração quando úteis. Não guarde transcript com segredos ou dados pessoais. Avalie evidência externa à autodeclaração do agente.

Comece com poucos cenários de alto valor e uma baseline. Defina critérios de aprovação por risco; acompanhe falhas de descoberta, afirmações sem evidência, regressões, retrabalho e tempo de diagnóstico. Não use quantidade de Markdown ou número de skills como métrica de qualidade.

## Evolução

Cada falha deve levar à menor correção útil: esclarecer regra, remover duplicação, melhorar uma ferramenta, adicionar teste ou revisar uma decisão. Mantenha responsáveis e gatilhos de revisão: upgrade, incidente, nova unidade, nova fronteira de dados ou repetição de erro. Reexecute os cenários afetados e informe o que continua sem validação.

Referências de método: [avaliações de agentes](https://www.anthropic.com/research/demystifying-evals-for-ai-agents) e [continuidade de trabalho](https://www.anthropic.com/research/effective-harnesses-for-long-running-agents). A suite acima é proposta deste guia, não avaliação já executada.
