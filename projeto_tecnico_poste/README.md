# Projeto Técnico do Poste

Este módulo concentra todos os insumos necessários para detalhar a infraestrutura física dos postes (cabeamento, fixações, alimentação e rede). A pasta está pronta para receber novos documentos assim que você disponibilizar os referenciais técnicos e as imagens planejadas.

Estrutura sugerida:
- `entrada_requisitos/`: briefings operacionais, checklists de órgãos reguladores, dados de campo.
- `referencias_normativas/`: normas ABNT, resoluções municipais, padrões de concessionárias.
- `desenhos/`: plantas, cortes, modelos CAD/BIM e renders.
- `memorial_descritivo/`: textos explicando solução, materiais e critérios de dimensionamento.
- `orcamento/`: planilhas de quantitativos, cotações e memórias de cálculo financeiro (já contém `lista_materiais.csv` derivado da planilha do Google Sheets e a exportação original em `raw/`).
- `imagens_postes/`: fotos e croquis coletados em campo (serão adicionados quando você enviar).
- `mapas/`: shapes/tabelas do ISP com divisões de batalhões da PMERJ (já inclui `Relacao_RISPxAISPxCISP.csv` em UTF-8 e um resumo `aisp_resumo.csv`; mantenha os arquivos originais em `mapas/raw/`).

Processo recomendado:
1. Salve todo documento-fonte no respectivo subdiretório e gere exportações (PDF/DWG) lado a lado.
2. Atualize `inventario_arquivos.csv` com cada novo item para manter rastreabilidade.
3. Ao receber as imagens dos postes ou mapas ISP/PMERJ, nomeie-os com padrões consistentes (`bpmXX_area_tipo.ext`) e registre detalhes (fonte, data de coleta) nos READMEs correspondentes para manter rastreabilidade.
