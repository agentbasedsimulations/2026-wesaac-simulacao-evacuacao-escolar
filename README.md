# 2026-wesaac-simulacao-evacuacao-escolar

**Análise de Evacuação de Emergência em Edificação Escolar via Simulação Baseada em Agentes**

---

## Sobre o projeto

Este repositório contém os arquivos do projeto de simulação desenvolvido no **PTV Vissim** e no módulo de dinâmica de pedestres **PTV Viswalk**, utilizados no artigo submetido ao WESAAC 2026.

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
└── Scenarios/                    # Arquivos essenciais e arquivos de projeto salvos dos cenários selecionados (S000001, S000021 e S000056)
    └── S000001 / S000021 / S000056/  # Pastas contendo os arquivos .pp de cada variação dos cenários liberados
```

---

## Sobre o trabalho

O artigo completo, com a descrição da metodologia, dos cenários simulados e dos resultados de Tempo Total de Evacuação (TTE), está disponível em `[link do artigo, quando publicado]`.

---

## Autores

- Kaique de Oliveira
- Guilherme Rode
- Fernando Santos

Departamento de Engenharia de Software — CEAVI/UDESC
