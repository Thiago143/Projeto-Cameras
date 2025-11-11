# Manual de Uso do Git/GitHub – Projeto Câmeras

**Última atualização:** 2025-11-11  
**Versão:** 0.1

---

## 1. Objetivo

Padronizar como o repositório “Projeto Câmeras Ostensivas” é versionado localmente e sincronizado com o GitHub. Todo artefato (documentos, mapas, scripts) deve passar pelo mesmo fluxo para manter rastreabilidade e permitir expansão futura.

Principais metas:
- Histórico auditável (`git log` + `CHANGELOG.md`);
- Sincronização privada no GitHub (dados sensíveis);
- Base para automações do **DevOps Agent** (CI/CD, exports, deploys).

---

## 2. Estrutura Esperada

```
Projeto-Cameras/
├── README.md
├── CHANGELOG.md
├── GITHUB_MANUAL.md
├── docs/
│   └── operacionais/
│       ├── AGENTS.md
│       └── DEVOPS_AGENT.md
├── arquivo/
├── base/
├── projeto_tecnico_poste/
│   ├── entrada_requisitos/
│   ├── referencias_normativas/
│   ├── desenhos/
│   ├── memorial_descritivo/
│   ├── imagens_postes/
│   ├── mapas/
│   └── orcamento/
├── inventario_arquivos.csv
└── .gitignore
```

Manter o inventário atualizado é requisito antes de cada commit.

Arquivos a ignorar (já listados em `.gitignore`, ampliar se necessário):
```
*.tmp
*.swp
*~
.DS_Store
node_modules/
venv/
__pycache__/
*.bak
backup/
```

---

## 3. Fluxo Diário

1. **Atualizar inventário** (`inventario_arquivos.csv`) com status correto dos arquivos.
2. **Revisar diretórios** afetados e garantir que READMEs explicam as mudanças.
3. **Executar checagem local**:
   ```bash
   git status -sb
   ```
4. **Atualizar CHANGELOG** (seção “Unreleased” ou data do dia).
5. **Commits atômicos**:
   ```bash
   git add <arquivos>
   git commit -m "docs: organiza mapas AISPs"
   ```
6. **Sincronizar** (assim que o repositório GitHub estiver configurado):
   ```bash
   git push origin main
   ```

---

## 4. Configuração Inicial

1. **Criar repositório no GitHub**  
   - Nome sugerido: `projeto-cameras-operacionais`  
   - Visibilidade: **Private**  
   - Sem README/licença automáticos.

2. **Conectar repositório local** (executar uma vez):
   ```bash
   cd "/Users/thiago/Projetos/Projeto Câmeras"
   git init
   git branch -M main
   git remote add origin git@github.com:<usuario>/projeto-cameras-operacionais.git
   git remote -v
   ```

3. **Configurar SSH** (se ainda não existir):
   ```bash
   ssh-keygen -t ed25519 -C "seu.email@exemplo.com"
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_ed25519
   pbcopy < ~/.ssh/id_ed25519.pub  # colar no GitHub > Settings > SSH keys
   ```

4. **Primeiro push**:
   ```bash
   git add .
   git commit -m "chore: primeira versão estruturada"
   git push -u origin main
   ```

---

## 5. Papel do DevOps Agent

O DevOps Agent automatiza:
- Verificações (`git status`, `inventario_arquivos.csv`, `README/CHANGELOG`);
- Criação de commits e atualização do `CHANGELOG.md`;
- Execução de pipelines (ex.: exportar DOCX→PDF, gerar GeoJSON dos shapefiles);
- Deploys futuros (publicação de relatórios ou dashboards).

Sempre que o agente precisar de acesso ao GitHub, forneça:
1. URL do repositório privado;
2. Credenciais/Token ou confirme que a chave SSH está configurada;
3. Restrições (branch protegida, revisões necessárias, etc.).

---

## 6. Boas Práticas
- Commits em português, modo imperativo: `docs: atualiza inventario 2025-11`.
- Atualize o `CHANGELOG.md` antes de encerrar cada sessão.
- Não versionar mídias originais sensíveis (vídeos, fotos com metadados).
- Para arquivos grandes (>25 MB), considerar LFS ou armazenar externamente.
- Validar que `projeto_tecnico_poste/mapas/raw/` não contém segredos (apenas dados públicos do ISP).

---

## 7. Checklist Rápido (antes de pedir push)

1. `git status` limpo ou apenas mudanças intencionais.
2. `inventario_arquivos.csv` atualizado.
3. `CHANGELOG.md` com entrada da sessão.
4. README/AGENTS refletindo novas estruturas.
5. Sem arquivos temporários (rodar `find . -name "*.DS_Store" -delete` se necessário).

Cumprindo estes passos, o repositório estará pronto para ser sincronizado com o GitHub e utilizado pelo DevOps Agent para automatizar o ciclo de vida do projeto.
