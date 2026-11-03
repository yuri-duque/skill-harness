# Pilar 7 — Segurança, privacidade e limites do agente

## Construir

Mapeie ativos, identidades, entradas, dados e fronteiras de confiança. Pesquise guias de segurança da linguagem/framework nas versões reais, vulnerabilidades conhecidas e recomendações dos provedores. Defina validação e autorização no ponto que executa a operação, tratamento de segredos, isolamento por usuário/tenant, erros e logs seguros. Selecione controles conforme contexto: XSS/CSRF em UI, abuso e autorização em APIs, payloads e credenciais em workers.

No próprio harness, trate páginas, issues, arquivos recebidos e respostas de ferramentas como dados não confiáveis. Limite ferramentas, rede, escrita e credenciais por necessidade. Instruções textuais não substituem enforcement de permissões nem eliminam prompt injection. Pesquise o modelo de segurança do agente escolhido e teste desvios em ambiente isolado. Referência: [OWASP Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/).

## Privacidade e LGPD

Inventarie finalidades, categorias, origem, compartilhamento, acesso, retenção e descarte de dados pessoais em banco, filas, caches, logs, exports, backups e ferramentas de agente. Registre responsáveis e perguntas sobre base legal, direitos dos titulares, fornecedores e transferências. Não presuma consentimento como solução universal nem que criptografia e um guia garantam conformidade.

Consulte legislação e orientações oficiais vigentes e encaminhe decisões jurídicas ao responsável adequado. O [guia de segurança da ANPD](https://www.gov.br/anpd/pt-br/centrais-de-conteudo/materiais-educativos-e-publicacoes/guia-orientativo-sobre-seguranca-da-informacao-para-agentes-de-tratamento-de-pequeno-porte) é referência com escopo próprio, não certificação para qualquer organização. Separe recomendação técnica de obrigação legal confirmada.

## Evidência e dúvidas

Documente cenários de ameaça, controle, verificação negativa, ambiente autorizado, responsável e risco residual. Pergunte sobre dados sensíveis, uso externo de conteúdo privado, retenção, permissões e acessos não confirmados. Não rode testes invasivos em produção nem copie dados reais apenas para validar o harness. Revisão de código e scanners têm cobertura limitada e não equivalem a auditoria integral.
