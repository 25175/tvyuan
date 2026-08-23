# TVBox Aggregated Sources

Automatically aggregates TVBox movie and TV sources, updated hourly via GitHub Actions.

## Usage

### 📺 One-Click Configuration (Recommended)

Directly copy the address into TVBox/Yingshicang/FongMi clients. Collection sites are sorted by playback speed tests for an out-of-the-box experience:

```
https://tv.cc0cd.cc.cd
```

### 📺 Concise Version

Contains only collection sites (fixed top 10 fastest), no dependency on JAR, **real playback speed sorting** (m3u8 → segment download):

| Channel | Address |
|------|------|
| 🔗 Direct Link | `https://tv.cc0cd.cc.cd/jj` |
| 🌍 GitHub | `https://raw.githubusercontent.com/25175/tvyuan/master/tvbox.json` |
| 🇨🇳 Gitee | `https://gitee.com/onm-hundred-and-eleven/tvyuan/raw/main/tvbox.json` |

### 🗄️ Full Version

Combines all sites. Collection sites are ranked first by playback speed, followed by crawler sites by latency. Includes spider JARs:

| Channel | Address |
|------|------|
| 🔗 Direct Link | `https://tv.cc0cd.cc.cd` |
| 🌍 GitHub | `https://raw.githubusercontent.com/25175/tvyuan/master/tvbox_full.json` |
| 🇨🇳 Gitee | `https://gitee.com/onm-hundred-and-eleven/tvyuan/raw/main/tvbox_full.json` (⚠️ May be unavailable due to Gitee censorship) |

### 📦 Multi-Repo Version

Keeps multiple repositories independent. Each source has its own JAR and sites, allowing you to switch repositories (Yingshicang/FongMi):

| Channel | Address |
|------|------|
| 🔗 Direct Link | `https://tv.cc0cd.cc.cd/multi` |
| 🇨🇳 Gitee | `https://gitee.com/onm-hundred-and-eleven/tvyuan/raw/main/tvbox_multi.json` |
| 🌍 GitHub | `https://raw.githubusercontent.com/25175/tvyuan/master/tvbox_multi.json` |

## Client Downloads

| Client | Multi-Repo | Repository Address |
|--------|:----:|---------|
| TVBox Original | ❌ | [GitHub Releases](https://github.com/o0HalfLife0o/TVBoxOSC/releases) |
| Yingshicang (影视仓) | ✅ | [GitHub Repo](https://github.com/q215613905/TVBoxOSC) |
| FongMi (丰米) | ✅ | [GitHub Repo](https://github.com/FongMi/Release) |
| TVBox Bundle Download | - | [Cloud Drive Download](https://pan.wpcoder.cn/?dir=tvbox) |

**Multi-Repo Configuration:**
- Yingshicang: Home → Configuration → Multi-Repo Address
- FongMi: Settings → Configuration → Multi-Repo

## Notes

- Data Source: [tvbox.clbug.com](https://tvbox.clbug.com/user.php)
- Automatic Hourly Updates: Speed Test → Scraping → Merging → Deployment
- Playback Speed Test Process: Fetch Video → Download m3u8 master playlist → Parse media list → Download ts segments → Calculate sustained speed
- **Pinning Rules**: Sony and 360 are fixed in the top two positions; others are sorted by playback speed/latency.
- GitHub Actions uses CF Tunnel + Local Proxy (Domestic IP) for speed tests to bypass collection site IP blocks.
- Unavailable sources are automatically cleaned and re-added once they recover.

## Update Frequency

Executes automatically every hour on the hour (UTC `0 * * * *`) via GitHub Actions.
