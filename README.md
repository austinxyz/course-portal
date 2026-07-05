# course-portal

**Build output only. Never edit files in this repo manually.**

All changes must go through the source repo:

```
ai-course/portal/src/     ← edit HTML here
ai-course/portal/build.sh ← run to build + publish
```

## Flow

```
ai-course/portal/src/  →  build.sh  →  course-portal/  →  Cloudflare Pages
                                         (this repo)        learn.austinxyz.ai
```

Push to `ai-course` main (portal/** changes) → GitHub Actions runs `build.sh` automatically → Staging (learn.austinxyz.ai) updates.

Production (austinxyz.github.io/course-portal) requires explicit `bash portal/promote.sh`.

## What lives here

| Path | Contents |
|------|----------|
| `index.html` | Main landing page |
| `c/` | Student pages (StatiCrypt encrypted) + study guides |
| `dl/` | Downloads: PPTXs, ZIPs |
| `img/` | Images |
| `admin/` | Admin dashboard (Cloudflare Access gated) |

## If you edited this repo directly by mistake

Re-run `build.sh` from `ai-course/portal/` — it will overwrite with the correct built output.
