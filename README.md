# datascienceub-skills

Claude Code plugin marketplace del [Grup de Data Science & IA de la Universitat de Barcelona](https://github.com/DataScienceUB).

## Instal·lació del marketplace

```bash
/plugin marketplace add DataScienceUB/datascienceub-skills
```

# Skills disponibles

## playgroundSJD — Salut Mental Clínica

Skills d'IA per donar suport al raonament clínic en salut mental. Dissenyades per a formació amb casos simulats o anonimitzats.

```bash
/plugin install playgroundSJD@datascienceub-skills
```

| Skill | Descripció |
|-------|------------|
| `clinical_case_review` | Revisió estructurada de cas clínic amb fets, hipòtesis prudents i preguntes de seguiment |
| `clinical_blindspot_audit` | Detecció d'omissions, supòsits ocults i tancaments prematurs en notes clíniques |
| `clinical_safety_audit` | Auditoria de seguretat de sortides clíniques generades per IA |
| `patient_family_communication` | Transformació de resums clínics en comunicació per al pacient o família |
| `clinical_demo_orchestrator` | Demo completa de formació per a clínics hospitalaris |

> **Avís**: Aquestes eines són exclusivament per a formació amb dades anònimes o sintètiques. No substitueixen el judici clínic professional ni s'han d'usar per a decisions autònomes de tractament.

## Afegir nous skill packs

Per afegir un nou pack de skills al marketplace, consulta [CONTRIBUTING.md](CONTRIBUTING.md).

## Llicència

MIT
