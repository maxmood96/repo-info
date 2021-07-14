## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:ea60a37d4cd836ad64d2085c4951355657b0593ae72734ed4fae65632a0d5a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4530; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull caddy@sha256:bb0c7b5f47048935ba4f19d0c50f077a55808b26054d949eb43de520cc831325
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6282340465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fc37d674fddb51ea1ea283e570fcdf6ffd759df69cce3e04b4aa21d7c65caa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 02:46:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 17:55:50 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Jul 2021 17:55:52 GMT
ENV CADDY_VERSION=v2.4.3
# Wed, 14 Jul 2021 17:57:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Jul 2021 17:57:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Jul 2021 17:57:37 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Jul 2021 17:57:40 GMT
VOLUME [c:/config]
# Wed, 14 Jul 2021 17:57:43 GMT
VOLUME [c:/data]
# Wed, 14 Jul 2021 17:57:47 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Wed, 14 Jul 2021 17:57:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Jul 2021 17:57:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Jul 2021 17:57:56 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Jul 2021 17:57:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Jul 2021 17:58:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Jul 2021 17:58:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Jul 2021 17:58:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Jul 2021 17:58:11 GMT
EXPOSE 80
# Wed, 14 Jul 2021 17:58:13 GMT
EXPOSE 443
# Wed, 14 Jul 2021 17:58:17 GMT
EXPOSE 2019
# Wed, 14 Jul 2021 17:59:27 GMT
RUN caddy version
# Wed, 14 Jul 2021 17:59:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:624cc64d28951435759fcbbc930532718666f3285fc939c97e36c2cda79f80f2`  
		Last Modified: Wed, 14 Jul 2021 03:41:42 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06238427c9b88265ed3cdfeec77aec8e724c862b5cad74b4c915f1155503fc23`  
		Last Modified: Wed, 14 Jul 2021 18:04:18 GMT  
		Size: 368.9 KB (368868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec631ec6104314fab092109f82e03e92a263f37016f9777f38216c398c0aaf21`  
		Last Modified: Wed, 14 Jul 2021 18:04:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71310a3dc2b1ff4839f83b7fa572580cbef410952e37e7ee82b775c53d2ce630`  
		Last Modified: Wed, 14 Jul 2021 18:04:31 GMT  
		Size: 12.0 MB (12037024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8ec887f9fda7c360451ca6bcccb940af9d1a24bb69e85a3ef346ba13415d2d`  
		Last Modified: Wed, 14 Jul 2021 18:04:17 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ffdfdd78569260947f2b1e29f82db6de5cb5ade25556346e86db7167cfc65f`  
		Last Modified: Wed, 14 Jul 2021 18:04:17 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b9ff736282e8509a54b0dad98e757e205f7be0b8520be831664a5cb74bb03`  
		Last Modified: Wed, 14 Jul 2021 18:04:15 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed1bfbe3cacc8f61a484038719184291148d04f84e6d2b695c1e996528e224c`  
		Last Modified: Wed, 14 Jul 2021 18:04:15 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c028396699085481f6601f2f95a0f1cbba44772397c6ae19d8a0d493763b873`  
		Last Modified: Wed, 14 Jul 2021 18:04:15 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35807ddc6d27e3a2a8ef0e94b444003b2fc474dd12b15f6624ae793bf2513706`  
		Last Modified: Wed, 14 Jul 2021 18:04:15 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c7dfba943a088b8b4f1517984d002b759aca03f254651e670d1d8007f0c357`  
		Last Modified: Wed, 14 Jul 2021 18:04:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7428ea97e0cf35bda688dc6f8dc66673365775aeb879c6dd81d1d6f6315ca5cc`  
		Last Modified: Wed, 14 Jul 2021 18:04:13 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab24fa6fdce2f9d78ffaaf1290dd6568e8e516d949135456eaa12e70405a784`  
		Last Modified: Wed, 14 Jul 2021 18:04:12 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89889237f657b2b38fa13dda844b3fd82fae1774030c2c14b30d0c53a692f896`  
		Last Modified: Wed, 14 Jul 2021 18:04:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b7322cb2537ea3d616a9a37befcae8fa41d99b2a8c0bbc92cbec5bca1b7ab`  
		Last Modified: Wed, 14 Jul 2021 18:04:12 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f62e712f8a5a941d3f050509ae2295e72d857e96917edd85d697d8474ed84`  
		Last Modified: Wed, 14 Jul 2021 18:04:12 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6d552982e783bd6b630354fac745cb1870f925adb21cbe45e89af6bc51b8e6`  
		Last Modified: Wed, 14 Jul 2021 18:04:10 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e980d5e293cda7f98db180869a0475da445f60e40c19c7f97e1fda93b70cc36e`  
		Last Modified: Wed, 14 Jul 2021 18:04:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c24b50f7f57376e17491201f7a792835873d08a9c2fc69c0a7316bff05dfbe9`  
		Last Modified: Wed, 14 Jul 2021 18:04:09 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012676c281bbdde57c6b77b5b5774d1c1851bb2db516b2e92186d26e021be89f`  
		Last Modified: Wed, 14 Jul 2021 18:04:10 GMT  
		Size: 277.2 KB (277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bcd309d2e58353362132147ed6353bf043d6db571b9fac67b0cc27ce26e533`  
		Last Modified: Wed, 14 Jul 2021 18:04:09 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
