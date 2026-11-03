# Pilar 9 — Módulos por contexto e operação

Selecione módulos pelo perfil real. Pesquise cada tema nos manuais da linguagem, framework, runtime e fornecedores utilizados. Os exemplos são perguntas de pesquisa, não uma lista de ferramentas para instalar.

## Frontend, mobile e interfaces

Documente estados, navegação, componentes compartilhados e consumidores; acessibilidade, responsividade ou adaptação ao dispositivo; movimento, desempenho, conteúdo público e cache. Pesquise padrões de renderização, formulários, estado, testes e acessibilidade do framework. Defina larguras, dispositivos e estados por produto e audiência; não reutilize breakpoints do repositório de origem. Pergunte por suporte de plataformas e referências visuais. Evidência: jornadas em dispositivos/viewports relevantes, foco/teclado quando aplicáveis, estados e limites de cobertura.

## Backend e APIs

Documente entradas, autenticação/autorização, validação, erros, limites, paginação, idempotência quando necessária e evolução de contrato. Pesquise padrões oficiais do framework e protocolo, middleware, serialização, cancelamento e segurança. Confira consumidores reais e versões candidatas; documentação gerada não demonstra comportamento. Pergunte sobre compatibilidade pública, proprietários e ambientes de validação. Evidência: cenários de sucesso, erro, acesso negado e incompatibilidade em ambiente isolado.

## Workers, agendadores e eventos

Documente semântica de entrega do broker, confirmação, retries/backoff, duplicatas, idempotência, ordenação, concorrência, DLQ/reprocessamento, cancelamento e desligamento. Pesquise broker e biblioteca nas versões reais: não suponha exactly-once ou ordem global. Inclua fuso e sobreposição de jobs agendados. Pergunte sobre perda tolerada, efeitos duplicados e quem reprocessa falhas. Evidência: falha entre efeito e confirmação, redelivery, indisponibilidade e recuperação.

## Bibliotecas, CLI e pipelines

Para biblioteca, pesquise empacotamento, API pública, compatibilidade e matriz de runtimes. Para CLI, entrada não interativa, códigos de saída, stdout/stderr, configuração e sinais. Para pipelines, linhagem, qualidade de dados, esquema, reexecução, checkpoints e descarte. Pergunte quem consome e quais compatibilidades são compromisso. Valide no modo de distribuição/execução realista.

## Operação em qualquer contexto

Documente instalação reproduzível, ambientes, configuração, deploy, promoção, smoke check, rollback/recuperação, observabilidade e incidentes. Pesquise recursos e restrições da plataforma efetiva, modelo de processos, health checks, escalabilidade e limites. Não escolha cloud ou monitoramento por conveniência do agente.

Defina sinais de falha, logs/traces/métricas minimizados, alertas, responsáveis e runbooks. Pergunte por SLO, orçamento, RPO/RTO e acesso quando indefinidos. Saída: procedimentos executáveis com pré-requisitos e limites. Deployment descrito continua proposto até existir configuração e evidência; teste operacional requer ambiente e autorização adequados.
