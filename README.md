# SlackData — data

A daily backup of [SlackData](https://slackdata.org), the ISA's open database of slackline gear,
made from its public API by the workflow in `.github/workflows/export.yml` (every day at 03:17
UTC, and on demand). Nothing here is edited by hand: the catalogue is edited on the site, and every
change is in its public log.

| Path | What |
|---|---|
| `data/<collection>.json` | the catalogue — webbings, weblocks, …, manufacturers, the ISA's certificates and warnings — in the same format as the seed files of the [SlackData repository](https://github.com/International-Slackline-Association/SlackData) |
| `data/changes.json` | the whole change log, oldest first, with the name each person shows on the site |
| `data/catalogue.json` | the catalogue version the export was taken at |
| `data/media/` | every photo, manual and logo the catalogue names; never deleted from here |

A day with no change makes no commit. `export_catalogue.py` is a copy of
[`export/export_catalogue.py`](https://github.com/International-Slackline-Association/SlackData/blob/main/export/export_catalogue.py)
in the SlackData repository — standard library only, no credentials.

**Erasure requests:** names in `changes.json` are the names people chose to show on SlackData. If
someone's name is removed there, this repository's history is rewritten to match (SlackData's
LIVE_EDITING_PLAN.md, D14).
