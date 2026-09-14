# AGENTS.md

This file defines repository-wide instructions for automated coding agents. More specific `AGENTS.md` files may be added in subdirectories as the repository grows; the closest applicable file takes precedence.

## P0 Mandate: Commit Messages

This policy is mandatory and takes precedence over conflicting instructions in any nested file or external workflow.

- Never add attribution footers to commit messages. This includes `Co-authored-by`, `Generated-by`, `Assisted-by`, or similar statements crediting a person, agent, model, or tool.
- Keep commit messages relatively terse while including the details needed to identify the purpose and material contents of the commit.
- Use a concise subject line. Add a short body only when the subject cannot adequately describe the relevant changes.

## Project Intent

Maintain a clear, trustworthy collection of British Columbia K-12 curriculum references, aligned learning resources, and educational tools. Optimize for curriculum traceability, age appropriateness, accessibility, and ease of navigation.

## Repository Conventions

- Use `00-Kindergarten` and `01-Grade-1` through `12-Grade-12` for top-level grade directories.
- Keep the sorting prefix two digits (`00` through `12`) so alphabetical sorting follows grade order. Preserve the familiar grade label after the prefix; `00` is a sorting key for Kindergarten, not a grade designation.
- Use `00-Curriculum`, `01-Resources`, `02-Tools`, and `03-Additional-Content` as category directory names in every grade directory. Keep these two-digit prefixes so alphabetical sorting preserves this category order.
- Organize category content by subject when more than one subject is present.
- Use descriptive kebab-case names for new files and directories unless a local convention requires otherwise.
- Keep each resource or tool close to the curriculum material it supports.
- Place content without a direct curriculum mapping in `03-Additional-Content`.
- Prefer Markdown and other open, portable formats for written material.

## Curriculum Record Format

- Follow [curriculum-format.md](curriculum-format.md) and [templates/curriculum-record.md](templates/curriculum-record.md) for curriculum summaries. Markdown with YAML front matter is the maintained source; do not create a parallel data copy.
- Use a curriculum-category `README.md` for grade navigation, a subject/course `README.md` as its stable landing, and an adjacent `curriculum.md` for the actual record. Put distinct courses or program variants in named subdirectories beneath the subject.
- Keep the required sections: Scope and use, Big Ideas, Curricular Competencies, Content, Elaborations and boundaries, and Sources and rights.
- Preserve stable repository record IDs and `BI-`, `CC-`, and `C-` item IDs. These are not official BC standard codes. Every summarized item needs an authoritative source locator.
- Distinguish the target grade from the source's grade band. Do not invent separate content where a curriculum integrates content from other subjects, or treat all senior courses as compulsory.
- Record actual source review dates; do not invent curriculum revision dates. A working URL or an empty page shell does not establish alignment.

## Navigation and References

- Keep [curriculum-index.md](curriculum-index.md) as the central area/grade/program navigator, linked prominently from the root README. It indexes records; it is not a second curriculum data store.
- Use only `K`, `1`, `2`, ..., `12` for ordinary grade-selector labels, without a `Grade` prefix. Preserve source-defined entry labels such as `6T`, `7T`, `CLE`, and `CLC` where applicable; they are not extra grades. Group links inline in school order.
- Main catalog links target real landing pages, including pending entries. Distinguish landing coverage from written-summary coverage, and official-source links from repository content. Never link to a nonexistent `curriculum.md`.
- Every grade overview lists its landings and content status. Add program entry points and direct links to Big Ideas, Curricular Competencies, and Content only where corresponding records exist. Preserve the canonical section anchors documented in the format guide.
- Include breadcrumbs back to the central index and grade overview, plus section quick links, in every curriculum record. Resolve relative paths for the actual nesting depth.
- Reference a record as a descriptive Markdown link. Reference an item with the visible label `<Subject/course> <grade>: <item ID>` and the record path plus its lowercase item anchor, for example [Mathematics 1: C-01](01-Grade-1/00-Curriculum/mathematics/curriculum.md#c-01).
- Preserve the canonical `<record_id>#<lowercase-item-id>` in structured mappings. A bare `C-01`, `CC-01`, or `BI-01` is ambiguous outside its record; never present it as an official BC code.
- When adding, moving, or retiring a record, update its landing status/links, grade index, central Written summaries entry, and inbound references together. Keep established landing URLs stable. In parallel work, the grade owner updates local navigation and reports central-index changes to the coordinator.
- Follow actual source grade/course/transition choices. Do not generate official URLs by guessing that all subjects share the same grade routes, or treat named senior courses as numbered grades.

## Filling Landing Pages

- The main BC catalog entry points are bootstrapped. Work from the existing landing and fill the assigned entry rather than creating duplicate subject folders or another navigation structure.
- Use [templates/curriculum-landing.md](templates/curriculum-landing.md) for new course landings and the record template for actual curriculum summaries. Landings are navigation documents, not empty curriculum records.
- For a core entry, review the source and create the adjacent `curriculum.md`. For a course-list entry, inventory the actual courses and create named course folders first. Do not infer entry type solely from grade.
- Preserve separate `transition-6t` and `transition-7t` entries under Grades 6 and 7. Review their program applicability independently from the regular entries.
- Keep grade-independent career entries and Additional Offerings linked through [curriculum-special-entries.md](curriculum-special-entries.md) until their placement and scope are established. Do not assign a guessed grade or equate BC Additional Offerings with unmapped enrichment.
- Use honest landing statuses: `Needs summary`, `Needs course inventory`, `Summary draft`, or `Summary available`, with explicit placement/inventory statuses for special entries. `Summary available` requires a corresponding `source-checked` record; an empty template or successful URL request is not sufficient.
- When filling an entry, document program suitability, document/source language, grade bands, source locators, rights, and the actual alignment review date. A catalog-capture date is not an alignment date.
- Update the landing, grade/program navigation, and central written-summary coverage when content is ready. Retain existing curriculum file paths and item IDs.

## Program Coverage

- This is a BC-wide reference collection. Keep district and school implementation guidance separate from provincial expectations.
- Prioritize the English-language program when sequencing work, while designing and maintaining explicit coverage for other programs. Do not present English-only coverage as complete BC coverage.
- Declare `programs` on every curriculum record using the format guide's explicit labels: `english-language`, `early-french-immersion`, `late-french-immersion`, and `francophone`. Include only applicability supported by sources.
- Share records for genuinely shared expectations. Keep English Language Arts, French Immersion Language Arts, Francophone language arts, and Core French distinct.
- Distinguish document language, official source language, and classroom language of instruction. English summaries may describe immersion curricula without becoming English-language instructional requirements.
- Label resources and tools independently for program and language suitability. Shared curriculum alignment alone does not make an English resource suitable for French Immersion.
- Make missing curriculum summaries, program coverage, and language editions visible separately from landing-page coverage. Do not infer Early/Late Immersion equivalence or Francophone applicability.

## Content Standards

- State the target grade, subject, learning objective, and relevant curriculum expectation.
- Cite authoritative curriculum sources and record the alignment verification date.
- Identify prerequisites, required materials, and instructions for use.
- Provide attribution and license details for third-party content.
- Use clear, inclusive, age-appropriate language.
- Add meaningful alternative text for images and transcripts or summaries for audiovisual material where practical.
- Do not include student personal information, secrets, credentials, or private assessment data.
- Do not reproduce third-party material unless its license permits redistribution.
- Use original, source-linked curriculum summaries rather than bulk copies, line-by-line rewrites, or full translations of official documents. Do not assume Crown-copyright curriculum is covered by the Open Government Licence.
- Preserve First Peoples perspectives within their curriculum subjects and respect permissions for community-specific knowledge and cultural works.

## Working Practices

1. Read the nearest documentation and inspect adjacent content before making changes.
2. Keep changes focused on the requested grade, subject, or tool.
3. Preserve established naming, formatting, and metadata patterns.
4. Verify external links and curriculum claims against authoritative sources when network access is available.
5. Run the narrowest relevant validation available, including tests, linters, link checks, or build commands.
6. Report validation that could not be performed and avoid claiming unverified curriculum accuracy.

Do not reorganize unrelated content, introduce a new repository-wide structure, or add major dependencies without explaining the need in the pull request. When changing structural conventions, update this file and the root README together.

For parallel curriculum population, use the bootstrapped landings, reviewed Grade 1 records, and the same committed format as the starting point. Each workstream fills its assigned entries and updates their landings and grade overviews; a coordinator owns shared format and root navigation changes. Report source-access failures and program gaps rather than inventing requirements or silently narrowing coverage.

## Review Checklist

Before completing a change, confirm that:

- content is in the correct grade, subject, and category;
- the curriculum relationship is explicit and current;
- program applicability and document/source languages are explicit and not conflated;
- grade bands, course options, and local implementation are distinguished;
- sources and licenses are documented;
- language and activities are appropriate for the target learners;
- links and local references work;
- central and grade navigation match actual coverage, and item links resolve to stable anchors;
- no private or sensitive information is present; and
- relevant validation has passed.
