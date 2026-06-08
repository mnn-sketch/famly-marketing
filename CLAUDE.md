
cd famly-marketing

mkdir -p scripts automations tools experiments
touch scripts/.gitkeep automations/.gitkeep tools/.gitkeep experiments/.gitkeep

cat > CLAUDE.md << 'EOF'
# CLAUDE.md — Famly Marketing Repo

This is the Famly marketing team's shared repository for scripts, automations, tools, and internal frontends.

## About Famly

Famly is a childcare management SaaS company. Markets: UK, US, DACH. The marketing team builds internal tools, automations, and data pipelines to support campaigns across these markets.

## Stack

- Python 3.12+ for scripts and automations
- Svelte for internal frontends (deployed to famly.tools)
- GitHub Actions for scheduled jobs and CI/CD
- Notion API for task and content management
- HubSpot for CRM data
- Google Sheets / Google Drive for shared data
- Anthropic API (claude-sonnet-4-6) for AI-powered scripts

## Repo structure

- /scripts — one-off and utility Python scripts
- /automations — scheduled Python scripts that run regularly
- /tools — Svelte frontends for internal use
- /experiments — hackathon builds, prototypes, rough work. Don't depend on anything in here.

## Conventions

- Always use a virtual environment (venv) for Python work
- Never commit API keys or secrets — use environment variables
- Put a README.md in each subfolder explaining what it does
- Experimental work goes in /experiments — keep main folders clean

## Do not touch

- GitHub Actions workflow files unless you know what you're doing
- Other people's subfolders without checking with them first

## Tone

This is a marketing team, not an engineering team. Scripts should be readable and well-commented. Prefer simple and working over clever and fragile.
