# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an educational repository for the Duke Statistical Science Department's computing bootcamp for incoming PhD and MS students. The repository contains presentation slides and example materials covering reproducible research, version control, literate programming, and Duke Compute Cluster (DCC) usage.

## Architecture

### Repository Structure
- `slides/` - Quarto presentation slides (.qmd files) covering 5 main topics
- `examples/` - Sample R code and Quarto documents for hands-on exercises
- `examples/data/` - UN voting data used in examples
- R Project configuration in `bootcamp.Rproj`

### Key Technologies
- **Quarto** - Primary presentation format using revealjs
- **R** - Programming language for examples and data analysis
- **RMarkdown/Quarto** - Literate programming examples
- **Git/GitHub** - Version control instruction materials

## Common Development Commands

### Rendering Presentations
```bash
# Render individual slide presentation
quarto render slides/01_introduction_and_resources.qmd

# Render all slides
quarto render slides/

# Render example documents
quarto render examples/unvotes.qmd
```

### R Project
- Open `bootcamp.Rproj` in RStudio for proper project environment
- R code uses `=` for assignment (not `<-`)
- 2-space indentation configured in project

### Testing Examples
```bash
# Run R test script
Rscript examples/test.R

# Check for output file
ls examples/test-output.txt
```

## Slide Content Structure

Each slide deck follows consistent format:
- YAML header with revealjs format and custom styling
- Self-contained output for distribution
- Custom SCSS theme in `slides/custom.scss`
- Images stored in `slides/images/`

## Data Files

The `examples/data/` directory contains UN voting datasets:
- `un_votes.csv` - Country voting records
- `un_roll_calls.csv` - Roll call metadata  
- `un_roll_call_issues.csv` - Issue classifications

## Development Notes

- Presentations are designed for 2025 bootcamp
- Content builds from basic computing concepts to advanced cluster usage
- Examples demonstrate tidyverse and data visualization workflows
- Materials adapted from Shawn Santo, Mine Çetinkaya-Rundel, and Colin Rundel