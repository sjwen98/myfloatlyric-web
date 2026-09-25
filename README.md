# myfloatlyric-web

myFloatLyric（悬浮歌词）的官网 + 法务页。静态站，部署到 Vercel（仿 myshakeeat-web）。

## 内容

- `index.html`：落地页
- `privacy.html` / `terms.html` / `data-deletion.html`：Play 上架要的法务页
- `app-ads.txt` / `ads.txt`：AdMob 认证（publisher pub-4551036589300765）
- `assets/logo.svg`、`favicon.svg`：由 app 的 J6 启动图标矢量（`ic_launcher_foreground.xml`）转出
- `assets/site.css`：样式，配色同 J6 图标（#0B0B0F 底、#D4FF3A 荧光绿）

App 不用 Android App Links，所以没有 `.well-known/assetlinks.json` 和 `vercel.json`。

## 隐私政策要跟着 app 改

隐私政策写的是 app **当前**的实际行为，改了下面任何一项都要回来更新：

- 歌词来源列表：目前是 LRCLIB、网易云、QQ 音乐、酷狗、酷我。Musixmatch / LyricFind 配了 key 才会启用，启用后要加进去。
- 「贡献歌词到云端」的默认值：目前默认开。
- AI 听写：目前默认开；音频只在手机上处理，不上传不保存；模型从 Hugging Face 下载。
- 广告：目前只有首页横幅（AdMob），欧洲经济区 / 英国 / 瑞士先经 UMP 征得同意。
- 加任何统计 / 崩溃上报 SDK（目前没有）。

## 部署（Vercel）

1. push 到 GitHub（如 `sjwen98/myfloatlyric-web`）。
2. 在 Vercel 里 Import 这个 repo，项目名设成 `myfloatlyric`，得到域名
   `https://myfloatlyric.vercel.app`。
3. Play Console 的隐私政策网址填 `https://myfloatlyric.vercel.app/privacy.html`。
