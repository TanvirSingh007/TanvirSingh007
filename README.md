```console
$ whoami
Tanvir Singh — software engineer, Ludhiana
```

I spend most of my time in code I didn't write, on enterprise products older than my
time at the company. The reports come in vague, the people who wrote the thing left
years ago, and the fix itself is rarely the hard part. Working out where the fix
belongs is. I didn't expect to enjoy that as much as I do.

A lot of it has turned into getting agents to do it alongside me, though not the part
everyone means by that. The models are fine. What they can't do is build a two-decade-old
desktop app that only compiles on Windows, or debug an iOS client that needs a physical
iPad plugged in somewhere. So I spend my time on the plumbing: VMs an agent can drive,
hardware it can reach, the context it should read before it touches anything.

The bit I actually care about is whether I can trust what comes back. An agent will
write a regression test that passes against the broken code and tell you it's done,
which is worse than useless. So nothing counts until I've watched the test fail first.
That rule has caught me more often than I'd like to admit.

Probably the same instinct is why there's a homelab, and why it got out of hand. It
runs on Unraid, every service is a compose stack in git, and it does considerably more
than it needs to: GitLab, Appwrite, Nextcloud, Home Assistant, Jellyfin, Bitwarden,
all sitting behind nginx on an internal domain with cloudflared handling the few things
that need to be reachable from outside.

The two I like most are Frigate, doing camera detection on the Intel iGPU, and Immich,
running embedding search across the photo library. Both do real inference on hardware
in my house instead of someone else's API, which I find more satisfying than it
probably deserves. I'd also rather my photos and passwords lived on a machine I can
see. Mostly, though, you don't really understand a system until you've had to restore
it at an inconvenient hour, and the homelab has given me plenty of those.

Day to day that means Python, Ruby, TypeScript, C#, Go, Scala and a fair bit of C++ and
Objective-C when something old breaks. Rails and Postgres for most things with a
database behind them. Docker, GitHub Actions, Jenkins, Terraform and self-hosted
runners for everything that builds it. Claude Code and MCP for the agent side.

There's a longer version of all this, including the homelab, at
**[tanvir.sh](https://tanvir.sh)**, which answers `curl` too if you'd rather read it in
a terminal.

[linkedin](https://www.linkedin.com/in/tanvir-singh-b21032236/) ·
[singhtanvir032@gmail.com](mailto:singhtanvir032@gmail.com)
