# Pilar 8 — Banco de dados e ciclo de vida dos dados

Aplique quando uma unidade acessa persistência ou tem responsabilidade sobre dados. Se apenas consome uma API, documente a fronteira e o responsável pelo banco; não invente acesso direto. Este pilar não pressupõe SQL, PostgreSQL, ORM ou serviço gerenciado.

## Identificação e pesquisa obrigatória

Confirme motor, versão/edição, hospedagem, driver, ORM, pool, ferramenta de migração e modelo de tenancy. Pesquise **o motor escolhido**, além do ORM: segurança e privilégios; consistência/transações; modelagem; query planner e índices; concorrência/locks; migrações; backup e restore; manutenção e limites operacionais. Some as recomendações do provedor gerenciado e compatibilidade de versões. Se o banco ainda não foi escolhido, pergunte sobre necessidades e restrições antes de fixar padrões.

## Contrato a documentar

| Tema | Pesquisa e regra local | Evidência prevista |
| --- | --- | --- |
| Acesso | Identidades distintas de aplicação, migração e operação; privilégios mínimos, rede, TLS e rotação | Tentativas permitidas e negadas com a identidade real de runtime |
| Isolamento | Tenant, usuário, objetos e campos; controles nativos quando adequados | Leitura e escrita cruzadas negadas; caminhos de bypass verificados |
| Integridade | Constraints, transações, concorrência, duplicatas e consistência do motor | Casos de corrida, falha parcial e invariantes |
| Queries | Parametrização, consultas do ORM, volume, distribuição, paginação, N+1, pool e timeouts | Plano e latência antes/depois com dados representativos e sanitizados |
| Índices | Estratégia nativa, seletividade, ordem e custo de escrita/armazenamento | Medição do workload, sem criar índice por hábito |
| Migração | Compatibilidade entre versões da aplicação, locks, backfill, rollout e recuperação | Ensaio isolado e procedimento de recuperação, inclusive migrações irreversíveis |
| Recuperação | Backup, retenção, criptografia/chaves, RPO/RTO e restauração | Restore testado; existência de backup isoladamente não basta |
| Privacidade | Minimização, classificação, acesso, exportação, retenção, descarte e cópias | Cenários de direitos e descarte acordados com responsáveis |

Não faça benchmarks destrutivos, alterações de schema ou restaurações em produção como parte de pesquisa. Ferramentas de análise podem executar queries; confirme a semântica no motor antes de usá-las.

## Exemplo de método, não escolha padrão

Se o projeto usar PostgreSQL, consulte a documentação da versão instalada sobre [planos](https://www.postgresql.org/docs/18/using-explain.html), [índices](https://www.postgresql.org/docs/18/indexes.html) e [RLS](https://www.postgresql.org/docs/18/ddl-rowsecurity.html). `EXPLAIN ANALYZE` executa a instrução; índices acrescentam custos; RLS tem bypass por papéis privilegiados. Portanto, confira identidade de runtime e ambiente de teste. Para outro motor, substitua essas referências e os mecanismos pelos equivalentes oficiais; não traduza sintaxe e garantias automaticamente.

## Decisões do usuário

Pergunte sobre motor indefinido, tenancy, classificação, retenção, recuperação, risco de indisponibilidade e autoridade para migração. LGPD exige decisões organizacionais e jurídicas além do banco: articule com [segurança](07-seguranca.md). O agente não deve inventar prazo legal ou alegar conformidade. Saída: documento de dados com fontes versionadas, regras, comandos seguros, responsáveis, verificações e lacunas.
