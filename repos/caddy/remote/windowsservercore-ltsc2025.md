## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:55c13c747495e6c4b2ce4d0c6ca5a92d1abb9780a0c273319e60286df4bf24a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull caddy@sha256:e36d18a89c288bae717237f6ec4551d12c2a8bc61a70ca60abb653cf4b6ee3a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3492599094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc47cc456e5ffe80e00e628995343ffb7ef9801d9805db9d4b9db444f6fa91`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:34:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:34:42 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Jun 2025 21:34:43 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 10 Jun 2025 21:34:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Jun 2025 21:34:54 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Jun 2025 21:34:55 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Jun 2025 21:34:56 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Tue, 10 Jun 2025 21:34:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Jun 2025 21:34:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Jun 2025 21:34:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Jun 2025 21:34:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Jun 2025 21:35:01 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Jun 2025 21:35:02 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Jun 2025 21:35:02 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Jun 2025 21:35:03 GMT
EXPOSE 80
# Tue, 10 Jun 2025 21:35:04 GMT
EXPOSE 443
# Tue, 10 Jun 2025 21:35:05 GMT
EXPOSE 443/udp
# Tue, 10 Jun 2025 21:35:06 GMT
EXPOSE 2019
# Tue, 10 Jun 2025 21:35:11 GMT
RUN caddy version
# Tue, 10 Jun 2025 21:35:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3caab1dcbf5b8d24435dfe840a2125725f4a9a2176fee372f045bc85cdb0cf`  
		Last Modified: Tue, 10 Jun 2025 21:38:57 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a083786cf955a53a1e72ca79c58db985baf0b47d78f1358ecfbbd2b13d02e6a1`  
		Last Modified: Tue, 10 Jun 2025 21:38:58 GMT  
		Size: 388.3 KB (388311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9ce4bf9e7447e94642c6c121f3bd81b79169d94685b9e7f8f3c275b6db1755`  
		Last Modified: Tue, 10 Jun 2025 21:38:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96349fcf026f07bce17631d0b6ac19e533b0cd2cfafcd7968502a81afc83d67`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 15.6 MB (15640456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bbfe63f9fb6ee82533d599e69bda2cd333cdbc0752070eb3606e329c068a0e`  
		Last Modified: Tue, 10 Jun 2025 21:38:59 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac8ec186e23e63c916f3800277ba39c5b2488f807d97036b1cd22591b7e4690`  
		Last Modified: Tue, 10 Jun 2025 21:38:59 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9734d9135874c0de3633c63e6b53d8b25e3ae755c6ab4071bcffab46a06f3b`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf82296b97f6852031dcd90ea98e718f0ea0b1c6f9457e4ff8f227189837a08`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a929112da06ad53dd76381285921c4b0743e30e3532b9e190f8dc6139da3b49`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8579a3adac1583b54fc9db9fe3abf4cf015a1360a2dcb23b7b3da632e7249e3c`  
		Last Modified: Tue, 10 Jun 2025 21:39:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f90066cdfadc8a932f6d2d1a9534e55e90d88af1301c1a22d646f376be53ac`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54a9f76c009405dc8c726ddc4b16b1e761b48442af4ea352ec41b992736db30`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9747180ce23a71373095bbafbcfd9336d86b2658245b8ef726dc294cded3fa`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1f6332ffdfdc483a13e2f0b99dc27b9d25769a80de3dc13e9f64e4b326be38`  
		Last Modified: Tue, 10 Jun 2025 21:39:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135c6694a5f6f21e6842b65034228f2ebabcca7a02522653d8f5537b47dbb81d`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4820d05441404d06f206e63f58441f2096db0c3764d17d83224f8d566ebd00`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58106080363bb83028d5b03b1a625c5c1d408856efc741fef7a9a2a83bb480af`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3ff34450abf1162a5107abd80c46694b1e55c990ae4e2028688e6db2ce3d30`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e2298a4816f7b1d3c66211e72de5575c54346c6a118940dd632faa34ad5dab`  
		Last Modified: Tue, 10 Jun 2025 21:39:03 GMT  
		Size: 374.1 KB (374087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d78efe76ea42dd6481f214527712a8d331e2ea38ac0e2e3d92580b2e68599d3`  
		Last Modified: Tue, 10 Jun 2025 21:39:02 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
