---
name: technical-audit
description: "NEEDS A SECOND STEP. This is a placeholder: the real technical-audit skill (by younesbenallal) installs separately. Claude downloads it on first use, after you say yes, or see the README to install it now. Run a technical SEO audit of a website that keeps only checks that move results: crawl and index access, AI crawler access, canonicals, JavaScript rendering, cannibalization, internal links, speed, schema. Use when the user asks for a technical audit, a tech SEO check, a site health check, or why a site is not indexed or not cited by AI answers."
---

# technical-audit (install placeholder)

The real `technical-audit` skill is not installed yet. This file only installs it. It has no SEO method, so do not do the user's task with it.

The real skill lives in https://github.com/younesbenallal/seo-skills. That repo has no license, so this repo cannot bundle it and links to it instead.

## Steps

1. Tell the user, in one or two sentences: the `technical-audit` skill is a placeholder, and the real skill must be downloaded from github.com/younesbenallal/seo-skills. Ask for permission to install it. Do not continue without a yes.
2. Find the skills folder: the parent folder of the folder that holds this file. If this folder is a symlink, resolve it first (`realpath`). Call the result `SKILLS_DIR`.
3. Check `SKILLS_DIR/docs`. The real skill reads `../docs/credentials-and-tooling.md`. If `SKILLS_DIR/docs` exists and does not contain `credentials-and-tooling.md`, stop and ask the user before you write into it.
4. Run, with `SKILLS_DIR` filled in:

   ```bash
   TMP=$(mktemp -d)
   git clone --depth 1 https://github.com/younesbenallal/seo-skills "$TMP/younes"
   cp -R "$TMP/younes/technical-audit/." "SKILLS_DIR/technical-audit/"
   mkdir -p "SKILLS_DIR/docs"
   cp -R "$TMP/younes/docs/." "SKILLS_DIR/docs/"
   rm -rf "$TMP"
   ```

   The copy replaces this placeholder `SKILL.md` with the real one.
5. Check that `SKILLS_DIR/technical-audit/SKILL.md` no longer contains the words "install placeholder". If it still does, tell the user the install failed and show the error.
6. Tell the user to restart Claude Code (or start a new session) so the real skill loads, and then to ask their question again.

If the user says no, do the task without a skill and say that the result does not follow the `technical-audit` method.
