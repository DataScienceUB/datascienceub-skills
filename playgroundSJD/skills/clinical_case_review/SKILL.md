---
name: clinical_case_review
description: Utilitza quan vulguis revisar un cas clínic de salut mental simulat o anonimitzat per produir un resum estructurat i prudent amb fets, inferències raonables, informació absent i preguntes de seguiment. No s'ha d'usar mai per a un diagnòstic autònom ni per prendre decisions de tractament.
version: 0.2.0
---

# Revisió de Cas Clínic

## Propòsit
Convertir notes clíniques en revisions estructurades que preparin clínics per a reflexió, supervisió o seguiment. Aplica criteris d'avaluació infanto-juvenil quan escaigui (IACAPAP A.5).

## Límits de seguretat clau
- Només casos anonimitzats.
- No realitza diagnòstics.
- No prescriu medicació.
- No infereix fets no presents al text.
- Manté la responsabilitat clínica humana en tot moment.

## Estructura obligatòria de sortida

### 1. Abast i advertiment
Declaració explícita que la revisió és suport a la decisió per a professionals, no una decisió clínica autònoma.

### 2. Context de derivació
Qui consulta, expectatives expressades, informants presents i absents.

### 3. Fets explícits
Únicament dades presents al text, sense inferències. Clarament delimitats.

### 4. Anàlisi SIFFE
- **S** — Símptomes: freqüència, intensitat, durada i evolució.
- **I** — Impacte: família, escola, iguals, funcionament diari.
- **F** — Factors de risc (les 3 Ps): predisposants, precipitants i perpetuants.
- **F** — Fortaleses: recursos personals, relacionals i contextuals.
- **E** — Explicacions i tractaments previs: historial, adherència, resultats.

### 5. Context de desenvolupament
Interpretació dels símptomes en relació amb l'edat i l'etapa evolutiva. Fites i discontinuïtats rellevants.

### 6. Hipòtesis prudents
Formulades amb llenguatge cautelós ("mereix exploració", "és compatible amb", "no pot descartar-se"). Inclou diagnòstic diferencial i comorbiditats possibles.

### 7. Informació absent
Dades clínicament rellevants no presents al text: risc, medicació, antecedents, dinàmica familiar, context escolar, etc. Etiquetades com "no explorat", no com a evidència negativa.

### 8. Mapa risc/protecció
Factors de risc i factors protectors identificats al text, sense categorització definitiva de risc.

### 9. Preguntes de seguiment
Preguntes pràctiques i no tendencioses que un clínic podria fer en la propera visita.

### 10. Llista de no-inferències
Conclusions explícites a evitar basant-se en la informació disponible.

### 11. Proposta de revisió humana
Paràgraf orientador per al professional que rep el resum: quins aspectes prioritzar, quines incerteses validar.

## Estil requerit
Professional i cautelós. Prefereix "necessita avaluació" a afirmacions categòriques. Prefereix "refereix" o "s'observa" a "és" o "pateix".
