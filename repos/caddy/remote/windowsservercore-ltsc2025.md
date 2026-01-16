## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:fb773f36fb8467abc811d4ccd46f96fda635fbff94b6ffba6e74379fd277cb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:89a5b05d302de19c76ba6492f6b044f0a61ed7f5134f3cfd6b6bb66ba1fff566
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1513108446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0cccf98d86da25e10384197f0e57da0cdea17b786a92e7ae15c2a74da3d7aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:53:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:01:52 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 13 Jan 2026 23:01:53 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 13 Jan 2026 23:02:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 13 Jan 2026 23:02:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 13 Jan 2026 23:02:02 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 13 Jan 2026 23:02:02 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 13 Jan 2026 23:02:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 13 Jan 2026 23:02:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 13 Jan 2026 23:02:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 13 Jan 2026 23:02:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 13 Jan 2026 23:02:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 13 Jan 2026 23:02:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Jan 2026 23:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 13 Jan 2026 23:02:08 GMT
EXPOSE 80
# Tue, 13 Jan 2026 23:02:09 GMT
EXPOSE 443
# Tue, 13 Jan 2026 23:02:09 GMT
EXPOSE 443/udp
# Tue, 13 Jan 2026 23:02:10 GMT
EXPOSE 2019
# Tue, 13 Jan 2026 23:02:15 GMT
RUN caddy version
# Tue, 13 Jan 2026 23:02:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed7aff12eed6d468fbfd98c5cdb643204448d37e6b4376b4863d715fe54870b`  
		Last Modified: Tue, 13 Jan 2026 22:57:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da097337a4d3cbc7958e8ec21410fb5200b496d7de5fae11c38ea0da871043a`  
		Last Modified: Tue, 13 Jan 2026 23:02:25 GMT  
		Size: 375.9 KB (375907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcbc4d3f9dfa3586f0cc9134c923d1e867b9c110e6f538ea8824c2ff7297017`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06418096271160bc79da14a747237061fef0e29a1b8ed86e1e8812ff4de5c8a`  
		Last Modified: Tue, 13 Jan 2026 23:02:36 GMT  
		Size: 16.6 MB (16589920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8230676e63f4b75b11d68282f09290b80213da451a30b7cee7f8125a40514de2`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71c6ac69b27677f667dede07c33f53020f4ec91a4a595ae4c262fa0d54194e0`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a311d60e48b37065ff0e1127f4aee98919f8da4d76bac43be102a628956bf3f`  
		Last Modified: Tue, 13 Jan 2026 23:02:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a847ed606b5a64babd841582dfe71d4f87a070104b3f789105086b628ff7bd`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6ff6671da48f882b3ec08aedfb559296c7a303344a02847a9bfb9353eaa424`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99da0f85d6d903b13e62292e81ba6ca04474ed189f806d8be0b211df83d0632`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5432867dcbfccfda8d6c5ec1642611696cba9f81b089b38eb9205f674bf84ef9`  
		Last Modified: Tue, 13 Jan 2026 23:02:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e082aacddee60fc4c0b19a825b3a352cd969e8566ad69cd4af232a3285b1de`  
		Last Modified: Tue, 13 Jan 2026 23:02:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b07f49843e37bb0a1157c2a40603f408adcd48b9ee7b9431340f8c49836168a`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2d0e7c199858c2dfbf9d56c369cfc5ab6758b7dab3961ef3f7c6517722bdc1`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a45151381c655b14049f6ad847d562417d35af1a95656b09a22fd597fdbd6e`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d53fdee35e407adb8a1b8dd79ba05d8feb079c1790bbe50add4a7baa096bd0`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fba317332cea91a89fffb13144617c631d421047ccf045207e2a3a3a23700f8`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5b658530e2be3ddb8ef77f9a3821e25bc2dab4d2f0deda7eb219fe4cd10fdb`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23e9193af276d309e65d2ac2789b6a39a3d59715bf62e00c037cab9b25c8b96`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 359.9 KB (359868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1ec6b1051386239a6f953225cd9230de85f32cb8cf813382b6690eaa200f25`  
		Last Modified: Tue, 13 Jan 2026 23:02:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
