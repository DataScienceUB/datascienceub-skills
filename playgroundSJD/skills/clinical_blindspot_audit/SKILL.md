---
name: clinical_blindspot_audit
description: Utilitza quan vulguis auditar un resum clínic, una revisió de cas de salut mental o una nota clínica generada per IA per detectar omissions, supòsits ocults, tancaments prematurs, estigma, ancoratge i preguntes contextuals que falten.
version: 0.2.0
---

# Auditoria de Punts Cecs Clínics

## Propòsit
Identificar allò que un clínic o un resum generat per IA pot estar passant per alt. Aquesta habilitat s'inspira en la revisió de "punts cecs": cerca omissions, supòsits ocults, conclusions prematures i oportunitats desaprofitades.

Quan el cas impliqui un infant o adolescent, s'apliquen dimensions addicionals derivades dels criteris de l'avaluació clínica infanto-juvenil (IACAPAP A.5).

## Entrades
- Text original del cas.
- Resum generat per IA o esborrany de nota.
- Qualsevol criteri clínic local o política de seguretat.

## Dimensions de l'auditoria

### Dimensions generals

1. **Informació absent** — Quina informació clínicament rellevant manca? L'absència queda marcada clarament com "no explorada"?

2. **Tancament prematur** — El text salta a una sola explicació? S'ignoren alternatives diagnòstiques?

3. **Supòsits ocults** — Supòsits socioeconòmics, familiars, de gènere, culturals, migratoris o educatius presents?

4. **Infradetecció de risc** — Seguretat, autolesió, violència, consum de substàncies, protecció o deteriorament funcional insuficientment explorats?

5. **Sobredetecció de risc** — La sortida exagera el risc més enllà de l'evidència?

6. **Estigma i enquadrament** — Llenguatge que moralitza, culpabilitza, patologitza o medicalitza en excés?

7. **Factors protectors i fortaleses** — Es noten fortaleses, relacions, motivació, rutines i conducta de cerca d'ajuda?

8. **Preguntes de seguiment accionables** — Genera preguntes que un clínic podria fer?

### Dimensions específiques per a casos infanto-juvenils

9. **Avaluació aïllada del nen** — S'ha avaluat sense context familiar, escolar i comunitari? Els símptomes poden reflectir incompatibilitat ambiental.

10. **Font i motiu real de la derivació** — Qui ha iniciat la consulta? Les expectatives dels pares, escola, pediatre i nen estan explorades o s'assumeix coincidència?

11. **Perspectiva múltiple d'informants** — Informació de pares, educadors, pediatre i altres cuidadors considerada? Desacords tractats com a dada clínica?

12. **Context de desenvolupament ignorat** — Els símptomes s'interpreten sense tenir compte l'edat? Discontinuïtats o retards en fites evolutives ignorats?

13. **Marc SIFFE incomplet**
    - **S** — Freqüència, intensitat, durada i evolució del símptoma: explorat?
    - **I** — Impacte en família, escola, iguals i desenvolupament: explorat?
    - **F** — Factors de risc (les 3 Ps): predisposants, precipitants i perpetuants identificats?
    - **F** — Fortaleses del nen, família i entorn: identificades?
    - **E** — Explicacions i tractaments previs: recollits?

14. **Les 3 Ps de factors de risc no aplicades** — Factors confosos sense distinció entre predisposició, precipitació o perpetuació? Els perpetuants són més modificables.

15. **Psicopatologia parental no considerada** — La percepció parental pot estar esbiaixada per la seva pròpia salut mental?

16. **Context escolar absent** — Manquen informes escolars? Declivi acadèmic, diferències entre assignatures o problemes socials/emocionals recollits?

17. **Comorbiditats i diagnòstic diferencial no explorats** — Comorbiditat extremadament freqüent: s'ha considerat? Símptomes com irritabilitat poden correspondre a múltiples trastorns.

## Format de sortida
Taula amb:
- Punt cec
- Per què importa
- Evidència al text
- Pregunta suggerida per al clínic
- Gravetat: Baixa / Mitjana / Alta

Apartat breu de "consells de revisió".

## Limitacions
- No generis diagnòstic.
- No suggereixis tractament.
- No afirmis que el risc és present quan és només no avaluat.
