## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:ca2b4747cb915866e1bffaada9f965ee042d63a9157ab57f9456a5907a8e907c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull caddy@sha256:36b5b63d5aac0300092e9a7d6abbc6988c49e3630cd515adcfd0a367bf18c7ed
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3252769132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd339825d8b04e1993ceb11aba41945c5f9c7e6ce79c24ef8cba494a64b6994e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:28:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 Nov 2025 19:28:25 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 11 Nov 2025 19:28:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 Nov 2025 19:28:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 Nov 2025 19:28:34 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 Nov 2025 19:28:34 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Tue, 11 Nov 2025 19:28:35 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 Nov 2025 19:28:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 Nov 2025 19:28:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 Nov 2025 19:28:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 Nov 2025 19:28:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 Nov 2025 19:28:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Nov 2025 19:28:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 Nov 2025 19:28:41 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:28:42 GMT
EXPOSE 443
# Tue, 11 Nov 2025 19:28:43 GMT
EXPOSE 443/udp
# Tue, 11 Nov 2025 19:28:44 GMT
EXPOSE 2019
# Tue, 11 Nov 2025 19:28:49 GMT
RUN caddy version
# Tue, 11 Nov 2025 19:28:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef403ccf6a06c5d6bccd87b689e94f0a23d74b0c4458a3fc098e12f03e64f20`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5031c06549494388931d484767e6e95c386309193d113357b94856fc6d649f35`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 369.5 KB (369464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ef61fad4aec13ff6c7dfb46a15bfa28756d1d3becdb23ab933864099c9f1f2`  
		Last Modified: Tue, 11 Nov 2025 19:29:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095a1389a45c105833f8c9cdf3bd39a6b783a5e3bf75aec67fd73ad737b014a4`  
		Last Modified: Tue, 11 Nov 2025 19:29:11 GMT  
		Size: 16.6 MB (16569586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738373222303a7dbe20ee94a46e3913bb6d7f48a1308b1291cce873b25556238`  
		Last Modified: Tue, 11 Nov 2025 19:29:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be59bc7193f27ce07f7b2e8c77b39e9231810511c10e369075cbf1c61ed10c3`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a0e66b3bdf5c2e56567689a63dbdcea10acd354a7f6256339e3ae237bb0fa0`  
		Last Modified: Tue, 11 Nov 2025 19:29:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223e21e7049143946cd0357c43ca29be9f9088fe005c0cdd9444da32fc5187e4`  
		Last Modified: Tue, 11 Nov 2025 19:29:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ba333182fd626e7146ffc6c131dcb2784c69567bcaa0e57cd5920350c9aebf`  
		Last Modified: Tue, 11 Nov 2025 19:29:12 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc1078d23da42dc400d7ca6da18b7b1ec974466bffc33415f03e014af31b5f6`  
		Last Modified: Tue, 11 Nov 2025 19:29:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6abfd2489eebd3ef2d501be791f774da8d1a81ee91127ce0e427cc5d844c9c`  
		Last Modified: Tue, 11 Nov 2025 19:29:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7e4eb8bc585044379bc6bf1c1d036899d2c22ef2b498012cfe5db7242d18f`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35c743c8f00657d066e1200bfc725660e739f77d0573111d2a98730b8c43321`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc11880233f4d5e8a4f3d4196925acb7ff2901aaee1ed0aca9f875719ceeda`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a966f2f9ea9a06d932ca013f31f3a2a25b7a959e493b12526af5096ed74611`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2200c6ae86442d75bf2ecb43c51b0ba84fe1c4706392f2b0472f84766bef57bb`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd2e39b27498768071a4eb72b34b732abb20abf12d0379791cb6fe15d047845`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940a71a122bb51a8ace56ee314ea2e0bc832c03d6f4735bf0adf5e7820d37306`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ed40aaf602f1cb7879964c8e4190ef328d50afa2b2e305031359b973204c3a`  
		Last Modified: Tue, 11 Nov 2025 19:29:10 GMT  
		Size: 352.0 KB (351981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e3bb54241731747c15aca0be9cbe087a98562002aa4c595fe6253a7b72f270`  
		Last Modified: Tue, 11 Nov 2025 19:29:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
