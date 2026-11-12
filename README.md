# QualiMadeira

**Wood quality assessment based on ABNT and ASTM standards — a free, installation-free web application.**
*Avaliação da qualidade da madeira segundo normas ABNT e ASTM — aplicativo web gratuito, sem instalação.*

[English](#english) · [Português](#português)

---

## English

QualiMadeira computes physical, chemical and mechanical wood properties from raw laboratory readings, following Brazilian (ABNT) and American (ASTM) standards. It returns per-specimen results, statistics by species, characteristic values, the strength class of ABNT NBR 7190-1:2022 and an indicative quality overview. Automatic consistency checks flag physically implausible values.

**Live app:** https://omadsongalvao.github.io/qualimadeira/

### Features

| Tab | Outputs |
| --- | --- |
| Physical | Moisture content; basic, apparent (12%) and oven-dry density; radial, tangential, longitudinal and volumetric shrinkage; anisotropy coefficient |
| Chemical | Total extractives; Klason lignin (extractive-free and whole-wood basis); ash; holocellulose by difference |
| Mechanical | MOR, MOE, fc0, Ec0, fv0, Janka hardness; correction to 12% moisture (ABNT) |
| Quality | Strength class D20–D60, density class, dimensional stability class, indicative end uses |
| Standards & formulas | Every formula with its standard and classification tables |

- Two entry modes: one specimen at a time, or import of a standardized Excel/CSV workbook.
- Statistics by species: n, mean, SD, CV, min, max; characteristic values by the NBR 7190 estimator.
- Export of results, statistics and inputs to Excel.
- Interface in Portuguese (Brazil) and English (US); Excel columns accepted in either language.
- Runs entirely in the browser: no server, no account, no data leaves the device.

### Quick start

1. Open the live app, or download this repository and open `index.html` in any modern browser.
2. Choose the language and the reference standard (ABNT or ASTM).
3. Enter data specimen by specimen, or download the Excel template and import your filled sheet.
4. Tap **Load example** to try the app with fictitious data.

### Spreadsheet format

Templates are in the repository root (`QualiMadeira_template.xlsx`, `QualiMadeira_modelo.xlsx`): one sheet per property group (`Physical`, `Chemical`, `Mechanical`), an instructions sheet and a data dictionary. Row 1 holds the column names; one row per specimen; `Species` is required. Units: g, cm³, mm, N, %. A filled example with fictitious species is `QualiMadeira_example_fictitious.xlsx`.

### Repository structure

```
index.html                               the whole application (HTML, CSS, JavaScript)
QualiMadeira_template.xlsx               empty Excel template (English)
QualiMadeira_modelo.xlsx                 empty Excel template (Portuguese)
QualiMadeira_example_fictitious.xlsx     example workbook with fictitious data
```

The only external dependency, SheetJS Community Edition 0.18.5 (Apache-2.0), is loaded from cdnjs.

### Validation

Formulas were checked against hand calculations and against a real dataset of three tropical hardwoods (419 specimen records, species anonymized), reproducing reference values within 0.2%. Details are in the accompanying article.

### Limitations

Quality classes and end-use suggestions are screening aids, not a technical report. Strength classes apply to clear specimens of native hardwoods. ASTM results are not adjusted for moisture.

### How to cite

See [`CITATION.cff`](CITATION.cff). Article: *submitted to the Journal of the Indian Academy of Wood Science*.

### License

MIT — see [`LICENSE`](LICENSE). SheetJS is distributed under Apache-2.0.

---

## Português

O QualiMadeira calcula propriedades físicas, químicas e mecânicas da madeira a partir das leituras brutas de laboratório, segundo normas ABNT e ASTM. Ele fornece resultados por corpo de prova, estatística por espécie, valores característicos, a classe de resistência da ABNT NBR 7190-1:2022 e uma visão prévia da qualidade. Alertas automáticos sinalizam valores fisicamente implausíveis.

**App online:** https://omadsongalvao.github.io/qualimadeira/

### Como usar

1. Abra o app online ou baixe este repositório e abra `index.html` em qualquer navegador moderno.
2. Escolha o idioma e a norma de referência (ABNT ou ASTM).
3. Insira os dados corpo de prova a corpo de prova, ou baixe o modelo Excel e importe a planilha preenchida.
4. Toque em **Carregar exemplo** para testar com dados fictícios.

Os modelos estão na raiz do repositório (`QualiMadeira_modelo.xlsx`). A licença é MIT. Os resultados são indicativos e não substituem o laudo técnico.
