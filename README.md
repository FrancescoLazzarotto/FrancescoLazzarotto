<div align="center">

# Francesco Lazzarotto

**AI Research Fellow — University of Turin, Dept. of Computer Science**

Knowledge Graphs&nbsp;&nbsp;·&nbsp;&nbsp;Retrieval-Augmented Generation&nbsp;&nbsp;·&nbsp;&nbsp;LLM Evaluation

<a href="https://www.linkedin.com/in/francesco-lazzarotto-a09aa51ba/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:francesco.lazzarotto@edu.unito.it"><img alt="Academic email" src="https://img.shields.io/badge/Academic%20Mail-1F6FEB?style=for-the-badge&logo=maildotru&logoColor=white"/></a>
<a href="https://stackoverflow.com/users/14979870/francesco-lazzarotto"><img alt="Stack Overflow" src="https://img.shields.io/badge/Stack%20Overflow-F58025?style=for-the-badge&logo=stackoverflow&logoColor=white"/></a>

</div>

<br/>

I work on getting language models to answer from **structured, verifiable knowledge** instead of parametric memory — grounding retrieval in knowledge graphs and domain ontologies, then measuring whether it actually helped.

Right now that means **GraphRAG applied to the circular economy for food**, part of the GaIA project at the University of Turin, in collaboration with the University of Gastronomic Sciences of Pollenzo.

<br/>

## Currently

**Graph-grounded retrieval over food-security knowledge** — a Neo4j knowledge graph built from FAO and EU corpora, with an ongoing quality-repair cycle (structural metrics → Cypher/Python fixes → re-evaluation).

**Comparing knowledge-provision strategies** — plain-text baseline vs. locally materialized GraphRAG vs. vocabulary-anchored retrieval over AGROVOC, ChEBI and CEON. The question is not "does RAG work" but *which* form of structure pays for itself.

**LLM-as-judge evaluation harness** — a custom framework running Qwen3-30B-A3B and Qwen2.5-72B-Instruct on a multi-GPU vLLM cluster, used to score groundedness and answer quality at scale.

<br/>

## What the pipeline looks like

```mermaid
flowchart LR
    Q([Question]) --> R{Hybrid retrieval}
    R -->|dense + sparse| D[(Text chunks)]
    R -->|Cypher| G[(Neo4j<br/>knowledge graph)]
    O[AGROVOC · ChEBI · CEON] -.->|anchors| G
    D --> C[Grounded context]
    G --> C
    C --> L[LLM]
    L --> A([Verifiable answer])
    A --> J{{LLM-as-judge}}
```

Every claim in the answer should trace back to a node, an edge, or a source passage. That constraint is the whole point.

<br/>

## Publications

**Balancing Thematic Relevance and Cognitive Load in Adaptive Text Recommendation for Learners with SLDs**
<!-- verifica l'ordine degli autori prima di pubblicare -->
G. Coucourde, F. Lazzarotto, F. Cena — **ACM UMAP 2026** · `accepted`

**Comparing Knowledge Provision Strategies for RAG in the Circular Food Domain**
<!-- sostituisci con il titolo esatto del paper ISWC -->
F. Lazzarotto et al. — **ISWC 2026 Workshop** · `under review`

**Ontology-Grounded Verifiable Question Answering in the Circular Food Domain**
M.Sc. thesis, University of Turin · [`read`](LINK-TESI)

<br/>

## Selected work

| | |
|---|---|
| **[graphrag-ceff](LINK-REPO)** | End-to-end GraphRAG system for the circular food domain — retrieval strategies, KG construction, benchmarks, live demo. |
| **[kg-quality](LINK-REPO)** | Metrics and repair routines for knowledge-graph quality: structural diagnostics, Cypher-based fixes, before/after evaluation. |
| **[rag-eval](LINK-REPO)** | LLM-as-judge evaluation harness — rubric prompting, batched vLLM inference, agreement analysis. |

<br/>

## Stack

**Core** &nbsp;
<img alt="Python" src="https://img.shields.io/badge/Python-1F2328?style=flat-square&logo=python&logoColor=3776AB"/>
<img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-1F2328?style=flat-square&logo=pytorch&logoColor=EE4C2C"/>
<img alt="Hugging Face" src="https://img.shields.io/badge/Hugging%20Face-1F2328?style=flat-square&logo=huggingface&logoColor=FFD21E"/>
<img alt="LangChain" src="https://img.shields.io/badge/LangChain-1F2328?style=flat-square&logo=langchain&logoColor=1C3C3C"/>
<img alt="vLLM" src="https://img.shields.io/badge/vLLM-1F2328?style=flat-square&logo=lightning&logoColor=FDB515"/>

**Knowledge & data** &nbsp;
<img alt="Neo4j" src="https://img.shields.io/badge/Neo4j-1F2328?style=flat-square&logo=neo4j&logoColor=4581C3"/>
<img alt="RDF / SPARQL" src="https://img.shields.io/badge/RDF%20%2F%20SPARQL-1F2328?style=flat-square&logo=w3c&logoColor=005A9C"/>
<img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-1F2328?style=flat-square&logo=postgresql&logoColor=4169E1"/>
<img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-1F2328?style=flat-square&logo=scikitlearn&logoColor=F7931E"/>

<details>
<summary>Also worked with</summary>

<br/>

Keras · MySQL · PHP · Arduino · HTML/CSS/JS · Bootstrap · Figma — from earlier front-end and teaching work.

</details>

<br/>

## Elsewhere

**Personal** — [francescolazzarotto01@gmail.com](mailto:francescolazzarotto01@gmail.com) &nbsp;·&nbsp; **Academic** — [francesco.lazzarotto@edu.unito.it](mailto:francesco.lazzarotto@edu.unito.it)

<br/>

<div align="center">
<sub>Off-hours: astronomy, robotics, and the mountains around Biella.</sub>
</div>

<!--
════════════════════════════════════════════════════════════════
BLOCCHI OPZIONALI — scommenta se ti servono
════════════════════════════════════════════════════════════════

1) CARD DELLE STATISTICHE GITHUB
   Sostituisci USERNAME. Sfondo trasparente: si adatta a tema chiaro e scuro.
   Nota: l'istanza pubblica va spesso in rate limit; se l'immagine si rompe
   spesso, fai il self-host su Vercel (fork di anuraghazra/github-readme-stats).

<div align="center">
  <img alt="GitHub stats" height="150" src="https://github-readme-stats.vercel.app/api?username=USERNAME&show_icons=true&hide_border=true&bg_color=00000000&title_color=1F6FEB&text_color=768390&icon_color=1F6FEB&hide=issues&hide_title=true"/>
</div>

2) ORCID / GOOGLE SCHOLAR (consigliati per un profilo accademico)

<a href="https://orcid.org/XXXX-XXXX-XXXX-XXXX"><img alt="ORCID" src="https://img.shields.io/badge/ORCID-A6CE39?style=for-the-badge&logo=orcid&logoColor=white"/></a>
<a href="https://scholar.google.com/citations?user=XXXX"><img alt="Google Scholar" src="https://img.shields.io/badge/Google%20Scholar-4285F4?style=for-the-badge&logo=googlescholar&logoColor=white"/></a>

════════════════════════════════════════════════════════════════
-->
