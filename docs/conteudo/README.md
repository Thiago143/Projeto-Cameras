# Conteúdo em Markdown

Este diretório abriga as versões editáveis (Markdown) dos documentos anteriormente mantidos como DOCX/Pages/PDF. Fluxo recomendado:

1. **Fonte**: mantenha o arquivo original em `arquivo/` ou `base/` apenas como referência.
2. **Conversão**: gere o `.md` correspondente neste diretório (use `textutil`, `pandoc` ou scripts específicos).
3. **Revisão**: aplique formatação Markdown (títulos, listas, tabelas) para facilitar diffs.
4. **Exportação**: quando precisar distribuir, gere novamente o PDF a partir do `.md` e armazene a saída em `base/<ano>/`.

Arquivos já convertidos:
- `projeto_cameras.md` – documento-base “Escala 24x72” (DOCX original em `arquivo/2025-05/`).
- `documento_tecnico_cameras.md` – especificações técnicas gerais (DOCX original em `arquivo/2025-05/`).
- `orcamento_imaginatech_caixa.md` – orçamento da caixa de serviço (HTML original em `projeto_tecnico_poste/orcamento/caixa_servico/`).

Arquivos pendentes de conversão (criar `.md` e atualizar o inventário):
- `base/2025-06-07/sumario_executivo_cameras.pdf`
- `base/2025-11/PROJETO_DE_IMPLEMENTACAO_DE_CAMERAS_OSTENSIVAS-1.pdf`
- `arquivo/2025-05/documento_tecnico_camera.pages` (exportar para DOCX/RTF antes de converter)
- Demais PDFs em `arquivo/2025-05/` (`impacto_dissuasao_criminal_A4.pdf`, `guia_implementacao_A4.pdf`, etc.)

Sugestão: ao converter, use o padrão `docs/conteudo/<nome_documento>.md` e registre a data/fonte no cabeçalho do arquivo.
