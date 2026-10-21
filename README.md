# Ugens register — nye virksomheder og konkurser i Danmark, uge for uge

Antal virksomheder **stiftet** (stiftelsesdato) og antal **konkursdekreter** (dekretdato) i Danmark pr.
ISO-uge, fordelt på virksomhedsform, kommune og branche. Opgjort fra CVR-registret af
[Bizdex](https://bizdex.dk/register), fra og med uge 28, 2026. Opdateres automatisk hver mandag.

*Weekly counts of companies founded and bankruptcy decrees in Denmark, by company form, municipality
and industry code, compiled from the Danish business register (CVR). Updated every Monday.*

| Fil | Indhold |
|---|---|
| [`data/ugens-register.csv`](data/ugens-register.csv) | Alle uger, én række pr. optælling |
| [`datapackage.json`](datapackage.json) | Kolonnerne beskrevet ([Frictionless Data Package](https://specs.frictionlessdata.io/data-package/)) |

**Kolonner:** `uge` (ÅÅÅÅ-UU) · `mandag` · `soendag` · `haendelse` (`nye_virksomheder` / `konkurser`) ·
`dimension` (`i_alt` / `virksomhedsform` / `kommune` / `branche`) · `kode` (branchekoden fra CVR for branche) ·
`navn` · `antal` · `foreloebige_tal` (`ja` mens ugens tal stadig kan stige).

**Sådan er tallene opgjort:** en ny virksomhed er en virksomhed, hvis stiftelsesdato i CVR ligger i ugen.
En konkurs er et konkursdekret, hvis dekretdato ligger i ugen; senere trin i det samme bo tælles ikke
igen. En uge udgives otte dage efter dens afslutning og er foreløbig i 28 dage, fordi CVR registrerer
med nogle dages forsinkelse. Filerne indeholder kun antal — ingen virksomhedsnavne.

Hver uge kan også ses som side, med ugens største konkurser: <https://bizdex.dk/register>

## Licens

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Kildeangivelse:
**«Bizdex, baseret på CVR (Erhvervsstyrelsen)»** med link til <https://bizdex.dk/register>.
