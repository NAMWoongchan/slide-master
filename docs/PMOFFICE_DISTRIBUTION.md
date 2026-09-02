# PMOffice Distribution Workflow

## 1. Repository relationship

| Name | Role |
|---|---|
| `origin` | The PMOffice Fork: `https://github.com/NAMWoongchan/slide-master.git` |
| `upstream` | The source repository: `https://github.com/byungjunjang/slide-master.git` |
| `main` | Protected distribution baseline. |
| `pmoffice-v1` | Working branch for reviewed PMOffice changes. |

## 2. Change and review flow

1. Start from a clean `pmoffice-v1` branch based on `origin/main`.
2. Review the diff, license notices, source attribution, links, and sensitive
   information.
3. Create a local commit only for approved files.
4. Before any Push, Pull Request, Merge, Release, or GitHub Pages action,
   report the target and public impact and obtain approval.
5. Push the working branch, review a Pull Request into `main`, and verify the
   merged result before a release.

## 3. Release and upstream maintenance

- Create `v1.0.0` only after the approved `main` commit includes the intended
  PMOffice documentation and any validated brand assets.
- Before importing updates, compare `origin/main` and `upstream/main`.
- Perform upstream synchronization in a separate branch. Do not force-push,
  rewrite history, or overwrite PMOffice-specific documentation without review.

## 4. Publication boundary

Do not publish customer materials, personal data, `.env` files, API keys,
passwords, authentication tokens, or assets whose reuse rights are unclear.
The PMOffice contribution boundary is defined in
[`NOTICE.md`](../NOTICE.md) and
[`PMOFFICE_COPYRIGHT.md`](PMOFFICE_COPYRIGHT.md); upstream license terms remain
in force.
