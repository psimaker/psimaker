<div align="center">

# Hi, I'm Umo

I run Linux boxes, break things, fix them, then automate the boring parts.

Switzerland · DevOps / Platform Engineering · Self-hosting

</div>

---

I spend a lot of time around servers, containers, monitoring, networking, and self-hosted tools.

Most of what I build comes from something I actually needed.

I'm currently going deeper into Kubernetes and building real AI agents.

---

## Stuff I built

### [VaultSync](https://github.com/psimaker/vaultsync)

An iOS app for syncing Obsidian vaults through Syncthing.

I built this because I wanted a self-hosted way to keep my notes on iPhone and iPad without moving everything into iCloud, Dropbox, or another managed sync service.

- Available on the [App Store](https://apps.apple.com/app/vaultsync/id6761845197)
- Built with Swift
- Designed around Syncthing and Obsidian
- Includes a small Docker-based helper setup
- Has CI, docs, screenshots, and a proper release flow

---

### [Homelab](https://github.com/psimaker/homelab)

My home infrastructure. Hosts [loogi.ch](https://loogi.ch) in production.

Two tiers, deliberately split: a Kubernetes platform for new workloads, a Docker Compose dataplane for the stateful giants. Replatforming Plex, Nextcloud and the rest to k8s would buy nothing and cost weeks, so they stay on Compose with proper config-mgmt and observability around them.

Some of the stack:

- k3s + Cilium + Flux v2 (GitOps)
- OpenTofu + Ansible (Hetzner edge + airbase home)
- Cloudflare Tunnel + Traefik + cert-manager
- Self-hosted Headscale (own Tailscale control-plane) and Pocket-ID (OIDC)
- kube-prometheus-stack + Loki + Tempo + Beszel — internal-only
- SOPS + age for secrets, encrypted in the public repo
- restic 3-2-1 backup (Hetzner Storage Box + Backblaze B2), weekly restore test
- Renovate self-hosted, auto-merge on patch+minor
- Tier-2 still runs: Plex, *arr, Nextcloud-AIO, Immich, Paperless, Vaultwarden, Gitea, n8n, Syncthing, ntfy, …

Documented end-to-end: 13 ADRs, runbooks, and post-mortems for the things that actually broke.

It's not meant to be a perfect template. It's more of a working setup that reflects how I actually run things.

---

### [Twitter/X Spy Link Remover](https://github.com/psimaker/twitter-x-spy-link-remover)

A small userscript that skips Twitter/X `t.co` tracking redirects and opens the real link directly.

No backend. No external requests. Just vanilla JavaScript doing one job.

Works with Tampermonkey / Violentmonkey.

---

## Open source

I contribute fixes when I run into something broken or annoying enough to investigate.

- [Nextcloud Server PR #59317](https://github.com/nextcloud/server/pull/59317)

---

## Things I'm interested in

- Linux servers
- Self-hosting
- Kubernetes
- Containers
- Monitoring
- Automation
- Privacy-focused tools
- Practical AI tooling
- Open-source infrastructure

---

<div align="center">

Automate first. Regret later. Fix properly after coffee.

</div>
