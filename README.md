# Finnish language skill for Claude, Codex and any other AI that supports skills

**Teach AI to write correct Finnish.** This skill provides comprehensive Finnish language rules — spelling, grammar, punctuation, compound words, and style — so AI produces natural, publication-ready Finnish instead of the awkward, anglicism-filled output LLMs typically generate.

Works with Claude Code, Codex, and any other AI agent platform that supports skills.

Built on the official [Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/) (Institute for the Languages of Finland).

---

## Why this exists

LLMs make predictable mistakes when writing Finnish:

- **Compound words split apart**: "verkko sivusto" instead of *verkkosivu*, "asiakas palvelu" instead of *asiakaspalvelu*
- **Anglicisms everywhere**: "sukella syvemmalle", "implementoida", "adressoida"
- **Wrong punctuation**: English-style decimals (3.14 instead of 3,14), Oxford commas, missing commas before subordinate clauses
- **Overly pompous tone**: American corporate rhetoric translated literally into Finnish
- **Capitalization errors**: weekdays, months, and nationalities capitalized (English rules applied to Finnish)
- **Broken inflection**: Finnish has 15 grammatical cases and complex word inflection — LLMs frequently produce wrong case endings, garbled possessive suffixes, and incorrect verb conjugations
- **Mangled ä and ö**: LLMs drop or swap Finnish diacritics, writing "a" instead of "ä" and "o" instead of "ö", which changes word meanings entirely and leads to incorrect translations

This skill catches and prevents all of these. It's been used in production to generate hundreds of pages of Finnish web content.

## Installation

### Option 1: Add to a project (recommended)

Copy the whole skill — `SKILL.md` and the `references/` folder — into your project's skills directory:

```bash
mkdir -p .claude/skills/suomi-finnish
cp -R SKILL.md references .claude/skills/suomi-finnish/
```

`SKILL.md` also works on its own as a single file. You then lose the reference files, which cover lists, sentence structure, inflection and rections, punctuation, conventional notation, and word choice in more detail.

The skill will automatically activate when Claude Code detects Finnish language work.

### Option 2: Add globally (all projects)

```bash
mkdir -p ~/.claude/skills/suomi-finnish
cp -R SKILL.md references ~/.claude/skills/suomi-finnish/
```

### Option 3: One-liner install from GitHub

```bash
git clone --depth 1 https://github.com/akunikkola/suomi-finnish-skill.git /tmp/sfs && mkdir -p .claude/skills/suomi-finnish && cp -R /tmp/sfs/SKILL.md /tmp/sfs/references .claude/skills/suomi-finnish/ && rm -rf /tmp/sfs
```

Replace `.claude` with `~/.claude` to install globally.

### Option 4: Install with AI

Give Claude, Codex, or any other skill-supporting AI the repo URL and ask it to install the skill:

```
Install this skill: https://github.com/akunikkola/suomi-finnish-skill
```

### Option 5: Download the .skill file

Download the ready-made skill package and add it directly to Claude:

[Download suomi-finnish.skill (Google Drive)](https://drive.google.com/file/d/1NkfIn7sj8bvBmAM4ZI2ypP3kv9UtRMHF/view?usp=sharing)

Add the downloaded file to Claude by dragging it into the Claude Code window or importing it as a skill from settings.

## What it covers

| Area | Examples |
|---|---|
| Compound words | When to join vs. separate, hyphenation rules |
| Punctuation | Comma rules, decimal comma, no Oxford comma |
| Capitalization | Lowercase weekdays, months, nationalities |
| Numbers & units | Space as thousands separator, unit spacing (5 kg, 15 %) |
| Abbreviations | Dot rules, inflection with colons (EU:n) |
| Dashes | Hyphen (-) vs. en dash (--) usage |
| Sentence structure | Case agreement, postpositions, possessive suffixes |
| AI-specific errors | Anglicisms, overly formal tone, filler text |
| Proofreading | Step-by-step review checklist |

Plus detailed reference files loaded on demand:

| File | Covers |
|---|---|
| `references/luetelmat.md` | List punctuation, capitalization, parallel form |
| `references/lauserakenne.md` | Locative attributes, dangling essives, joka vs. mikä, nominalization |
| `references/taivutus.md` | Foreign name inflection, rections, abbreviation inflection |
| `references/valimerkit.md` | Semicolon, colon, brackets, omission marks, non-breaking space |
| `references/merkinnat.md` | Dates, times, units, contact details, alphabetical order |
| `references/sanojen-asu.md` | Loanword spelling, anglicisms, parallel accepted forms |

## Usage

Once installed, the skill activates automatically when you:

- Write or generate Finnish text
- Proofread or review Finnish content
- Translate content into Finnish
- Create content for Finnish websites or services

You can also invoke it manually:

```
/suomi-finnish
```

## Sources

All rules are based on:

- [Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/) (Institute for the Languages of Finland)
- [Kielitoimiston sanakirja](https://www.kielitoimistonsanakirja.fi/) (Dictionary of Contemporary Finnish)
- [Iso suomen kielioppi](https://kaino.kotus.fi/visk/etusivu.php) (Comprehensive Finnish Grammar)

## Contributing

Found a rule that's missing or incorrect? Open an issue or PR. Finnish language nerds welcome.

## License

MIT

---

# Suomen kielen skills-tiedosto Claudelle, Codexille tai mille tahansa muulle skills-ominaisuutta tukevalle työkalulle

**Opeta tekoäly kirjoittamaan oikeaa suomea.** Tämä skill antaa tekoälylle kattavat suomen kielen säännöt — oikeinkirjoituksen, kieliopin, pilkutuksen, yhdyssanat ja tyylin — jotta se tuottaa luonnollista, julkaisukelpoista suomea anglismien täyttämän konekielen sijaan.

Toimii Claude Coden, Codexin ja minkä tahansa muun skillejä tukevan tekoälyagentin kanssa.

Perustuu [Kielitoimiston ohjepankin](https://kielitoimistonohjepankki.fi/) virallisiin ohjeisiin.

## Asennus

### Vaihtoehto 1: Projektitasoinen asennus (suositeltu)

Kopioi koko skill eli `SKILL.md` ja `references/`-kansio:

```bash
mkdir -p .claude/skills/suomi-finnish
cp -R SKILL.md references .claude/skills/suomi-finnish/
```

Pelkkä `SKILL.md` toimii myös yksinään, mutta silloin tarkemmat ohjeet jäävät pois.

### Vaihtoehto 2: Globaali asennus (kaikki projektit)

```bash
mkdir -p ~/.claude/skills/suomi-finnish
cp -R SKILL.md references ~/.claude/skills/suomi-finnish/
```

### Vaihtoehto 3: Suora asennus GitHubista

```bash
git clone --depth 1 https://github.com/akunikkola/suomi-finnish-skill.git /tmp/sfs && mkdir -p .claude/skills/suomi-finnish && cp -R /tmp/sfs/SKILL.md /tmp/sfs/references .claude/skills/suomi-finnish/ && rm -rf /tmp/sfs
```

Globaaliin asennukseen korvaa `.claude` polulla `~/.claude`.

### Vaihtoehto 4: Asenna tekoälyllä

Anna Claudelle, Codexille tai muulle skillejä tukevalle tekoälylle repon osoite ja pyydä asentamaan skill:

```
Asenna tämä skill: https://github.com/akunikkola/suomi-finnish-skill
```

### Vaihtoehto 5: Lataa .skill-tiedosto

Lataa valmis skill-paketti ja lisää se suoraan Claudeen:

[Lataa suomi-finnish.skill (Google Drive)](https://drive.google.com/file/d/1NkfIn7sj8bvBmAM4ZI2ypP3kv9UtRMHF/view?usp=sharing)

Lisää ladattu tiedosto Claudeen raahaamalla se Claude Code -ikkunaan tai tuomalla se skillinä asetuksista.

## Mitä skill kattaa

- Yhdyssanasäännöt (yleisin virhetyyppi)
- Pilkutus (sivulauseet, päälauseet, luettelot)
- Iso ja pieni alkukirjain
- Numerot, lyhenteet ja mittayksiköt
- Ajatusviiva vs. yhdysviiva
- Lauserakenne ja kielioppi
- Tekoälylle tyypilliset virheet (anglismit, mahtipontisuus, täytesanat)
- Vaiheittainen oikolukuprosessi

Lisäksi `references/`-kansiossa tarkemmat ohjeet, jotka ladataan tarvittaessa:

- `luetelmat.md` — luetelmien välimerkit, alkukirjaimet ja samanmuotoisuus
- `lauserakenne.md` — paikallissija-attribuutit, kelluva essiivi, joka/mikä, substantiivitauti
- `taivutus.md` — vieraskielisten nimien taivutus, rektiot, lyhenteiden taivutus
- `valimerkit.md` — puolipiste, kaksoispiste, sulkeet, poisjätön merkintä, sitova välilyönti
- `merkinnat.md` — päivämäärät, kellonajat, suureet, yhteystiedot, aakkostus
- `sanojen-asu.md` — vierassanojen asu, anglismit, rinnakkain hyväksytyt muodot

## Lisenssi

MIT
