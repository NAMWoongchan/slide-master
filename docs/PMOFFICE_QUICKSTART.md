# PMOffice Quick Start

Copyright (c) 2026 피엠오피스 남웅찬 (WoongChan NAM / PMOffice)

PMOffice-authored documentation; upstream software remains under its original
licenses.

## 1. Prerequisites

| Requirement | Check |
|---|---|
| Git | `git --version` |
| Python 3.10 or later | `python --version` |
| ChatGPT Desktop with Work locally, or Codex Local | Open the cloned folder as the local project folder. |
| PowerPoint | Recommended for reviewing the exported editable PPTX. |

For Windows installation guidance, see
[`windows-installation.md`](windows-installation.md). Do not place passwords,
API keys, or tokens in this document, a prompt, or Git.

## 2. Clone and install

```powershell
git clone https://github.com/NAMWoongchan/slide-master.git
cd slide-master
python -m pip install -r requirements.txt
```

Confirm that `README.md` and `AGENTS.md` are present. The default branch is
`main`; keep personal source material and generated decks under `projects/` so
they remain excluded by the repository `.gitignore` policy.

## 3. Open in ChatGPT Desktop or Codex

1. Create or open a local project in ChatGPT Desktop.
2. Add the cloned `slide-master` folder and set it as the primary folder.
3. Start a Work locally or Codex Local task.
4. Ask the agent to read `README.md`, `AGENTS.md`, and the applicable workflow
   before it creates a deck.

## 4. First editable PPTX check

1. Put approved source files under `projects/<project-name>/`.
2. Request a deck using the repository workflow.
3. Open the resulting PPTX in PowerPoint.
4. Verify that text and shapes can be selected and edited individually.

> Note: The PMOffice Brand Preset is available at
> [`.claude/skills/ppt-master/templates/brands/pmoffice/`](../.claude/skills/ppt-master/templates/brands/pmoffice/).
> Include this exact workspace path in the initial request when the PMOffice
> identity is required. Do not infer a brand from its name alone.

```text
.claude/skills/ppt-master/templates/brands/pmoffice/를 사용해서 프로젝트 관리 교육용 PPT를 만들어 줘.
```

## 5. Troubleshooting

| Symptom | Safe first check |
|---|---|
| Python command fails | Run `python --version` and use the Windows installation guide. |
| Dependencies fail | Run `python -m pip install -r requirements.txt` and retain the error output. |
| Generated files appear in Git status | Confirm they are under `projects/` and review `.gitignore`; do not delete files automatically. |
| Git remote is unclear | Run `git remote -v`; `origin` should be the PMOffice Fork and `upstream` the source repository. |
