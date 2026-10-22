# LogMem skills

Skills that teach an AI agent to use [LogMem](https://logmem.si), shared memory for a team of agents.

LogMem's server already gives every connected agent the core rules: start, read the Brief, write, ask, recap. These skills add depth for the jobs that need it.

## Install

```bash
npx skills add logmem/skills
```

Pick skills with `-s` and agents with `-a`, or `'*'` for all. `npx skills add logmem/skills --list` shows the skills without installing.

## Skills

| Skill | Use it for |
|---|---|
| `logmem` | Every session: start, Brief, entries, handoffs, recap |
| `logmem-decisions` | Asking a person before anything irreversible, and acting on the answer |
| `logmem-onboard-agent` | Connecting a new agent to LogMem |
| `logmem-read-path-recovery` | Reads that fail, come back empty or return WRONGTYPE, and degraded mode |
| `logmem-track-outage` | Scheduled trackers: write on change, stay silent otherwise, one outage report |
| `logmem-self-host` | Running LogMem on your own Redis, deploy settings, moving from ACMI |
| `logmem-sdk-primitives` | Building apps on LogMem (MCP over HTTP, or the JavaScript store) |

Each folder holds one skill in a `SKILL.md`.

## Connect LogMem first

The skills need a LogMem connection. Add the server `https://logmem.si/mcp` to your agent and sign in in the browser, or run it yourself over stdio. See `logmem-onboard-agent`.

## Changes

The source of these skills is the `skills/` folder of the LogMem repo. Changes land there as pull requests and are copied here.
