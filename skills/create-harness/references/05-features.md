# Pilar 5 — Produto, domínio e análise de impacto

## Construir

Registre capacidades principais, propósito, atores, regras, estados, relações e integrações. Um frontend pode organizar jornadas; um backend, capacidades de domínio; um worker, processamento e efeitos. Use o vocabulário do projeto, sem exigir que tudo seja chamado de feature.

Cada documento deve separar implementado, demonstrativo, decidido, proposto e desconhecido. Inclua mapa curto de arquivos existentes, dependências, contratos e testes relevantes. O mapa orienta a busca, não a substitui. Mantenha detalhe técnico global no pilar responsável e comportamento específico aqui.

Antes de alterar comportamento, rastreie consumidores e efeitos indiretos: autorização, dados, relatórios, notificações, eventos, UI e serviços externos. Atualize documentação responsável e índice na mesma mudança quando houver impacto. Uma correção puramente editorial pode não exigir documento de feature.

## Pesquisa e perguntas

Não é obrigatório pesquisar na web para descobrir regras particulares do produto. Use código, contratos, testes, documentação e usuário. Não invente regras comerciais a partir de padrões de mercado. Se uma capacidade depender de comportamento técnico do framework, banco ou protocolo, pesquise esse comportamento no pilar correspondente.

Pergunte sobre regras ambíguas, definição de sucesso, papéis, tratamento de falha ou inconsistência entre requisito e código. Entregue impactos confirmados, hipóteses e lacunas separadamente.

## Validação

Escolha uma capacidade piloto e peça a um agente em sessão nova para localizar regra, arquivos, dependências e verificações. Confira contra o código e um cenário observável. Mapas incompletos não podem sustentar afirmação de cobertura total.
