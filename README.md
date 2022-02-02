# de-omicron-wave-results

This repository contains results of a modelling study regarding the spread of the SARS-CoV-2 VOC "Omicron" in Germany.

## Columns and values

| column name | type | description EN | description DE |
| -- | -- | -- | -- |
| `infectious_period_both` | int | Mean infectious period (in days) for both variants | Mittlere Infektiositaetsperiode fuer beide Varianten (in Tagen) |
| `omicron_latent_period` | int | Mean latent period of VOC Omicron (in days) | Mittlere Latenzzeit der VOC Omikron (in Tagen) |
| `booster_reach` | str | Reach of the booster campaign | Reichweite der Auffrischkampagne |
| `booster_VE` | str | Vaccine efficacy of the booster vaccination | Impfeffektivitaet der Auffrischimpfung |
| `contact_reduction_scenario_id` | int | ID of the contact reduction scenario | ID des Kontaktreduktionsszenarios |
| `contact_reduction_strength` | float | prefactor with which the contact modulation f(t) is multiplied | Vorfaktor, mit der die Kontaktmodulation f(t) waehrend der Kontaktreduktionsperiode skaliert wird |
| `contact_reduction_start` | date (ISO 8601) | Date when contact reduction begins | Beginn der Kontaktreduktion |
| `contact_reduction_end` | date (ISO 8601) | Date when contact reduction ends | Ende der Kontaktreduktion |
| `relative_risk_hospitalization` | float | Relative risk (RR) of hospitalization after infection with Omicron as compared to infection with Delta | Relatives Risiko (RR) der Hospitalisierung nach Infektion mit Omicron gegenueber Infektion mit Delta |
| `relative_risk_icu` | float | Relative risk (RR) of ICU admission after infection with Omicron as compared to infection with Delta | Relatives Risiko (RR) der Intensivpflichtigkeit nach Infektion mit Omicron gegenueber Infektion mit Delta |
| `value_type` | str | Wich value is shown in the `value` column | Art des Wertes in der Spalte `value` |
| `date`  | date (ISO 8601) | Date associated with the modeling result given in column `value` | Datum assoziiert mit dem Modellergebnis des Wertes in der Spalte `value` |
| `value` | int | Model result (rounded to nearest integer) | Modellergebnis (gerundet auf ganze Zahl) |

Additional columns regarding combinations of plausible scenarios (rounded to nearest integer) and 180 stochastic simulations per parameter combination:

| column name | type | description EN | description DE |
| -- | -- | -- | -- |
| `95_PI_lower` | int | 95% PI lower bound (rounded to nearest integer) | Untere Schranke des 95% PIs (gerundet auf ganze Zahl) |
| `50_PI_lower` | int | 50% PI lower bound (rounded to nearest integer) | Untere Schranke des 50% PIs (gerundet auf ganze Zahl) |
| `median` | int | median (rounded to nearest integer) | Median (gerundet auf ganze Zahl) |
| `50_PI_upper` | int | 50% PI upper bound (rounded to nearest integer) | Obere Schranke des 50% PIs (gerundet auf ganze Zahl) |
| `95_PI_upper` | int | 95% PI upper bound (rounded to nearest integer) | Obere Schranke des 95% PIs (gerundet auf ganze Zahl) |

### Values: `booster_reach`

| value | description EN | description DE |
| -- | -- | -- |
| `md` | medium booster campaign reach (80% of those that received full vaccination in 2021 receive booster vaccination) | Medium, 80% derjenigen, die in 2021 vollstaendig geimpft wurden, erhalten eine Auffrischimpfung |
| `hi` | high booster campaign reach (100% of those that received full vaccination in 2021 receive booster vaccination) | Hoch, 100% derjenigen, die in 2021 vollstaendig geimpft wurden, erhalten eine Auffrischimpfung |


### Values: `booster_VE`

| value | description EN | description DE |
| -- | -- | -- |
| `lo` | low booster vaccine efficacy (assumption: booster protects as well against infection as 2nd dose) | Niedrige Impfeffektivitaet (Auffr. schuetzt genauso gut vor Infektion wie 2 Dosen) |
| `hi` | high booster vaccine efficacy (assumption: booster protects as well against infection as against symptomatic disease) | Hohe Impfeffektivitaet (Auffr. schuetzt genauso gut vor Infektion wie vor symptomatischer Erkrankung) |

### Values: `value_type`

| value | description EN | description DE |
| -- | -- | -- |
| `inc` | incidence (absolute number of new reported cases per day) | Inzidenz (Zahl der gemeldeten Neuinfektion an diesem Tag, absolut) |
| `hsp` | hospitalization incidence (absolute number of new hospital admissions per day) | Hospitalisierungsinzidenz (Zahl der gemeldeten Neuhospitalisierungen an diesem Tag, absolut) |
| `icu` | total number of patients in ICUs | Gesamtzahl der intensivpflichtigen Patient:innen |

## License

Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
