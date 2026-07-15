# HelpMe — Emergency Lifeline

Umbrella repository for the **HelpMe** emergency-response system by team **FivesFromF**.

HelpMe identifies people in distress (via AI face recognition, NFC tags, or QR codes) so responders can reach their medical profile and next-of-kin within the "golden hour".

## Structure

This repo aggregates the component repositories as **git submodules**:

| Submodule | Stack | Description |
| :-- | :-- | :-- |
| [`help_me_context`](https://github.com/FivesFromF/help_me_context) | Docs | Vision, system design, and functional requirements |
| [`help_me_backend`](https://github.com/FivesFromF/help_me_backend) | TypeScript Lambdas + Python FastAPI | API, AI face service, Terraform infra |
| [`help_me_app`](https://github.com/FivesFromF/help_me_app) | Flutter | Mobile app (face / NFC / QR capture) |
| [`help_me_web`](https://github.com/FivesFromF/help_me_web) | Next.js 16 | `admin-dashboard/` and `landing-page/` |
| [`help_me_ai_face_poc`](https://github.com/FivesFromF/help_me_ai_face_poc) | Python | Face-recognition proof-of-concept |

## Getting started

Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/FivesFromF/help_me.git
```

If you already cloned without `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

Pull the latest for every submodule:

```bash
git submodule update --remote --merge
```

After advancing a submodule to a new commit, commit the updated pointer here:

```bash
git add <submodule> && git commit -m "chore: bump <submodule>"
```

See each submodule's own README for build/run instructions.
