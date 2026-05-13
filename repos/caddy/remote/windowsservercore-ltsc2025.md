## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:206dde5cb85762b952e1ced7003d7630ae6e1f8f347ae67b56c84026948e8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b16462cc7a0f16b89f53e9daab1aeb8eb23e4744b2ea6e023210dadc61fdbdaa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224655434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972b7ef31899945cc177efa3431eb890f8fd35b6922b934860e69cafdc2a713`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:51:04 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 12 May 2026 23:51:05 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 12 May 2026 23:51:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.3/caddy_2.11.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('338f5557a1554677875b79dbc4b10d008781111ad29223811e64217936fa5d58602ddd54724ef1cb1473b7ec07805cf5286d6aa1e810febde7e36daf497d791f')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 23:51:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 23:51:16 GMT
LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 23:51:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 23:51:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 23:51:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 23:51:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 23:51:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 23:51:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 23:51:23 GMT
EXPOSE 80
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443
# Tue, 12 May 2026 23:51:24 GMT
EXPOSE 443/udp
# Tue, 12 May 2026 23:51:25 GMT
EXPOSE 2019
# Tue, 12 May 2026 23:51:30 GMT
RUN caddy version
# Tue, 12 May 2026 23:51:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b51f7f8f80dada0ff15ebfc020be610f4ccb1f56aa991e13148edd33df8342`  
		Last Modified: Tue, 12 May 2026 23:39:57 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe1944ff5efba96fd30329293ab8134ace0b6684af082bf47cda84e4f7204c`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 397.3 KB (397315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3c39b66eb6795624a847c056772dab53370128bbcb4e538baf188c7df3b9a`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f68a4b0ce8e1336f561dc1314ceea99d290a5a26a89fcf895fccc46c572de84`  
		Last Modified: Tue, 12 May 2026 23:51:43 GMT  
		Size: 17.9 MB (17925812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e454b307a8f6be02612b6199eea5cf454d70d962c7ff77f8bc5f114c39a64b9`  
		Last Modified: Tue, 12 May 2026 23:51:40 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde1568c0a1480d4d6c097328e54316cf7de933fccf79d86060ce97c6d636bd9`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d055e6806538c851021b3dddd0514c58b4d522742ac7d6044147cf9b1cd4e`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c13c6892dcfe7293f31402fd685b3bf1f71df6a266f062dde2423d43579615`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09471348081b3b03babb39155b859f194119e3cff711e24c78f17f8a06dc1038`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d571880e2a100b02a0084a5bf3ad833473d805e63cbdf48505bd20db8a59c`  
		Last Modified: Tue, 12 May 2026 23:51:38 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528808aa330d8c9852a027409e72327cec60ec8dc2e7bceb2f50498b5833c8ae`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879a15a0f71e61c7b8dd0561a8048b9cc16f1196ca792b06b2b56cf42ac5d47`  
		Last Modified: Tue, 12 May 2026 23:51:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf6a6ab367f1fe2776f8885301292a5bf760d415846647dee2743652ca5d59`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde47a461e52b5287788c82892d05e381914226b7fbb8842aea7c3b52c426d2`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed9cee8659d90315075a4646f49d52a549fd16c98b2fa8b924c03b2876ecda`  
		Last Modified: Tue, 12 May 2026 23:51:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a39302d516f37b6ad0643d4d34405d9bbecd01ecbda5bcb5715b3605eef59`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d56991752a6ad8922565856226f0b7a4bc008b96e16c3e3eac3a59509b9fd6b`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db660d2a8b5f65ee6d345395fe2cd35ac148cc4a849fd683380c1498336f6fe8`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f9236b001ff836f088fc705a18b2e8c4994215d2fdf8c6027d4730429bb`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 368.1 KB (368052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e486a577a11f9202b7784c79d9e69fad384f8731219958d76691be25629eb030`  
		Last Modified: Tue, 12 May 2026 23:51:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
