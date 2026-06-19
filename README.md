# Home Improvement (`home-improvement`)

![Build Status](https://github.com/Natur3-Boy/home-improvement/actions/workflows/deploy.yml/badge.svg)

Centralized, version-controlled documentation platform for residential infrastructure engineering, automation setups, and land management. Built using Markdown, rendered via MkDocs Material, and continuously deployed using GitHub Actions.

## Quickstart (Local Development)

To run the site locally, edit documentation, and preview changes in real time:

```bash
# 1. Setup virtual environment
python3 -m venv venv
source venv/bin/activate

# 2. Install dependencies
pip install mkdocs-material mkdocs-mermaid2-plugin

# 3. Spin up the local development server
mkdocs serve
