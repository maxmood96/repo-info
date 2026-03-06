## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3018ceecd70c39106087c9a459b0b99c4dd9724910479e34c8c80b6374f604f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull caddy@sha256:9b4fd7f581daedf54b6b756b8a46a77c30e12d3121e3d55f67629bbefbbf8318
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1881253536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fdfed50b686da621e00edbc3dcb12aeb42229f728f0450307ed58ad0ac360d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Fri, 06 Mar 2026 18:18:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Mar 2026 18:19:17 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 06 Mar 2026 18:19:18 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:19:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('77db9ab02b0dbfc3a8b3928e1c88e48f2b328adcdb02affbc49442ce183cc901d1f4d2ce2a5d1dc897a318948133b1f98f209e1cad56b050bb98336c2ffddd04')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 06 Mar 2026 18:19:40 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 06 Mar 2026 18:19:41 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 06 Mar 2026 18:19:42 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Fri, 06 Mar 2026 18:19:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 06 Mar 2026 18:19:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 06 Mar 2026 18:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 06 Mar 2026 18:19:47 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 06 Mar 2026 18:19:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 06 Mar 2026 18:19:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 06 Mar 2026 18:19:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 06 Mar 2026 18:19:50 GMT
EXPOSE 80
# Fri, 06 Mar 2026 18:19:51 GMT
EXPOSE 443
# Fri, 06 Mar 2026 18:19:52 GMT
EXPOSE 443/udp
# Fri, 06 Mar 2026 18:19:54 GMT
EXPOSE 2019
# Fri, 06 Mar 2026 18:20:08 GMT
RUN caddy version
# Fri, 06 Mar 2026 18:20:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e4598ca0a476eb0015b70ea5f18464badaddec4f5cd4879f1d76b1f03637e8`  
		Last Modified: Fri, 06 Mar 2026 18:20:17 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06617f3d44ff1ec52e887219bcb44aac3c0ad1e81516694c739cb66e8cca50de`  
		Last Modified: Fri, 06 Mar 2026 18:20:17 GMT  
		Size: 514.7 KB (514735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a55f77ed1215c23e6cd813c17dc358e603e51423c19aa7a6cc959389950729`  
		Last Modified: Fri, 06 Mar 2026 18:20:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c42a2c8a26c95aee51ab20fabbcc6704d70de49aa0c67a792ff8acb7cf30e53`  
		Last Modified: Fri, 06 Mar 2026 18:20:19 GMT  
		Size: 17.7 MB (17689919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6f24dfce07db84280668b05bfb1b88827d3e82f50e599f059f1fe66c4ebc4e`  
		Last Modified: Fri, 06 Mar 2026 18:20:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ad7149aa410736a5723036d7eb71fd6be48d2f1625246e02b777404bc38ac4`  
		Last Modified: Fri, 06 Mar 2026 18:20:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5044415d948876ef367b3c66c84d65b6c57baf4779fd70fcb356674e7a629fcc`  
		Last Modified: Fri, 06 Mar 2026 18:20:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e09d1dd43bc552815e89ec99457b981a20469a7b79d29fc4be541820b61cfb`  
		Last Modified: Fri, 06 Mar 2026 18:20:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99841f72b399819c8aeb93d30c30e8362fd7149de46440ae13e8850f63bf1706`  
		Last Modified: Fri, 06 Mar 2026 18:20:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35422342fcded2b3462ae3b653e05d8753e0667d31e41e1572e3c29104360c50`  
		Last Modified: Fri, 06 Mar 2026 18:20:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c752e06d298dda8a2e2be08835696957c4387f489deb8c829e54454692e2f0d9`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378ff428e7d12f28c6c0d4198bdb0356f04b51c3a73b7843bd209a3117de67e3`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb707731d6c1f17f69688c27a8120534325d9c53039e392d1af69bf2b60ad0`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fc5a99866a9da9894f662fa3257d6ed8ec1fa8a7ae45d8b48e9041182f1000`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eade25abef305aec63bde64cd354b936d0335f91a5b3b32623294ecec19ec2a`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc5bd5e55f0cc5ae41d8bb135d44f3b11dcb0a89125d4d2e43d031e57bde2a5`  
		Last Modified: Fri, 06 Mar 2026 18:20:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d016b9d5ffbea07bf1174d874922cb571acd7fdc8baa001647f70554ff5e1b`  
		Last Modified: Fri, 06 Mar 2026 18:20:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6ca2130f055d8cc536f3fa288be982b9ec18b7504b9fc34f741cd4f257828f`  
		Last Modified: Fri, 06 Mar 2026 18:20:12 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ddb46aed9b510ba95c7a4fb925f794560d0c63e42903084524a811aa8b0737`  
		Last Modified: Fri, 06 Mar 2026 18:20:12 GMT  
		Size: 369.5 KB (369468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473afaa3dfa197a2d7e35a522d2f3cf0baf2b52c7016d2245ef13f78b84cd180`  
		Last Modified: Fri, 06 Mar 2026 18:20:12 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
