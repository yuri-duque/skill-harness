# Pilar 1 — Descoberta de contexto e stack

## Resultado esperado

Um perfil verificável do projeto que determine o restante do harness. Detecte o que existe antes de sugerir arquitetura ou ferramentas.

## Procedimento

- Leia instruções globais e locais, README, manifestos, lockfiles, configuração de runtime/build, contêineres, CI, infraestrutura e estrutura do código. Não leia arquivos de segredos para inventariar valores.
- Classifique cada unidade: frontend, backend/API, worker, scheduler, pipeline de dados, biblioteca, CLI, mobile ou combinação. Separe linguagem de framework, ORM de banco e ambiente local de produção.
- Registre versões declaradas, resolvidas e executadas separadamente, incluindo linguagem/runtime, gerenciador, framework, driver, ORM, banco e broker. Divergências são lacunas, não autorização para atualizar tudo.
- Identifique fronteiras: quem chama quem, quem autoriza, quem persiste, quem opera; dados públicos, pessoais, sensíveis e de teste; ambientes e consumidores externos.
- Identifique agente/editor, suporte a instruções e skills, ferramentas disponíveis e permissões reais. Não suponha acesso à web, navegador, banco, CI ou outros repositórios.

## Matriz inicial

| Unidade/caminho | Contexto | Linguagem/runtime/versão | Framework/versão | Dados/dependências | Evidência | Dúvida |
| --- | --- | --- | --- | --- | --- | --- |
| Preencher pela inspeção | Confirmar | Manifesto + lock + runtime | Confirmar plugins/modo | Banco, broker, APIs | Arquivo/comando/data | Responsável |

Em monorepos, mantenha um índice comum e regras locais por unidade; não imponha um único runner ou padrão a stacks diferentes. Em projeto novo, pergunte sobre o objetivo, contexto de execução, restrições e stack desejada antes de fixá-la. Documente alternativas enquanto aguarda.

## Pesquisa obrigatória

Depois da detecção, pesquise documentação oficial e suporte de versões da linguagem e framework; padrões de estrutura, execução e deploy; orientações oficiais para agentes e documentação versionada disponível. Repita por unidade relevante. A ausência de um guia oficial de harness deve ser registrada: componha recomendações a partir de documentação oficial e experimentos locais identificados como tal.

## Perguntar e validar

Pergunte se houver ambiguidade sobre stack futura, ambientes, responsabilidade de dados ou versão suportada. Uma dependência isolada não demonstra uso em produção. Valide o perfil com caminhos reais e comandos não destrutivos disponíveis; entregue pilares aplicáveis, não aplicáveis e ainda dependentes de resposta.
