# Pilar 6 — Qualidade, testes e ciclos de feedback

## Construir

Inventarie comandos realmente existentes, pré-requisitos, diretórios cobertos e resultados. Separe compilação, análise estática, formatação, testes e revisão. Uma ferramenta instalada não demonstra uso; um script de lint pode ignorar grande parte do projeto.

Pesquise ferramentas oficiais e recomendadas para linguagem/framework/versão, suporte a concorrência, testes de componentes ou módulos, integração, ambiente realista e CI. Selecione por comportamento e risco; não imponha runner, porcentagem de cobertura ou pirâmide universal. Registre isolamento, dados sintéticos, limpeza, determinismo e diagnóstico.

| Fronteira | Evidência desejada conforme aplicável |
| --- | --- |
| Lógica | Regras e casos limites com resultado observável |
| Integração | Banco, broker ou provedor isolado com versões representativas |
| Contrato | Consumidor e versão candidata do provedor; erros e semântica além do schema |
| UI | Estados, interação, acessibilidade, responsividade e visual conforme risco |
| Worker | Duplicatas, falhas, redelivery, cancelamento e recuperação |

Mock comprova comportamento nas condições simuladas, não compatibilidade real. Build não substitui teste funcional. Não ajuste expectativas para ocultar regressões; investigue o requisito e a causa.

## Automação

Introduza gates gradualmente: instalação reproduzível, checks existentes, testes críticos e demais controles conforme maturidade. Defina permissões, ambiente, duração, retenção sanitizada, falha de infraestrutura, exceções com responsável/prazo e critérios de bloqueio. Hooks locais são conveniência; confirme suporte e execução e não os apresente como CI.

Pergunte sobre gates, risco aceito e ambientes quando não houver decisão. Execute verificações proporcionais e relate comando, revisão, escopo, resultado e bloqueios. A disponibilidade de navegador ou serviço define evidência possível, não autorização para declarar sucesso sem executar.
