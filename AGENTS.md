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
- Use `Curriculum`, `Resources`, `Tools`, and `Additional-Content` as category directory names.
- Organize category content by subject when more than one subject is present.
- Use descriptive kebab-case names for new files and directories unless a local convention requires otherwise.
- Keep each resource or tool close to the curriculum material it supports.
- Place content without a direct curriculum mapping in `Additional-Content`.
- Prefer Markdown and other open, portable formats for written material.

## Content Standards

- State the target grade, subject, learning objective, and relevant curriculum expectation.
- Cite authoritative curriculum sources and record the alignment verification date.
- Identify prerequisites, required materials, and instructions for use.
- Provide attribution and license details for third-party content.
- Use clear, inclusive, age-appropriate language.
- Add meaningful alternative text for images and transcripts or summaries for audiovisual material where practical.
- Do not include student personal information, secrets, credentials, or private assessment data.
- Do not reproduce third-party material unless its license permits redistribution.

## Working Practices

1. Read the nearest documentation and inspect adjacent content before making changes.
2. Keep changes focused on the requested grade, subject, or tool.
3. Preserve established naming, formatting, and metadata patterns.
4. Verify external links and curriculum claims against authoritative sources when network access is available.
5. Run the narrowest relevant validation available, including tests, linters, link checks, or build commands.
6. Report validation that could not be performed and avoid claiming unverified curriculum accuracy.

Do not reorganize unrelated content, introduce a new repository-wide structure, or add major dependencies without explaining the need in the pull request. When changing structural conventions, update this file and the root README together.

## Review Checklist

Before completing a change, confirm that:

- content is in the correct grade, subject, and category;
- the curriculum relationship is explicit and current;
- sources and licenses are documented;
- language and activities are appropriate for the target learners;
- links and local references work;
- no private or sensitive information is present; and
- relevant validation has passed.
