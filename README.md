```console
$ whoami
Tanvir Singh — software engineer, Ludhiana

$ cat interests.txt
ai agents · infrastructure · self-hosting

$ curl tanvir.sh
```

## AI agents

Almost none of the interesting work is the model itself.

Most agents are useless on the systems I care about, because those systems cannot be
reached from a container with a text editor. A two-decade-old desktop app builds on
Windows. An iOS client needs real hardware to install and debug on. So I build the
harnesses: provisioning and driving Windows VMs, instrumenting physical devices,
handing an agent the same access a person would have.

The other half is trust. An agent will happily write a regression test that passes
against the broken code, which proves nothing at all. So every test has to be observed
failing before the fix goes back in. Without that check the throughput is worthless,
because you cannot tell a fixed bug from a closed one.

Somewhere between those two is the boring, underrated part: the context an agent reads
before it touches a codebase. Most of the quality comes from there.

## Infrastructure

Build systems, CI, self-hosted runner fleets, containers. I like the work where the
feedback loop is slow and the failure modes are annoying, because that is usually where
nobody else wants to go.

I hold the general position that you do not understand a system until you have operated
one. Reading about backups is not the same as restoring one.

## The homelab

Which is why there is a homelab, and why it has grown well past what it needed to be.
Everything is reproducible from a git repository. No snowflake containers, no
configuration that exists only in my head.

| | |
|---|---|
| **host** | Unraid, Portainer-managed compose stacks |
| **ingress** | nginx on an internal domain, cloudflared tunnels for a subset |
| **scm / ci** | self-hosted GitLab CE |
| **platform** | Appwrite, self-hosted, multi-container |
| **vision** | Frigate, continuous detection on the Intel iGPU |
| **photos** | Immich with a dedicated ML container on pgvector |
| **also** | Home Assistant · Jellyfin · Nextcloud · Bitwarden · PostgreSQL · Valkey |

The two I enjoy most are Frigate and Immich, because both do real inference on hardware
I already own rather than on somebody's API. Frigate gets the iGPU passed through for
decode and detection; doing that on the CPU pins the machine permanently. Immich runs
embedding search over the photo library, which is the same shape as a production
retrieval stack at house scale.

Longer write-up: **[tanvir.sh/homelab](https://tanvir.sh/homelab/)**

## What I work with

**agent tooling:** Claude Code · OpenCode · MCP servers · harness design

**languages:** Python · Ruby · TypeScript · C# · Go · Scala · C++ · Objective-C · SQL · Bash

**backend:** Rails · REST · GraphQL · PostgreSQL · MySQL · MongoDB · Redis · RabbitMQ

**platform:** GitHub Actions · Jenkins · Docker · Kubernetes · Terraform · AWS · nginx · Unraid

## Elsewhere

- [tanvir.sh](https://tanvir.sh), which answers `curl` too
- [linkedin](https://www.linkedin.com/in/tanvir-singh-b21032236/)
- [singhtanvir032@gmail.com](mailto:singhtanvir032@gmail.com)
