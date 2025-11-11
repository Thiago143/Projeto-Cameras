# Mapas PMERJ / ISP

Este diretório guardará os arquivos geográficos usados para planejar a instalação (KML, GeoJSON, shapefiles) com as divisões de batalhões/regiões da PMERJ, além de mapas-base dos bairros do Rio.

Arquivos atuais:
- `raw/Relacao_RISPxAISPxCISP_iso.csv`: export original do site do ISP (mantido em ISO-8859-1 para referência).
- `Relacao_RISPxAISPxCISP.csv`: versão UTF-8 pronta para ser ingerida por QGIS/Excel.
- `aisp_resumo.csv`: contagem de CISPs por AISP + municípios associados para consulta rápida.
- `pontos_instalacao.csv`: template para relacionar coordenadas dos pontos planejados/instalados (sincronize com `entrada_requisitos/locais_instalacao.csv`).
- `raw/shp_limite_aisp_072024/*`: shapefile completo das AISPs (arquivos `.shp`, `.dbf`, `.prj`, etc.) extraído do pacote `AISPshp_2025.rar`. Copie esta pasta para o software SIG de preferência e mantenha um `metadata.md` aqui com o histórico de download.

Como preparar os dados:
1. Baixe os shapes oficiais no portal do ISP ou outra fonte confiável fora deste ambiente e copie-os para cá mantendo a estrutura original (`mapas/pmrj_areas/`, `mapas/bairros_rj/`, etc.).
2. Inclua um arquivo `metadata.md` ou `README` em cada subpasta registrando fonte, data de download e projeção.
3. Quando gerar mapas temáticos (PDF/SVG) para apresentações, salve-os em `mapas/exports/` com a mesma nomenclatura usada nos documentos (`bpmXX_localidade_vYYMMDD.pdf`).
