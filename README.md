# 2026-wesaac-simulacao-evacuacao-escolar

**Análise de Evacuação de Emergência em Edificação Escolar via Simulação Baseada em Agentes**

[![DOI](https://img.shields.io/badge/DOI-10.5753%2Fwesaac.2026.31819-blue)](https://doi.org/10.5753/wesaac.2026.31819)
[![WESAAC 2026](https://img.shields.io/badge/WESAAC-2026-green)](https://sol.sbc.org.br/index.php/wesaac/article/view/45237)

---

## Publicação

Este repositório acompanha o artigo publicado no **WESAAC 2026**:

> **Emergency Evacuation Analysis in a School Building via Agent-Based Simulations**
> Kaique de Oliveira, Guilherme Rode, Fernando Santos — UDESC
>
> 📄 Artigo: https://sol.sbc.org.br/index.php/wesaac/article/view/45237
> 🔗 DOI: [10.5753/wesaac.2026.31819](https://doi.org/10.5753/wesaac.2026.31819)

O artigo traz a descrição completa da metodologia, dos cenários simulados e dos resultados de Tempo Total de Evacuação (TTE).

---

## Sobre o projeto

Este repositório contém os arquivos do projeto de simulação desenvolvido no **PTV Vissim** e no módulo de dinâmica de pedestres **PTV Viswalk**, utilizados no artigo.

O trabalho modela a evacuação de emergência da ECIM EEB Walmor Ribeiro (Ibirama, SC), avaliando:

- **6** cenários de disponibilidade de saídas
- **3** turnos de ocupação
- **4** regimes de velocidade dos pedestres

com base no **Social Force Model (SFM)**.

---

## Requisitos

- [PTV Vissim](https://www.ptvgroup.com/pt/produtos/ptv-vissim) com o módulo **PTV Viswalk** habilitado
- Versão utilizada no projeto: **Academic 2026 SP06**

---

## Como executar

1. Abra o arquivo do projeto (`.inpx`) no PTV Vissim.

2. Para rodar uma simulação única, em tempo real e na velocidade normal, acesse:

   `Simulation > Parameters`

   e configure os campos:

   | Campo | Valor |
   |---|---|
   | Number of runs | `1` |
   | Simulation Speed — Factor | `1,0` |

3. Salve as alterações e execute a simulação (**Simulate**).

> **⚠️ Sobre o mapa de calor (heatmap)**
> O projeto inclui uma configuração de mapa de calor para densidade de pedestres que **não funcionou corretamente** nesta versão. Se a simulação for exibida com o mapa colorido e você quiser desativar isso, acesse:
>
> `Evaluation > Configuration`
>
> e desmarque a flag **`Pedestrian grid cells`**.
>
> Com essa flag desmarcada, a simulação roda em tempo real e é exibida sem a coloração do mapa de calor.

---

## Estrutura do repositório

```
WalmorRibeiro-Main/
├── Modelagem - ECIM EEB Walmor Ribeiro.inpx      # Projeto principal — abrir este arquivo no Vissim
├── Modelagem - ECIM EEB Walmor Ribeiro.layx      # Layout de visualização
├── Modelagem - ECIM EEB Walmor Ribeiro.inp0      # Dados da rede/simulação
├── Modelagem - ECIM EEB Walmor Ribeiro.vissimpdb # Banco de dados do projeto
│
├── Componentes externos/         # Modelos 3D (.skp) e mídias usados na cena (mobiliário, bebedouros, hidrantes, UDESC.jpg, etc.)
│
├── Backups/                      # Backups do projeto e arquivos de salvamento (.trax)
│
├── Modifications/                # Histórico de modificações do projeto (M000001–M000079.trax)
│
└── Scenarios/                    # Arquivos essenciais e arquivos de projeto salvos dos cenários
    └── S000001 ao S000072  # Pastas contendo os arquivos .pp de cada variação dos cenários
```

---

## Como citar

Se este trabalho ou os arquivos de simulação forem úteis para você, por favor cite o artigo:

**Texto:**

OLIVEIRA, Kaique de; RODE, Guilherme; SANTOS, Fernando. Emergency Evacuation Analysis in a School Building via Agent-Based Simulations. In: WORKSHOP-ESCOLA DE SISTEMAS DE AGENTES, SEUS AMBIENTES E APLICAÇÕES (WESAAC), 2026. Porto Alegre: Sociedade Brasileira de Computação, 2026. DOI: https://doi.org/10.5753/wesaac.2026.31819.

**BibTeX:**

```bibtex
@inproceedings{oliveira2026evacuation,
  author    = {Kaique de Oliveira and Guilherme Rode and Fernando Santos},
  title     = {Emergency Evacuation Analysis in a School Building via Agent-Based Simulations},
  booktitle = {Anais do Workshop-Escola de Sistemas de Agentes, seus Ambientes e Aplicações (WESAAC)},
  year      = {2026},
  publisher = {Sociedade Brasileira de Computação},
  address   = {Porto Alegre, RS, Brasil},
  doi       = {10.5753/wesaac.2026.31819},
  url       = {https://sol.sbc.org.br/index.php/wesaac/article/view/45237}
}
```

---

## Autores

- Kaique de Oliveira
- Guilherme Rode
- Fernando Santos

Departamento de Engenharia de Software — CEAVI/UDESC
