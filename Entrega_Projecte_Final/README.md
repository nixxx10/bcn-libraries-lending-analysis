# Performance de la xarxa de Biblioteques de Barcelona

**Projecte Final · Bootcamp d'Analítica de Dades** — Nizar El Ouarma

## Tema
Anàlisi de l'ús i el rendiment del préstec a la xarxa de biblioteques públiques de
Barcelona (2011–2024) i la seva relació amb el territori, la renda i la demografia.

## Troballa principal
El factor que millor explica el préstec per habitant és la **superfície de biblioteca
per habitant (m²)** —de manera robusta (r = +0,88; IC95% [+0,56, +0,94])—, per damunt
de la renda, la demografia, el fons documental i el nombre de biblioteques, que no
mostren cap relació fiable. Com que el catàleg és compartit per tota la xarxa (oferta
"líquida"), el que roman ancorat al territori és l'espai físic.

## Estructura de la carpeta

```
Entrega_Projecte_Final/
├── Informe.pdf                       Informe final (article científic, 4 pàgines)
├── Presentacio_Biblioteques_BCN.pptx Presentació de la defensa
├── README.md                         Aquest document
├── codi/                             Notebooks de Python
│   ├── F01_extraccion_datos.ipynb       Fase 1 · extracció (Open Data BCN)
│   ├── F02_limpieza_transformacion.ipynb Fase 2 · neteja i taula mestra
│   └── F03_visualizaciones.ipynb        Fase 3 · anàlisi i figures
├── dades/
│   ├── interim/                      Dades netejades per districte-any (5 CSV)
│   └── processed/
│       └── maestra_distrito_anyo.csv Taula mestra final (150 × 16)
└── figures/                          Figures generades amb Python (12 PNG)
```

> Les dades **crudes (`raw/`)** no s'inclouen al repositori per la seva mida; són
> descarregables directament d'**Open Data BCN** (vegeu *Fonts de dades*). Les dades
> netejades (`interim/`) i la taula mestra (`processed/`) sí que hi són i basten per
> reproduir tota l'anàlisi.

## Eines i mètodes
Python (pandas, numpy, matplotlib) per a l'ETL i l'anàlisi. Correlacions de Pearson i
Spearman amb intervals de confiança per *bootstrap* de conglomerats; renda deflactada a
euros de 2019 (IPC).

## Fonts de dades
Open Data BCN (Ajuntament de Barcelona): préstecs i equipaments de la Xarxa de
Biblioteques, renda familiar disponible i padró municipal.
