# Curriculum reference format

[Curriculum index](curriculum-index.md) > Format guide

**Format version:** 1.

**Content status:** Main catalog landings are bootstrapped and summaries are being populated. The [curriculum index](curriculum-index.md) tracks available records and the landings identify remaining work.

Use Markdown with YAML front matter: one readable, source-linked curriculum summary per subject or named course. Markdown is the maintained source; do not maintain a second JSON or YAML copy of the same curriculum. The [record template](templates/curriculum-record.md) and [Grade 1 curriculum](01-Grade-1/00-Curriculum/README.md) demonstrate the format.

These are original reference summaries, not official curriculum documents, lesson plans, assessment checklists, or a prescribed teaching sequence. The linked provincial sources remain authoritative.

## Provincial curriculum and local implementation

British Columbia publishes the curriculum used as the provincial reference here. SD43 is a local implementation context, not a separate provincial or national curriculum.

Keep three layers distinct:

| Layer | Where it belongs | Authority |
| --- | --- | --- |
| Provincial subject or course expectations | A subject's `curriculum.md` | BC Curriculum and applicable provincial policy |
| District or school program implementation | A clearly labelled context page linked from the grade overview | The named district or school |
| Lessons, activities, resources, and tools | The existing resource and tool categories, with explicit curriculum references | The item's author; not a new provincial requirement |

Do not turn a school's term plan, suggested textbook, or enrichment activity into a province-wide expectation.

## Programs and languages

Every curriculum record must explicitly list its applicable programs. There is no implicit program default.

| `programs` value | Meaning |
| --- | --- |
| `english-language` | The English-language program |
| `early-french-immersion` | Early French Immersion |
| `late-french-immersion` | Late French Immersion; only for applicable grades and records |
| `francophone` | The distinct first-language Francophone program |

A program label's presence in this table or in a source-linked landing does not establish written coverage. Use the actual records and grade/program indexes to identify reviewed applicability and remaining gaps.

The English-language program is the initial research and navigation priority. Prioritization must never hide missing coverage for another program or label English-only material as universal.

- Share a provincial subject summary across programs only when the applicability is supported by sources. List each applicable program in `programs`; do not duplicate identical summaries into program folders.
- Keep English Language Arts, French Immersion Language Arts, Francophone language arts, and Core French distinct. A French translation of a mathematics document is not a different mathematics curriculum or evidence of program applicability.
- `document_language` describes the language of this repository document. `source.language` describes the official source. Neither field, by itself, specifies the language of classroom instruction.
- Put program-specific language of instruction and scheduling in the grade overview or a sourced district context page. Do not infer them from the document language.
- Label resources and tools separately. An English worksheet does not automatically suit an immersion classroom just because the mapped mathematics expectations are shared.
- Research Early and Late Immersion separately where their language-arts expectations or English Language Arts schedules differ.

All current summaries are written in English, including the summary of the French-language immersion source. This is not a claim to provide French teaching materials or an authorized translation. Future translated summaries may use `curriculum.fr.md`, keep the same record and item IDs, and set an appropriate `document_language`. Link the language editions together. Never use translation naming to merge different programs' language-arts curricula.

## Files and grade scope

Keep the existing grade and category directories. Every curriculum category has a `README.md` grade index. Each subject or course has a stable `README.md` landing, whether or not its separate `curriculum.md` record has been written. Indexes and landings must distinguish pending content from written summaries and reviewed program coverage.

```text
01-Grade-1/
  00-Curriculum/
    README.md
    sd43-context.md
    mathematics/
      README.md
      curriculum.md
    english-language-arts/
      README.md
      curriculum.md
    french-immersion-language-arts/
      README.md
      curriculum.md
  01-Resources/
  02-Tools/
  03-Additional-Content/
```

Use the subject directory names already established by the landings consistently across grades. Official website abbreviations such as `adst` and `fral` belong in source URLs; repository subject names need not copy them.

For a subject with multiple courses or program variants, add a named directory beneath the subject and put its landing and record there:

```text
<grade>/00-Curriculum/<subject>/<course-or-variant>/README.md
<grade>/00-Curriculum/<subject>/<course-or-variant>/curriculum.md
```

The same record format applies to Kindergarten, grade-banded standards, and Grades 10-12 course choices:

- `grade` is the target repository grade: `"K"` or `"1"` through `"12"`. Kindergarten is not Grade 0.
- `source.grade_scope` records the grades covered by the relevant source standards, not every grade included in a downloadable compilation.
- A Grade 1 record may reference K-3 standards; it must explain that the standards are grade-banded rather than invent Grade 1-specific requirements.
- Use `course` for a named course or distinct curriculum variant; use `null` for an unsplit subject-level record. The slug is a repository identifier, not a ministry course code.
- Keep a transition label such as an immersion source's `6T` associated with its actual grade and a distinct variant. Do not create a new top-level grade directory.
- At secondary level, distinguish required areas, course alternatives, and electives in the overview using current policy sources. A course's existence does not mean every student must take it. Do not extrapolate the elementary subject list into a senior graduation plan.

The central index, grade overviews, subject/course landings, special-entry page, and district context pages are navigation or explanatory documents, not curriculum records. They do not use the record front matter or pretend to contain learning standards.

The [special-entry page](curriculum-special-entries.md) holds stable landing anchors for CLE, CLC, and Additional Offerings because the main catalog does not give them ordinary grade selectors. Fill in source-backed placement and course links there; do not invent grade assignments to fit the directory structure.

### Course hosts and delivery years

Keep curriculum grade, registry/credit classification, student eligibility, and teaching year distinct. A course may have a registry classification but allow delivery across several grades.

Where a verified registry or credit-level designation supplies a canonical host, `grade` identifies that repository host and `source.grade_scope` retains the full source-backed band. Explain the host in the title or Scope and use section, cite the registry and applicable policy, and link the record from all relevant grade overviews. Do not duplicate one curriculum merely because it can be taken in several years or has split-credit or translated reporting codes.

For example, CLE has a source-backed administrative Grade 10 host and CLC a Grade 12 credit-level host, while both permit delivery in 10, 11, or 12. Their records use their respective host grades with `source.grade_scope: ["10", "11", "12"]`; neither folder implies a compulsory teaching year. Keep the `CLE` and `CLC` special-entry anchors as cross-grade navigation.

If no defensible host or source band is established, keep placement explicitly pending rather than choosing a grade from common practice. Reporting alternatives that share standards belong in the same record/landing inventory; genuinely different curricula require distinct records.

## Navigation contract

Use the [curriculum index](curriculum-index.md) as a portable, GitHub-readable counterpart to the [BC catalog's](https://curriculum.gov.bc.ca/curriculum) area-to-grade/course navigation. No separate website or generated content store is required.

| Level | Required navigation |
| --- | --- |
| Root README | Prominent links to browsing by area, grade, and program |
| Central index | Areas with stable local landing links, a separate Written summaries column, grade indexes, reviewed program coverage, and official-source links |
| Grade overview | Pending and written entries, program entry points where populated, and direct section links for existing records |
| Subject/course landing | Official source, content status, next authoring step, and links to a record and its sections when available |
| Curriculum record | Breadcrumbs to the central index and grade overview, section quick links, and stable item headings |
| Resource or tool | Descriptive links to the exact curriculum items it supports, plus explicit program and language suitability |

Ordinary grade-selector links use only `K`, `1`, `2`, ..., `12`, without a `Grade` prefix. Preserve actual special-entry labels such as `6T`, `7T`, `CLE`, and `CLC`; they are not additional grades. Display links inline, separated by spaces and ordered as in the catalog. Keep descriptive labels for breadcrumbs and record/item citations; this display convention does not change directory names or identifiers.

Main catalog selectors link to actual landing pages, including entries that still need content. Pending landings are intentional; nonexistent destinations and empty curriculum records are not. Only publish summary and section links when the record exists. Keep official BC destinations, local landings, and written summaries distinguishable.

Each grade overview uses `#choose-a-program` for its program chooser and `#subjects-and-learning-standards` for the subject/course table. Program entry headings use anchors matching the canonical labels: `#english-language-program`, `#early-french-immersion`, `#late-french-immersion`, and `#francophone`. Include a program entry only when corresponding curriculum records and applicability are established; otherwise state that the summary pathway is not populated.

Keep these record-section anchors stable:

| Section | Anchor |
| --- | --- |
| Scope and use | `#scope-and-use` |
| Big Ideas | `#big-ideas` |
| Curricular Competencies | `#curricular-competencies` |
| Content | `#content` |
| Elaborations and boundaries | `#elaborations-and-boundaries` |
| Sources and rights | `#sources-and-rights` |

The English headings generate these anchors in GitHub Markdown. If a future language edition localizes section headings, preserve the canonical anchors explicitly. Item headings such as `### C-01` remain unchanged across language editions.

Place breadcrumbs and the quick-link row after the record title and before Scope and use. Include a return link at the end as well. Adjust paths for course-level nesting rather than copying a fixed number of parent-directory steps from another record.

Keep navigation synchronized with the record metadata. A landing captures a source entry and pending work; it is not evidence of reviewed curriculum alignment. Once a record exists, its metadata is authoritative for local grade, course, programs, document language, and coverage status. Do not claim that every program applies merely because a subject has a landing or record.

When adding senior courses or immersion transitions, preserve the actual source's choices and labels. The BC catalog includes named career courses and separate immersion transition entries; it does not have an identical grade-only route for every area. Confirm source links rather than constructing them from a guessed pattern.

## Filling a landing page

The expected content workflow starts with an existing landing. Use the [landing template](templates/curriculum-landing.md) only when another real source entry or a newly inventoried course needs a landing.

| Landing status | Meaning and next action |
| --- | --- |
| Needs summary | A source entry is linked, but no local curriculum summary is written; review the source and create `curriculum.md` |
| Needs course inventory | The source is a course list; identify the actual courses and create named course landings before writing their records |
| Summary draft | A real record exists with `status: draft`; describe remaining gaps and do not count it as source-checked coverage |
| Summary available | A corresponding record has `status: source-checked`; link the record and its three curriculum sections and show its program/document-language metadata |

Special entries may use more specific pending statuses for placement review or offering inventory. A course-list parent must remain honest about partial inventory or incomplete course coverage; one finished child does not make the entire subject complete.

1. Read the official entry linked from the landing. Confirm whether it is core curriculum, a course list, or a cross-grade/other entry. Establish the target grade or grade band, applicable programs, and source language before assigning metadata.
2. For a core entry, create the adjacent `curriculum.md` using the record template. For a course list, first inventory its actual choices and add named course folders containing `README.md` landings and, as authored, `curriculum.md` records. Keep the parent landing as the course navigator.
3. Write original summaries with the required metadata, sections, stable local IDs, source locators, and rights information. Do not copy an empty template into place and call it completed content.
4. Record the actual alignment review date after comparing the summary with the source. Until then, keep meaningful work in `draft` status with explicit gaps. The date on which the catalog link was captured is not a curriculum review date.
5. Update the landing with the record link, section links, program suitability, document language, and accurate status. Preserve the landing URL; add content behind it instead of moving the selector to a different destination.
6. Update the grade index's subject and program pathways. Add source-checked records to the central index's Written summaries column and update coverage statements; do not relabel every program as complete.

Use the source's actual entry type, not a blanket rule that every K-9 entry is core or every secondary entry is a course list. For example, the captured catalog routes Arts Education 9 to a course list and Social Studies 10 to a core entry.

The `6T` and `7T` landings are under `transition-6t` and `transition-7t` within Grades 6 and 7. Keep them distinct from the regular entries. For a record in one of those directories, use the actual numbered target grade and the matching course/variant slug; do not create a Grade 6T or Grade 7T.

For CLE, CLC, and Additional Offerings, begin at the special-entry page and establish placement or inventory from authoritative sources. Link appropriately placed records back from the stable named-entry anchors. Do not equate the BC Additional Offerings category with this repository's unmapped enrichment category.

Prioritize English-language summaries when sequencing content work while recording other programs and gaps explicitly. If a source is inaccessible or a scope decision cannot be established, describe the blocker on the landing rather than inventing curriculum or claiming completion.

## Required front matter

Use the fields in the template without renaming them.

| Field | Type and rule |
| --- | --- |
| `schema_version` | Integer; `1` for this format |
| `record_id` | Stable, unique repository ID, such as `bc-g01-mathematics` |
| `jurisdiction` | `CA-BC` for provincial BC records |
| `grade` | Quoted string: `"K"`, `"1"`, ..., `"12"` |
| `subject` | Descriptive kebab-case subject slug, matching the subject directory |
| `course` | Kebab-case course or variant slug matching its directory, or `null` |
| `programs` | Non-empty list of applicable values from the program table |
| `document_language` | BCP 47 language tag, such as `en-CA` or `fr-CA` |
| `coverage` | `core-summary`; a condensed treatment of Big Ideas and learning standards, not a transcript or a complete elaboration inventory |
| `status` | `draft` or `source-checked`; the latter means the author compared the summary to the primary source, not ministry endorsement or independent educator review |
| `source.authority` | The publisher responsible for the expectations |
| `source.title` | Identifying source title; an English title gloss is acceptable for a French source if labelled as such |
| `source.url` | Direct, public, authoritative subject/course URL |
| `source.language` | Language tag for the actual source content |
| `source.grade_scope` | Non-empty list of quoted target grade strings covered by these source standards |
| `source.version` | Explicit source revision/version if established; otherwise `null` |
| `source.rights` | Source copyright/license and the reuse approach |
| `alignment_verified_on` | Quoted ISO date `YYYY-MM-DD`, or `null` for an unverified draft |

Use `bc-gk-...` for Kindergarten IDs and `bc-g01-...` through `bc-g12-...` for numbered grades. Add a descriptive course/variant suffix when needed to avoid collisions. Program lists may change after source review without changing the record ID.

`alignment_verified_on` is a review date, not the source publication date, a curriculum edition, or an assurance that the source will remain unchanged. Do not call a curriculum a "2026 edition" merely because it was checked in 2026.

The unique key for a language edition is `(record_id, document_language)`. Keep the identifier stable when moving files, and update inbound links if a path changes.

## Required body sections

Use these second-level headings, in this order:

1. **Scope and use**: identify the target learners, programs, document language, overall learning objective, prerequisites, materials, and how to use the reference. Distinguish practical suggestions from official entry requirements.
2. **Big Ideas**: original summaries of the subject's enduring understandings.
3. **Curricular Competencies**: original summaries of what learners do, retaining the source's important strands.
4. **Content**: original summaries of what learners know, preserving important limits and distinctions.
5. **Elaborations and boundaries**: link to official elaborations, identify coverage limits, and prevent likely misreadings.
6. **Sources and rights**: identify the primary source, review date, rights, and relevant supporting sources.

Keep all six headings even for an exception. For example, ADST K-3 integrates content from other areas: explain the source's integration instruction under Content instead of inventing a separate content list.

The three curriculum components follow the [BC curriculum model](https://curriculum.gov.bc.ca/curriculum/overview). [Core Competencies](https://curriculum.gov.bc.ca/competencies) run across subjects and grades; they are not a replacement for subject-specific Curricular Competencies.

### Stable local references

Under the three curriculum sections, use headings containing only local IDs:

```markdown
### BI-01

An original summary of one idea or a clearly related group of ideas.

**Source locator:** [S1], Big Ideas, identifiable topic or phrase.
```

Use `BI-01`, `CC-01`, and `C-01` sequences for Big Ideas, Curricular Competencies, and Content. Their GitHub heading anchors are `#bi-01`, `#cc-01`, and `#c-01`. A complete local reference is, for example, `bc-g01-mathematics#c-01`.

These IDs are assigned by this repository. They are not official BC standard codes and their numbers do not denote source item numbers, priority, teaching order, or assessment levels.

Each item needs a source locator: the source reference, source section, and recognizable topic or subheading. For a French source, a labelled English locator gloss may be used. Locators are reading instructions, not invented deep links on the official website.

Group related expectations where useful, but retain important qualifications and strands. Do not add expectations from an adjacent grade. Do not promote an optional elaboration example into a required topic. Preserve First Peoples perspectives wherever they occur in the curriculum rather than moving them into enrichment.

Never silently renumber existing IDs. Allocate a new ID for a new meaning. If an item is retired, preserve its old heading with a short retirement note and replacement reference.

### Linking to records and items

Use relative Markdown links for repository content, so navigation works on branches and in local Markdown viewers. Use ordinary URL `/` separators in Markdown destinations; filesystem commands may use the platform's native separators.

| Reference | Canonical form | Rendered example |
| --- | --- | --- |
| Whole record | Descriptive subject/course and grade label linked to its file | [Mathematics 1](01-Grade-1/00-Curriculum/mathematics/curriculum.md) |
| Section | Record label plus section name, linked to its canonical section anchor | [Mathematics 1: Content](01-Grade-1/00-Curriculum/mathematics/curriculum.md#content) |
| Specific item | `<Subject/course> <grade>: <item ID>`, linked to the lowercase item anchor | [Mathematics 1: C-01](01-Grade-1/00-Curriculum/mathematics/curriculum.md#c-01) |
| Structured item key | `<record_id>#<lowercase-item-id>` | `bc-g01-mathematics#c-01` |

For example, from a root-level document:

```markdown
[Mathematics 1: C-01](01-Grade-1/00-Curriculum/mathematics/curriculum.md#c-01)
```

From another directory, adjust the relative file path but preserve the destination item anchor and canonical key. In prose outside the record, do not cite only `C-01` or show only a raw path: both the target and its readable identity should be clear. Inside a record, a local link such as `[C-01](#c-01)` is sufficient.

When a file moves or an item is retired, maintain the old item's meaning or retirement note and update navigation and inbound links in the same change. Do not rename IDs just to match a new display title.

### Connecting resources and tools

Link directly to the relevant curriculum record and item anchor, and include explicit program and language metadata on the resource or tool. For example:

```yaml
programs:
  - english-language
document_language: en-CA
curriculum_refs:
  - record_id: bc-g01-mathematics
    items:
      - C-01
alignment_verified_on: "2026-09-14"
```

The resource's prose must still state its specific learning objective, instructions, prerequisites, materials, and the source expectation it supports. A reference to a broad summary does not establish that every activity is aligned. Use the original source to resolve narrower claims.

## Rights and source freshness

Write independent summaries in original language and link to official wording. Do not bulk-copy, closely rewrite line by line, translate entire official documents, or commit curriculum PDFs, DOCX files, images, or third-party learning resources without documented redistribution permission.

The [BC copyright policy](https://www2.gov.bc.ca/gov/content/home/copyright) does not grant blanket redistribution permission. Do not assume the Open Government Licence covers curriculum pages. Record source-specific permission if it is established later; permission for one source does not relicense the repository or other sources.

This format does not select a license for the repository's original writing. Source attribution is not a claim of permission to redistribute the source.

Check both a URL's destination and its actual content. A successful HTTP response, an empty course shell, or a redirect to a district home page is not verification. Prefer live subject pages over old search results or school-hosted copies. If the primary source is inaccessible, leave the record as a draft, describe the gap, and do not fill it from memory.

When revisiting a record, compare meaning and program applicability as well as links. Preserve local IDs, update the review date only after the comparison, and describe material changes in the change history or pull request.

## Extending to other grades in parallel

Start from the bootstrapped landings and agree the grade, program, and course-inventory scope for each content workstream. Give each workstream a bounded grade or grade group and the same committed template and instructions.

Each workstream owns only its assigned grade directories and their overviews. Keep root documentation, the central index, and the shared template under a single coordinator to avoid conflicting format changes. Grade owners report the area/grade/program entries the coordinator must add to the central index. All workstreams must declare program coverage and gaps; English-language coverage may be completed first, but it must not be presented as completion of every program.

Fill the existing source-linked entries after researching the actual grade bands, courses, and program variants. Kindergarten, transition years, and course catalogs need source-specific decisions rather than mechanical copying of Grade 1. Expand course inventories where needed without rebuilding the grade/area navigation. Keep resources, tools, and enrichment placeholders until real content is added.

Before combining results, confirm consistent metadata, unique IDs, valid local links, source-backed program labels, dates, and rights. Do not silently expand to unresearched programs or claim a complete K-12 catalog while grades or programs are still missing.

## Design sources

The curriculum model, Core Competencies, and copyright sources linked above were checked on **2026-09-14**. Program distinctions are supported by the [provincial French Immersion policy](https://www2.gov.bc.ca/gov/content/education-training/k-12/administration/legislation-policy/public-schools/french-immersion-program) and the Grade 1 [SD43 context](01-Grade-1/00-Curriculum/sd43-context.md). Official sources take precedence over this format guide.
