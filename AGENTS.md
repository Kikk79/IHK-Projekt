# PROJECT KNOWLEDGE BASE

**Generated:** 2026-01-13
**Type:** Documentation Repository
**Language:** German (DE)

## OVERVIEW

German vocational training materials for IHK (Industrie- und Handelskammer) IT professional certification. Contains project application guides, official IHK documents, and templates for final examination Part 2.

Target professions: FISI (40h projects), FIAE (80h projects), FIDP, Kfm DigiMan, Kfm IT SysMan.

## STRUCTURE

```
PROJEKT/
├── 1_Anleitung Projektarbeit ANtrag/    # Project application instructions (9 MD + 3 PDF)
│   ├── 00-08: Step-by-step guides (German)
│   └── 09-11: PDF checklists, evaluation matrices, sample applications
├── 2_Infos_IHK_projekt/                # Official IHK information (4 PDF)
│   ├── Registration forms
│   ├── General project work guidelines
│   ├── DIHK implementation aids
│   └── 2025 information sheets
└── 3_MicrosoftWord_Vorlage_Projektdokumentation_ITBerufe.pdf  # Documentation template
```

## WHERE TO LOOK

| Task | Location | Notes |
|------|----------|-------|
| Start learning path | `1_Anleitung/00_uebersicht.md` | Table of contents |
| Entry requirements | `1_Anleitung/01_einstiegsvoraussetzung.md` | Prerequisites, timing |
| Project methodology | `1_Anleitung/02_modell_vollstaendige_handlung.md` | 6-phase model required |
| Contact support | `1_Anleitung/03_ansprechpartner.md` | IBB support by specialization |
| Application best practices | `1_Anleitung/04-05_best_practice_tipps_*.md` | Selection, planning, structure |
| Before upload | `1_Anleitung/06_tipps_vor_upload.md` | CRITICAL: 3-attempt rule, SMART goals |
| Rejection handling | `1_Anleitung/07_abgelehnte_projektantraege.md` | Common mistakes, solutions |
| Templates & downloads | `1_Anleitung/08_hilfsmittel_downloads.md` | Available resources |
| Official IHK requirements | `2_Infos_IHK_projekt/*.pdf` | Regional requirements override all |
| Project documentation template | `3_MicrosoftWord_Vorlage_*.pdf` | Word template for final documentation |

## CONVENTIONS

### File Organization
- Numbered prefixes (`1_`, `2_`) for top-level directories
- Sequential numbering (`00_`-`08_`) for learning unit pages
- PDF files in German with IHK official naming

### Document Structure (Markdown)
- Header: `# Lerneinheit: Vorbereitung des Projektantrages für die IHK`
- Sub-header: `## Seite X: [Page Title]`
- Section: `### Übersicht` (Overview)
- Separator: `---`
- Key terms: `### Schlüsselbegriffe für LLM-Verarbeitung`
- Footer: `*Nächste Seite: Navigation über 'Weiter'-Button*`

### Anti-Patterns (This Project)
| Pattern | Location | Issue |
|---------|----------|-------|
| `nul` file | Root directory | Shell artifact, should be removed |
| Spaces in folder names | `1_Anleitung Projektarbeit ANtrag`, `2_Infos_IHK_projekt` | Inconsistent naming |
| Inconsistent PDF naming | `AnmeldungTeil2 mit Infos.pdf` | Mixed case/spaces |
| Missing MD references | `00_uebersicht.md` lines 15-17 | Points to non-existent markdown files |

## CRITICAL RULES (IHK Requirements)

### 3-Attempt Rule
- Maximum 3 project application submissions to IHK
- If 3rd rejected → exam fails automatically
- **Aim for approval on first attempt** (draft can be reviewed internally via ILIAS)

### SMART Goals
Project goals MUST be:
- **S**pecific (Spezifisch)
- **M**easurable (Messbar)
- **A**ccepted (Akzeptiert)
- **R**ealistic (Realistisch)
- **T**erminated (Terminiert)

### 6-Phase Project Methodology (Modell der vollständigen Handlung)
1. **Informieren** - Gather and analyze information
2. **Planen** - Create project plan (Pflichtenheft)
3. **Entscheiden** - Make decision with instructor
4. **Ausführen** - Implement project
5. **Kontrollieren** - Verify results (Abnahmeprotokoll)
6. **Bewerten** - Evaluate project (reflection, goal achievement)

### Hour Planning
- FISI: 40h total, 6h recommended for customer documentation
- FIAE: 80h total, 12h recommended for customer documentation
- No time blocks larger than 4 hours
- Tabular format required

### Regional Requirements
- **Regional IHK requirements supersede all others**
- Each IHK has different evaluation criteria
- Check local IHK guidelines before submission

## KEY DOCUMENTS

| Document | Purpose | Location |
|----------|---------|----------|
| Lastenheft | Customer requirements (what they want) | Created during project |
| Pflichtenheft | Implementation plan (how to build) | Created during project |
| Kundendokumentation | Operating instructions for customer | Phase 4: Ausführen |
| Abnahmeprotokoll | Customer acceptance verification | Phase 5: Kontrollieren |
| Projektabschlussprotokoll | Reflection and goal achievement | Phase 6: Bewerten |

## PROJECT WORKFLOW

1. Praktikumssuche (Find internship/company)
2. IHK Prüfungsteil 2 Anmeldung (Register for exam)
3. Projektantrag erstellen (Create project application)
4. Internal review (optional via ILIAS)
5. Submit to IHK (3 attempts max)
6. Await approval (Genehmigung abwarten)
7. Execute project (6 weeks before written exam)
8. Create project documentation
9. Submit to IHK for evaluation

## NOTES

- This is **NOT a software codebase** - it's training documentation
- No build/CI infrastructure required
- No automated testing - testing refers to manual IT system verification
- All materials are in German
- Project counts 50% toward final exam grade
- Start with `00_uebersicht.md` for navigation
- **ALWAYS check regional IHK requirements** before submission
