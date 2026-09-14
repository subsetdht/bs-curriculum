# British Columbia K-12 Curriculum Resources

This repository organizes British Columbia K-12 curriculum information alongside learning resources and educational tools. Its purpose is to help families and educators find material that supports specific curriculum expectations and student learning outcomes.

## Scope

Content in this repository should:

- support learners from Kindergarten through Grade 12;
- align with the current British Columbia curriculum;
- identify the grade, subject, and curriculum expectation it supports;
- be age-appropriate, accessible, and suitable for educational use; and
- include a reliable source or attribution when content is not original.

This is an independent educational project. It is not affiliated with or endorsed by the Government of British Columbia or any school district. Official curriculum requirements should always be verified against the [BC Curriculum](https://curriculum.gov.bc.ca/) website.

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

Each grade directory has the same four categories. For example:

```text
01-Grade-1/
|-- Curriculum/
|-- Resources/
|-- Tools/
`-- Additional-Content/
```

- **Curriculum** contains curriculum summaries or references organized by subject and learning standard.
- **Resources** contains lessons, exercises, readings, media, and other material tied to a curriculum expectation.
- **Tools** contains applications, templates, scripts, or interactive aids tied to a curriculum expectation.
- **Additional Content** contains useful enrichment material that does not map directly to a curriculum expectation.

Within each category, organize content by subject when multiple subjects are present.

Empty category directories contain a `.gitkeep` placeholder so they are included in Git. Remove the placeholder when adding content to that directory.

## Content Requirements

Every resource or tool must include enough context for a reader to understand its educational purpose. At minimum, document:

- grade and subject;
- related curricular competency or content expectation;
- learning objective;
- prerequisites or required materials;
- instructions for use;
- source and license, where applicable; and
- the date on which external curriculum alignment was last verified.

If an item has no direct curriculum association, place it under `Additional-Content` and describe its intended enrichment value.

Do not commit copyrighted material unless its license permits redistribution. Prefer links to authoritative sources when redistribution rights are unclear, and never include student personal information, credentials, or private assessment data.

## Contributing

1. Create or update content in the appropriate grade, subject, and category.
2. Confirm curriculum alignment using an authoritative source.
3. Add attribution and licensing information for third-party material.
4. Review language, links, accessibility, and age appropriateness.
5. Submit a pull request that explains the learning objective and curriculum connection.

Changes to the repository-wide organization or naming conventions should update both this README and [AGENTS.md](AGENTS.md) in the same pull request.

## Agent Guidance

Automated coding agents must follow the repository instructions in [AGENTS.md](AGENTS.md).
