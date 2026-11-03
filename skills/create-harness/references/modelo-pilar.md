# Modelo para documentar um pilar no projeto de destino

Copie apenas as seções aplicáveis. Substitua os campos com evidências; remova exemplos que não pertençam à stack. Este modelo não é configuração executável.

## Objetivo e aplicabilidade

- Problema que este pilar resolve, unidades abrangidas e exclusões justificadas.
- Contexto, linguagem/runtime, framework e versões; banco/driver/ORM/broker quando relevante.

## Estado e evidências

| Item | Estado | Evidência/revisão/data | Limitação |
| --- | --- | --- | --- |
| Controle ou mecanismo | Observado / proposto / decidido / configurado / executado / verificado | Arquivo, fonte ou execução | Escopo não comprovado |

Esses estados não são uma progressão automática: uma decisão pode existir sem implementação; configuração pode existir sem execução; verificação só vale para o ambiente e cenários registrados.

## Pesquisa e decisões

| Pergunta | Fonte primária, versão e data | Recomendação e limites | Decisão local, motivo e responsável |
| --- | --- | --- | --- |
| Questão específica da stack/pilar | URL e seção | Exigência, recomendação ou hipótese | Confirmada ou pendente |

## Regras acionáveis

Para cada regra: quando se aplica, comportamento esperado, exceções justificadas, arquivo responsável e como verificar. Evite comandos imaginados e promessas sem mecanismo.

## Procedimento e ferramentas

Entradas, pré-requisitos, comandos confirmados, ambiente, permissões, passos, saída, tratamento de falha e fallback. Explique cobertura e efeitos colaterais. Nunca inclua valores de segredos.

## Validação e conclusão

Cenários, resultado esperado, comando/método, resultado observado e evidência sanitizada. Distinga validado de ainda não executado. Liste perguntas pendentes, bloqueios, responsável e próximo passo. Vincule índice, decisões e registro de trabalho sem duplicar contratos.
