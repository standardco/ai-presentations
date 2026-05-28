# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a presentation slides repository for the **Standard Co 6 Month AI Series** (March–August 2026). It contains PPTX files for each monthly session. There is no application code, build system, or test suite.

## Repository Structure

- PPTX presentation files live at the repository root, named with the pattern: `Standard Co - <Topic> - <Month Day Year>.pptx`
- `README.md` tracks the schedule and links to each slide deck
- `.tool-versions` specifies Node.js 25.3.0 via asdf

## Working with PPTX Files

PPTX files are binary (zipped XML). To inspect contents without PowerPoint, unzip to a temp directory:

```
unzip -o "<file>.pptx" -d /tmp/pptx_scan/
```

Temporary PowerPoint lock files (`~$*.pptx`) are gitignored.

## Adding New Presentations

1. Add the PPTX file to the repository root following the existing naming convention
2. Update the schedule table in `README.md` with the date, topic, and file link
