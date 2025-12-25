# 🏡 Homepage Configuration

A complete [Homepage](https://github.com/gethomepage/homepage) dashboard configuration for managing your entire homelab. It provides real-time monitoring, media server integrations, automation tools, and quick access to all your self-hosted services.

## 📸 Screenshots

#### <p align="center"> Media Details Tab

![Media Details](/assets/Homepage-MediaDetails.png)
_Media services with live streaming statistics and recently added content_

#### <p align="center"> Server Details Tab

![Server Details](/assets/Homepage-ServerDetails.png)
_System monitoring, management, and various utilities_

---

### 📋 Prerequisites

- [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-22-04) are installed.
- [Homepage](https://github.com/gethomepage/homepage) container running.
- Docker socket access configured (see [Homepage Wiki](https://gethomepage.dev/latest/installation/docker/#using-docker-socket-with-remote-hosts))

---

### 🚀 Installation

1. **Clone this repository**

   ```bash
   git clone https://github.com/TheKevinatorX/Homepage.git
   cd homepage-config
   ```

2. **Update variables**

   Modify the provided `env.sample` [file](env.sample) with your values.

   - IP addresses (`{{HOMEPAGE_VAR_LOCAL_IP}}`)
   - Domain names (`{{HOMEPAGE_VAR_DOMAIN_NAME}}`)
   - API keys and tokens (`{{HOMEPAGE_VAR_CONTAINER_API}}`)
   - Once you replace all environment variables with your specific values, rename the file to `.env` | **Important!** ⚠️

3. **Restart Homepage**
   ```bash
   docker restart homepage
   ```

> **Security Warning:** Never commit your `.env` file or any file containing API keys, passwords, or sensitive information to a public repository!

---

## 📁 Files Included

| File                 | Description                                                       |
| -------------------- | ----------------------------------------------------------------- |
| `services.yaml`      | Service definitions, widgets, and integrations for all containers |
| `settings.yaml`      | General Homepage settings and appearance configuration            |
| `widgets.yaml`       | Dashboard widgets (search, datetime, weather, etc.)               |
| `custom.js`          | Custom JavaScript for additional customization                    |
| `docker-compose.yml` | Example Docker Compose setup (optional)                           |
| `.env.example`       | Template for environment variables                                |
| `/images/`           | Custom icons and background images                                |

---

## ✨ Features

This configuration includes widgets and integrations for:

**Media Services**

- Plex & Jellyfin media servers with Tautulli statistics
- Radarr, Sonarr, and Bazarr for automated media management
- Overseerr for media requests
- Immich for photo management
- Custom title card generation and trailer management

**System Monitoring**

- Real-time CPU, memory, and disk usage via Glances
- Network device monitoring with NetAlertX
- Container health tracking with Komodo
- Service uptime monitoring with Uptime Kuma
- Server statistics with Beszel

**Homelab Management**

- Traefik reverse proxy dashboard
- Authentik single sign-on integration
- Cloudflare tunnel status
- Docker log viewing with Dozzle
- Container management via Portainer and Komodo

**Automation & Utilities**

- n8n workflow automation
- Subscription tracking with Wallos
- Recipe management with Mealie
- Web content collection with Karakeep
- Developer tools and VS Code server

**Calendar Integrations**

- Upcoming TV shows and anime releases
- Recently added media from Tautulli
- Custom iCal feed support

## 🔧 Service Categories

<details>
<summary><b>System Monitor (4 widgets)</b></summary>

> Monitor CPU, RAM, processes, and disk usage in real-time with Glances integration.

- CPU usage (Glances)
- Memory usage (Glances)
- Running processes (Glances)
- Hard drive statistics (Glances)
</details>

<details>
<summary><b>Media Services (8 services)</b></summary>

> Complete media streaming and management ecosystem with automated downloading and organization.

- Plex (Tautulli integration)
- Plexamp (Tautulli Music)
- Jellyfin
- TitleCardMaker
- Immich
- qBittorrent
- SABnzbd
</details>

<details>
<summary><b>Homelab Management (13 services)</b></summary>

> Essential infrastructure tools for monitoring, authentication, networking, and container management.

- Beszel (system statistics)
- NetAlertX (network monitoring)
- Synology NAS
- Authentik (SSO)
- Traefik (reverse proxy)
- Komodo (container management)
- Uptime Kuma
- Speedtest Tracker
- Cloudflared
- Karakeep
- Wallos
- Filebrowser
</details>

<details>
<summary><b>Arr Services (6 services)</b></summary>

> Automated media acquisition and organization suite for movies, TV shows, anime, and subtitles.

- Prowlarr
- Radarr
- Sonarr (TV Shows)
- Sonarr (Anime)
- Bazarr
- Overseerr
</details>

<details>
<summary><b>Utility Containers (13 services)</b></summary>

> Productivity and development tools for documentation, automation, recipes, and homelab workflows.

- Dozzle
- Notifiarr
- Code Server
- IT-Tools
- Trailarr
- MkDocs
- Metadata Manager
- n8n
- Portainer
- DAPS
- Wizarr
- Mealie

</details>

<details>
<summary><b>Media Calendars (4 widgets)</b></summary>

> Track upcoming releases and recent additions across your media library with integrated calendar views.

- Upcoming TV Shows
- Upcoming Anime
- Recently Added Shows
- Recently Added Movies
</details>

<details>
<summary><b>Quick Links (20 bookmarks)</b></summary>

> Frequently accessed websites and external services for productivity, entertainment, and daily use.

- Homepage
- Todoist
- Calendar
- Reddit
- YouTube
- Mail
- Drive
- Messages
- Keep
- Github
- Gemini
- Claude
- Grok
- ChatGPT
- Synology
- Discord
- Trakt
- Pastebin
- Photopea
- Amazon
- eBay

</details>

---

## 🔗 Useful Resources

- [Homepage GitHub Repository](https://github.com/gethomepage/homepage)
- [Homepage Documentation](https://gethomepage.dev/)
- [Widget Configuration Guide](https://gethomepage.dev/latest/widgets/)
- [Service Integration Guide](https://gethomepage.dev/latest/configs/services/)

---

### 📝 License

This configuration is provided as-is for personal use. Please respect the licenses of individual services and the Homepage project. See [LICENSE](LICENSE) for details.

---
