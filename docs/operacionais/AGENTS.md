# Repository Guidelines

## Project Structure & Module Organization
All deliverables sit in the repository root and fall into three buckets: analytical reports (`Análises.pdf`, `sumario_executivo_cameras.pdf`), implementation guides (`documento_tecnico_cameras.docx`, `implementacao_cameras_4bpm_print_20250518142735.pdf`), and visual assets (`Brasão_da_Polícia_...png`, `brazao4.jpg`). Keep new drafts grouped by topic and language and reuse the existing pattern `topic_context_language.format` so versions line up alphabetically. Always commit editable sources beside their exported PDFs to make downstream edits traceable.

## Build, Test, and Development Commands
“Build” here means exporting or validating documents:
- `ls -1 *.pdf *.docx` — quick completeness check before a commit.
- `textutil -convert pdf documento_tecnico_cameras.docx` — generate a peer-review PDF directly on macOS.
- `open impacto_dissuasao_criminal_A4.pdf` (or `qlmanage -p <file>`) — spot-check layout and typography.
Document any bespoke conversion script under `scripts/` so others can rerun it verbatim.

## Coding Style & Naming Conventions
Use UTF-8 filenames and retain Portuguese accents already in use. Apply concise suffixes for derivatives (`_A4`, `_print`, `_revN`) and prefer underscores over spaces when exporting for distribution. Inside the docs, keep headings in title case, cite sources inline, and standardize measurements to metric units. Markdown notes should wrap at ~80 characters and use fenced blocks for command snippets.

## Testing Guidelines
Validate each asset in both its authoring app and the exported PDF to confirm charts, seals, and tables survived the conversion. Run Preview’s accessibility inspector on PDFs destined for circulation and log pass/fail items in the document footer (e.g., “Verificado 2025‑05‑18: gráficos, ortografia”). Highlight any data disputes versus `Análises.pdf` through tracked changes or comments to maintain auditability.

## Commit & Pull Request Guidelines
When using Git, follow an imperative, topic-first format such as `docs: atualiza sumario executivo` or `assets: substitui brasao em alta resolucao`, and mention the source + export pair touched. Pull requests should call out goal, affected files, commands used to regenerate PDFs, and screenshots of any visual diffs. Link to the relevant briefing or ticket so reviewers understand why a document changed.

## Security & Confidentiality
Treat every file as sensitive: avoid committing raw footage or personal identifiers and store heavy media in encrypted systems outside Git. Strip EXIF metadata from PNG/JPG assets (`sips --stripImageMetadata brazao4.jpg`) before pushing to keep device details private.

## DevOps Agent
- **Contexto:** ver `docs/operacionais/DEVOPS_AGENT.md`.
- **Função:** garantir versionamento e automações (CI/CD, exports, deploys).
- **Ação:** antes de pedir push, confirme inventário, changelog e credenciais GitHub. O agente solicitará seus dados quando precisar sincronizar com o repositório remoto.
