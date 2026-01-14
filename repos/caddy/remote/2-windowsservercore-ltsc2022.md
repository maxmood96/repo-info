## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:d1f945b5825e44fd963f1b668ad1893cf5b13d79222f1154511f89ea48840f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull caddy@sha256:16becca79280378e88b2051d12d1314769a0b415cdb9b84f2f20136275ac5a65
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1853108079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c800254ee15911ef36cd6073759b20b36a57b6bbfd256a3feb4b241d152081`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:13:57 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 13 Jan 2026 23:14:51 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 13 Jan 2026 23:15:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 13 Jan 2026 23:15:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 13 Jan 2026 23:15:02 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 13 Jan 2026 23:15:02 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 13 Jan 2026 23:15:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 13 Jan 2026 23:15:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 13 Jan 2026 23:15:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 13 Jan 2026 23:15:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 13 Jan 2026 23:15:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 13 Jan 2026 23:15:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Jan 2026 23:15:06 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 13 Jan 2026 23:15:06 GMT
EXPOSE 80
# Tue, 13 Jan 2026 23:15:07 GMT
EXPOSE 443
# Tue, 13 Jan 2026 23:15:07 GMT
EXPOSE 443/udp
# Tue, 13 Jan 2026 23:15:08 GMT
EXPOSE 2019
# Tue, 13 Jan 2026 23:15:13 GMT
RUN caddy version
# Tue, 13 Jan 2026 23:15:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f681901ae8b8270ef4ad40879b419cd45d092d5d347a675266218039d5b88a0`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38cbb81961c2f4dd4ea0471e5c8e5d476a1cee19d5e742413d19c6651767ee`  
		Last Modified: Tue, 13 Jan 2026 23:14:41 GMT  
		Size: 500.3 KB (500339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b3132259ed2c561da6c075f3fbbd8a6698fd3dfafe958ce6d73cb0f6b468cf`  
		Last Modified: Tue, 13 Jan 2026 23:15:33 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc9dbab2b814e52914dd65f067ff05ce12996e5d0a8a20c58a7677e3913185f`  
		Last Modified: Tue, 13 Jan 2026 23:15:34 GMT  
		Size: 16.6 MB (16572692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90888733249e38209d1f591645d287ede10e90fc68a0af5e55ce957ee3d719d9`  
		Last Modified: Tue, 13 Jan 2026 23:15:33 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d2921ca83802ae4e09b634ce22b132306d3dd78e1e075223bd31fdf3f5366d`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2608027bd6b40a76afbf5e5c5692895818c121b77f7a4df56874534bdb75fc24`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05ecf704cf3a26570cc149e7fb15451d4809103024b11fe49c7c2520cba289e`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee862e5f19886a37dc2738b150f43731e8955604d3a4b59932fb4d524e07d3e5`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b02c163f059fc232d569e348d8f7637fc3f4598ae1d58873f67012610a470`  
		Last Modified: Tue, 13 Jan 2026 23:15:33 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a14284d33a02297abada7c44f4bcfb3360b2995d55195df6b72ebd213bf586`  
		Last Modified: Tue, 13 Jan 2026 23:15:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5bb149899c587e5736ac65d6a5e6cbcb1b8eeff409acdac8f548d0b50c1aa2`  
		Last Modified: Tue, 13 Jan 2026 23:15:33 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a06681c4fc83c53be724c809496ae9e2bb324b89ca51a1bca35089d29fb08e`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1768765146acda529dadabc875a9891416a04a9e1e5cecaab4d3d1c7f710135`  
		Last Modified: Tue, 13 Jan 2026 23:15:33 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1195eb7fc347ce743bd964aab52592159ad4fddc854aa1c3378608a7bba7ea21`  
		Last Modified: Tue, 13 Jan 2026 23:15:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d51b22edf1d7f844dbdd7821f496bfa97980b66a0ff31e25a960b4d219a40b0`  
		Last Modified: Tue, 13 Jan 2026 23:15:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18bcb4e0f4649925458e9f7f2bdc7c651b2958f85939e1b39bea6102b7c650e`  
		Last Modified: Tue, 13 Jan 2026 23:15:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35881d84aee053232b215fe7ce3ed897b5a402611fc82f0d6c766bd7ac047ae`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8622f6870f791ed6ad2f1e32e06720409e49dac44d25a28f63d5a5aa27a43b81`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 353.6 KB (353598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6c18714e5d08d6ccaa5d31e69f93a2045b504ec7481f8299cd8b23af9e5dab`  
		Last Modified: Tue, 13 Jan 2026 23:15:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
