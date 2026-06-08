# 00 — Manifesto e Ordem de Leitura

> Status: COMPLETO_LOTE_03  
> Maturidade: ESSENCIA_CONSOLIDADA  
> Escopo: Project Essence  
> Regra: este documento define navegação, fonte de verdade e modo seguro de uso da documentação. Ele não substitui dossiês, contracts, roadmap, context packs, playbooks ou prompts.

## 1. Finalidade

Este documento é o ponto de entrada da documentação refatorada da **ODM Engineering Platform V6/V7**.

A documentação existe para permitir desenvolvimento incremental, auditável e seguro com Devin, sem depender de memória de conversa, improviso de anexos ou inferência silenciosa sobre IBM ODM/BRE.

Ela deve funcionar como:

```text
- manifesto: define a fonte atual de verdade documental;
- mapa: indica onde encontrar cada tipo de decisão;
- contrato operacional: estabelece como Devin deve trabalhar;
- guarda-corpo: bloqueia atalhos perigosos;
- trilha de evidência: conecta requisito, decisão, artifact, teste, diagnostic e risco.
```

## 2. Fonte de verdade em caso de conflito

Em caso de conflito documental, aplicar esta ordem:

```text
1. Decisão explícita mais recente registrada no Decision Ledger ou ADR aprovado.
2. Project Essence, para regras globais e limites permanentes.
3. Architecture Contracts, para schemas, diagnostics, lifecycle e producer-consumer contracts.
4. IBM ODM Knowledge, para conhecimento ODM-aware e regras de consulta/validação.
5. Architecture Overview, para visão end-to-end, fluxos e registry.
6. DAG and Roadmap, para dependência, ordem operacional, context packs e gates.
7. Dossiês de elementos implementáveis, para responsabilidades locais.
8. Orchestrators, para coordenação de fluxos.
9. Devin Playbooks e Prompt Library, para execução de sessões.
10. Documentação legacy, apenas como origem histórica e evidência migrada.
11. Código existente, apenas como evidência de implementação atual, não como verdade arquitetural.
```

Se o conflito afetar comportamento IBM ODM, exportação, simulação, equivalência, patch, Canonical, IDs, lineage ou publicação, a sessão deve registrar `BLOCKER` ou `NEEDS_ADR` antes de avançar.

## 3. Ordem de leitura da documentação refatorada

### 3.1. Onboarding humano ou Devin

```text
1. 00_PROJECT_ESSENCE/00_MANIFESTO_E_ORDEM_DE_LEITURA.md
2. 00_PROJECT_ESSENCE/01_CONTEXTO_EXECUTIVO_E_OBJETIVOS.md
3. 00_PROJECT_ESSENCE/02_PRINCIPIOS_INVIOLAVEIS.md
4. 00_PROJECT_ESSENCE/03_MASTER_OPERATING_CONTRACT_DEVIN.md
5. 00_PROJECT_ESSENCE/04_SESSION_MODES_E_OUTPUTS.md
6. 00_PROJECT_ESSENCE/05_LIMITACOES_CRITERIOS_E_GUARDA_CORPOS.md
7. 00_PROJECT_ESSENCE/06_REQUIREMENT_TO_EVIDENCE.md
```

### 3.2. Antes de implementar qualquer camada

```text
1. Consultar 40_DAG_AND_ROADMAP/41_ROADMAP_EXECUTAVEL_DEVIN.md.
2. Identificar etapa e fase.
3. Abrir 40_DAG_AND_ROADMAP/42_CONTEXT_PACK_MATRIX.md.
4. Anexar somente documentos permitidos pela fase.
5. Abrir o dossiê principal da etapa.
6. Abrir producers e consumers diretos exigidos.
7. Aplicar o playbook da fase.
8. Exigir saída e gate definidos.
```

## 4. O que esta documentação deve impedir

A documentação deve impedir pedidos soltos como:

```text
implemente Symbol Table
refatore tudo
faça funcionar
simule o ODM
exporte para BRE
```

E deve conduzir pedidos controlados como:

```text
Execute STAGE_NNN em Investigation Mode, usando o context pack definido,
respeitando dossiê, producers, consumers, contracts, specs, playbook e gate.
```

## 5. Regras mínimas que sempre acompanham qualquer sessão

Mesmo quando não for possível anexar todo o contexto, estas regras são obrigatórias:

```text
- Canonical ODM Model é a fonte editável corrente.
- Derivados não são fonte primária de verdade.
- IBM ODM real permanece referência comportamental e de compatibilidade.
- Claims ODM-aware exigem IBM docs, ODM real, SME review ou blocker.
- Lacuna vira PENDENTE, NEEDS_REVIEW, NEEDS_ADR, NEEDS_REPO_DISCOVERY, NEEDS_IBM_DOCS ou BLOCKER.
- Devin não deve inventar contrato, comportamento ODM ou decisão arquitetural.
- Output igual não prova equivalência comportamental.
- Toda entrega relevante precisa de Requirement → Evidence.
- Uma sessão deve ter modo, escopo, arquivos permitidos e arquivos proibidos.
```

## 6. Separação entre blocos documentais

```text
Project Essence: objetivos, princípios, limites e contrato operacional permanente.
Architecture Overview: visão end-to-end, registry, fluxos e fontes de verdade.
Architecture Contracts: contracts transversais, schemas comuns, diagnostics e lifecycle.
IBM ODM Knowledge: conhecimento ODM-aware e regras de consulta/validação.
DAG and Roadmap: dependência, ordem de construção, context packs, paralelismo e gates.
Orchestrators: coordenação de fluxos, sem virar domínio.
Implementable Elements: dossiês locais das camadas/componentes.
Devin Playbooks: execução por tipo de sessão.
Prompt Library: prompts derivados, nunca fonte de verdade.
Audit and Release: checklists e auditoria final.
```

## 7. Estado de completude

Este arquivo consolida a essência de navegação e uso. Conteúdos profundos de arquitetura, contratos, dossiês, context packs, orquestradores, playbooks e prompts permanecem para seus lotes próprios.

## 8. Rastreabilidade

Origem e rastreabilidade:
- Documentação antiga: `00_INDICE_E_MODO_DE_USO.md`, `01_CONTEXTO_EXECUTIVO_E_OBJETIVOS.md`, `02_PRINCIPIOS_INVIOLAVEIS.md`, `08_TEMPLATE_OPERACIONAL_SESSAO_DEVIN.md`, `12_MASTER_OPERATING_CONTRACT.md`, `19_REQUIREMENT_TO_EVIDENCE_REPORTING.md`, `20_SESSION_CHANGE_CONTROL_AND_PR_SCOPE.md`.
- Plano completo: Lote 3 — Project Essence.
- Guia executor: Lote 3 — escopo, fora de escopo e critérios de aceite.
- Decision Ledger: DEC-001 a DEC-023, conforme aplicável.
