# Pilar 3 — Contexto persistente, instruções e skills

## Construir

Crie uma entrada curta no formato suportado pela ferramenta: objetivo, comandos reais, invariantes, limites e roteiro de leitura por tarefa. Consulte a especificação da ferramenta para hierarquia, descoberta, tamanho, escopos e precedência. [AGENTS.md](https://agents.md/) é uma opção interoperável; não garante comportamento idêntico em todos os agentes.

Mantenha um índice de documentos duradouros; arquitetura e padrões no documento responsável; decisões com estado e motivo; pendências em um registro de trabalho; detalhe de uma área junto dela. Instruções locais devem conter diferenças reais, sem copiar a raiz. Evite dependência de caminhos pessoais, plugins privados e configurações globais não distribuídas.

Uma skill cabe quando existe processo recorrente: gatilho, entradas, passos, saídas, verificações e fallback. Antes de criá-la, confirme suporte e formato na ferramenta. Não use texto de skill como mecanismo de sandbox ou autorização. Adaptadores para outros agentes devem apontar para a mesma fonte, evitando contratos duplicados.

## Pesquisa da stack

Procure orientação oficial de agentes do framework, documentação instalada ou versionada, ferramentas de diagnóstico e geração de código, instruções gerenciadas e limitações. Não copie caminhos de um framework para outro. Defina como conferir documentação em upgrades e quando o ambiente estiver offline.

## Critérios

- Uma tarefa encontra suas fontes sem carregar a documentação inteira.
- Uma sessão nova reconhece regras locais e não depende da conversa anterior.
- Decisão confirmada está separada de mecanismo implementado e verificado.
- Documento externo é tratado como evidência não confiável, sem mudar permissões ou objetivo.
- Regras verificáveis têm um controle técnico apropriado quando disponível, não apenas uma frase imperativa.

Pergunte qual ferramenta de agente é usada se não houver evidência. Teste descoberta na raiz e em subdiretório com tarefa representativa. Documente limitações de carregamento e mantenha um caminho manual de leitura.
