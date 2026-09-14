# British Columbia K-12 Curriculum Resources

This repository organizes British Columbia K-12 curriculum information alongside learning resources and educational tools. Its purpose is to help families and educators find material that supports specific curriculum expectations and student learning outcomes.

**Browse curriculum:** [By area of learning](curriculum-index.md#browse-by-area-of-learning) | [By grade](curriculum-index.md#browse-by-grade) | [By program](curriculum-index.md#browse-by-program)

## Scope

Content in this repository should:

- support learners from Kindergarten through Grade 12;
- align with the current British Columbia curriculum;
- identify the grade, subject, and curriculum expectation it supports;
- be age-appropriate, accessible, and suitable for educational use; and
- include a reliable source or attribution when content is not original.

This is an independent educational project. It is not affiliated with or endorsed by the Government of British Columbia or any school district. Official curriculum requirements should always be verified against the [BC Curriculum](https://curriculum.gov.bc.ca/) website.

## Start Here

Use the [curriculum index](curriculum-index.md) to browse subject areas and choose a grade, following a similar pattern to the official BC curriculum site. Grade selectors use compact labels `K`, `1`, `2`, ..., `12`, without a `Grade` prefix. Main catalog entry points now have real local landing pages, with official sources and clear content status. A landing link is not a claim that its curriculum summary is complete.

The [Grade 1 curriculum](01-Grade-1/00-Curriculum/README.md) provides worked examples of shared-subject references and distinct English, French Immersion, and Francophone language-arts records. Use the [curriculum index](curriculum-index.md) for current written coverage across grades and programs.

The [curriculum format guide](curriculum-format.md), [landing template](templates/curriculum-landing.md), and [record template](templates/curriculum-record.md) define how to fill the structure. Landings cover the main K-12 catalog entries, including course lists, immersion transitions, and [named or cross-grade entries](curriculum-special-entries.md). Landing statuses distinguish available summaries from pending inventories, source gaps, and other unfinished content.

## Programs and Languages

This repository is intended to serve BC learners beyond a single district or language program. English-language coverage is the initial priority, with French Immersion coverage identified separately rather than treated as an English translation or an afterthought.

Every curriculum record explicitly declares its applicable `programs` and its `document_language`. Shared provincial expectations have one record listing the supported programs; distinct language-arts curricula have separate records. Early French Immersion, Late French Immersion, and the first-language Francophone program are not interchangeable. Consult the record metadata and grade/program indexes for source-backed applicability rather than treating every landing as every program's curriculum.

The main catalog lists all source-derived landing entries without assuming program applicability. Program navigation lists written, source-checked coverage separately. Pending landings must not be labelled as universal or assigned to a program merely because their source exists.

All current summaries are written in English. An English summary of an immersion subject is not an English-language classroom requirement, a French learning resource, or an authorized translation. Resources and tools must state their own program and language suitability.

[SD43 guidance](01-Grade-1/00-Curriculum/sd43-context.md) is kept separate from provincial expectations. Families in other districts can use the BC subject references and consult their own district for implementation details.

## Repository Structure

The repository includes one top-level directory per grade. Two-digit prefixes keep the folders in school order when sorted alphabetically in GitHub or a file browser:

```text
00-Kindergarten/
01-Grade-1/
02-Grade-2/
03-Grade-3/
04-Grade-4/
05-Grade-5/
06-Grade-6/
07-Grade-7/
08-Grade-8/
09-Grade-9/
10-Grade-10/
11-Grade-11/
12-Grade-12/
```

Use `00-Kindergarten` for Kindergarten content and `01-Grade-1` through `12-Grade-12` for numbered grades. Keep sorting prefixes two digits; `00` is only a sorting key, not a grade designation.

Each grade directory has the same four categories, with two-digit prefixes to preserve this order when sorted alphabetically. For example:

```text
01-Grade-1/
|-- 00-Curriculum/
|-- 01-Resources/
|-- 02-Tools/
`-- 03-Additional-Content/
```

- **00-Curriculum** contains curriculum summaries or references organized by subject and learning standard.
- **01-Resources** contains lessons, exercises, readings, media, and other material tied to a curriculum expectation.
- **02-Tools** contains applications, templates, scripts, or interactive aids tied to a curriculum expectation.
- **03-Additional-Content** contains useful enrichment material that does not map directly to a curriculum expectation.

Within each category, organize content by subject when multiple subjects are present.

Within `00-Curriculum`, use a `README.md` grade index and a `README.md` landing in each subject directory. Write the actual curriculum summary in a separate `curriculum.md` beside the landing. For multiple courses or program variants, add named directories beneath the subject, each with its own landing and record. Follow the [format guide](curriculum-format.md) for grade bands, course choices, stable local reference IDs, and future language editions.

The central [curriculum index](curriculum-index.md) is the cross-grade navigation layer. Its main grade links point to stable landing pages; its Written summaries column points to actual records. Grade indexes show pending landings and, where records exist, direct links to Big Ideas, Curricular Competencies, and Content. Keep landings and indexes synchronized as content is added. Pending landing pages are expected; links to nonexistent records are not.

For a course with flexible delivery across grades, a source-backed registry or credit-level designation may determine its canonical directory host. That host must not be presented as a required teaching year. Preserve the full `source.grade_scope`, explain the distinction, and cross-link the shared record from every applicable grade. See [course-host conventions](curriculum-format.md#course-hosts-and-delivery-years).

Empty category directories contain a `.gitkeep` placeholder so they are included in Git. Remove the placeholder when adding content to that directory.

## Filling In Curriculum

The expected next work is to fill existing landings, not rebuild the navigation or create a second subject hierarchy.

1. Open a landing marked **Needs summary** or **Needs course inventory**, and read its official source.
2. Establish the source's grade scope, course choices, and program applicability. If it is a course list, inventory the actual courses and create named course landings before writing individual records.
3. Write an original, source-linked `curriculum.md` using the record template. Preserve the YAML fields, required sections, stable local IDs, source rights, and honest review dates.
4. Update the landing to **Summary draft** while work is incomplete, or **Summary available** when the record is source-checked. Add the summary and section links, explicit program coverage, and document language.
5. Update the grade's subject/program navigation and the central index's Written summaries column and coverage statements. Keep the established landing URL stable.

The [full workflow](curriculum-format.md#filling-a-landing-page) covers transition entries, course placement, and review. Parallel contributors own their assigned grade entries and indexes; a coordinator integrates shared navigation changes. Do not turn a catalog-capture date into an alignment verification date or mark an empty template as completed curriculum.

## Content Requirements

Every resource or tool must include enough context for a reader to understand its educational purpose. At minimum, document:

- grade and subject;
- applicable program or programs, and the document's language;
- related curricular competency or content expectation;
- learning objective;
- prerequisites or required materials;
- instructions for use;
- source and license, where applicable; and
- the date on which external curriculum alignment was last verified.

If an item has no direct curriculum association, place it under `03-Additional-Content` and describe its intended enrichment value.

Do not commit copyrighted material unless its license permits redistribution. Prefer links to authoritative sources when redistribution rights are unclear, and never include student personal information, credentials, or private assessment data.

Curriculum records use original summaries with links to the official wording. The [BC copyright policy](https://www2.gov.bc.ca/gov/content/home/copyright) does not grant blanket permission to mirror curriculum documents. A source review date is not a publication date or a guarantee of continuing accuracy.

When referencing a specific item, use a descriptive link such as [Mathematics 1: C-01](01-Grade-1/00-Curriculum/mathematics/curriculum.md#c-01). Preserve its canonical local reference, `bc-g01-mathematics#c-01`, in structured mappings. Follow the [linking convention](curriculum-format.md#linking-to-records-and-items); a bare item ID is not unique across subjects.

## Contributing

1. Create or update content in the appropriate grade, subject, and category.
2. Confirm curriculum alignment using an authoritative source.
3. Add attribution and licensing information for third-party material.
4. Review language, links, accessibility, and age appropriateness.
5. Submit a pull request that explains the learning objective and curriculum connection.

For curriculum summaries, start from the existing landing and shared template. Preserve the Big Ideas, Curricular Competencies, and Content sections, explicit program labels, and stable local IDs. Use the same committed format for each bounded content workstream. Contributors should fill their assigned entries and update their grade indexes, leaving shared format and central-index updates to a coordinator.

Changes to the repository-wide organization or naming conventions should update both this README and [AGENTS.md](AGENTS.md) in the same pull request.

## Agent Guidance

Automated coding agents must follow the repository instructions in [AGENTS.md](AGENTS.md).
