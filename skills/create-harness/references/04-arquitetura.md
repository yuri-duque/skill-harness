# Pilar 4 — Arquitetura e padrões da stack

## Construir

Mapeie responsabilidades, entradas, fluxo de dados, dependências e limites de confiança. Documente o estado atual e escolhas propostas separadamente. Defina onde colocar código novo a partir do repositório e dos padrões do framework, sem impor Atomic Design, Clean Architecture, MVC ou organização por features universalmente.

Pesquise para a versão adotada: organização oficial, gerenciamento de dependências, tipos e validação em runtime, tratamento de erros, concorrência, cancelamento, recursos/conexões, cache, extensões e geração de código. Registre anti-padrões com consequência concreta e exemplo local. Acrescente regras específicas de idioma e ecossistema somente após a identificação da linguagem.

| Contexto | Perguntas para a pesquisa |
| --- | --- |
| Frontend | Renderização, fronteira servidor/cliente, estado, cache por identidade, hidratação, componentes e acessibilidade |
| Backend | Ciclo da requisição, validação, autorização, transações, erros e compatibilidade de contratos |
| Worker | Entrega, idempotência, retries, ordenação, concorrência, confirmação e desligamento |
| Biblioteca/CLI | API pública, compatibilidade, empacotamento, efeitos colaterais, códigos de saída e configuração |

Não transforme uma convenção sugerida pelo fornecedor em escolha do usuário. Se faltarem decisões importantes, proponha alternativas pequenas com critérios e uma jornada piloto para validá-las. Pergunte quando a escolha afeta compatibilidade pública, limites entre equipes ou requisitos não inferíveis.

## Evidências

Entregue mapa conciso de arquivos existentes, direção de dependências, decisões com motivo e verificações disponíveis. Procure usos além do mapa. Só proponha lint arquitetural quando fronteiras estiverem estáveis; confirme que a regra detecta uma violação representativa sem bloquear casos legítimos. Reavalie arquitetura após a primeira fatia funcional.
