# Com contribuir a datascienceub-skills

Aquest repositori és un marketplace de skills per a [Claude Code](https://claude.ai/code). Pots afegir nous packs de skills o nous skills dins d'un pack existent.

## Estructura del repositori

```
datascienceub-skills/
├── .claude-plugin/
│   └── marketplace.json          ← índex global del marketplace
├── <nom-del-pack>/
│   └── skills/
│       └── <nom-del-skill>/
│           └── SKILL.md          ← definició del skill
└── README.md
```

---

## Afegir un nou pack de skills

Un **pack** és una col·lecció de skills relacionats (p. ex. `playgroundSJD`).

### 1. Crea la carpeta del pack

```
<nom-del-pack>/
└── skills/
    └── <primer-skill>/
        └── SKILL.md
```

### 2. Crea el `SKILL.md` de cada skill

El format és:

```markdown
---
name: nom_del_skill
description: Descripció breu d'quan cal usar el skill. Claude Code la llegeix per decidir si activar-lo.
version: 0.1.0
---

# Títol del skill

## Propòsit
...

## Entrades
...

## Format de sortida
...

## Limitacions
...
```

**Regles per a la `description`:**
- Ha de ser una frase clara de quan cal usar el skill.
- S'usa per al routing automàtic: Claude la llegeix per decidir si activar el skill.
- Longitud recomanada: 1-2 frases.

### 3. Registra el pack a `marketplace.json`

Afegeix una nova entrada a l'array `plugins` del fitxer `.claude-plugin/marketplace.json`:

```json
{
  "name": "nom-del-pack",
  "source": "./nom-del-pack",
  "description": "Descripció breu del pack",
  "version": "0.1.0",
  "author": {
    "name": "DataScienceUB"
  },
  "keywords": ["paraula1", "paraula2"],
  "category": "categoria"
}
```

---

## Afegir un skill a un pack existent

1. Crea la carpeta `<nom-del-pack>/skills/<nom-del-skill>/`
2. Afegeix el fitxer `SKILL.md` amb el format descrit més amunt
3. Actualitza el camp `version` del pack a `marketplace.json`

---

## Flux de treball recomanat

```bash
# 1. Clona el repositori
git clone https://github.com/DataScienceUB/datascienceub-skills.git
cd datascienceub-skills

# 2. Crea els fitxers del nou skill o pack
mkdir -p nou-pack/skills/nou-skill

# 3. Escriu el SKILL.md
# ... (edita nou-pack/skills/nou-skill/SKILL.md)

# 4. Actualitza marketplace.json
# ... (afegeix l'entrada del nou plugin)

# 5. Commit i push
git add .
git commit -m "Add: nou-pack/nou-skill"
git push
```

---

## Verificació local

Un cop el canvi és a GitHub, qualsevol usuari pot instal·lar el marketplace i el nou skill:

```bash
/plugin marketplace add DataScienceUB/datascienceub-skills
/plugin install <nom-del-pack>@datascienceub-skills
```

---

## Criteris de qualitat

- **Seguretat**: Si el skill genera contingut sensible (clínic, legal, etc.), ha d'incloure explícitament les limitacions i els avisos corresponents.
- **Idioma**: Els skills de DataScienceUB s'escriuen en català o castellà. La `description` del frontmatter pot ser en anglès si el skill es vol fer servir en contextos multilingües.
- **Versió**: Usa [SemVer](https://semver.org/) (`major.minor.patch`). Incrementa `patch` per correccions, `minor` per nous skills, `major` per canvis incompatibles.
