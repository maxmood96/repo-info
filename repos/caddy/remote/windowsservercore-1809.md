## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:42b2115a0f6b0c698531f3b41f61a85096377ad6f2bc9c7a967b5f7efaecf78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull caddy@sha256:e8b1865dd51a79cddf1ce786b52156e81cbaf67046a24bd475a8115ab960445c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312693391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddbcd3c45a5583a6c9b91d6672b879ac5fd94c25a88540d6ca81b52c37931de`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 18:02:29 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 10 Jun 2020 18:03:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 29 Jun 2020 20:14:27 GMT
ENV CADDY_VERSION=v2.1.0
# Mon, 29 Jun 2020 20:14:59 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.0/caddy_2.1.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('360bade38fea4d0e87bf00f2dc0c7e7b4434bb020af49d189b2c424246710bf6a3074e486ef2c3d6994473bcd62393302a1a704c215b4e323eeaecbfa359a533')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 29 Jun 2020 20:15:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 29 Jun 2020 20:15:02 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 29 Jun 2020 20:15:03 GMT
VOLUME [c:/config]
# Mon, 29 Jun 2020 20:15:04 GMT
VOLUME [c:/data]
# Mon, 29 Jun 2020 20:15:05 GMT
LABEL org.opencontainers.image.version=v2.1.0
# Mon, 29 Jun 2020 20:15:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 29 Jun 2020 20:15:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 29 Jun 2020 20:15:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 29 Jun 2020 20:15:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 29 Jun 2020 20:15:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 29 Jun 2020 20:15:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 29 Jun 2020 20:15:11 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 29 Jun 2020 20:15:11 GMT
EXPOSE 80
# Mon, 29 Jun 2020 20:15:12 GMT
EXPOSE 443
# Mon, 29 Jun 2020 20:15:13 GMT
EXPOSE 2019
# Mon, 29 Jun 2020 20:15:29 GMT
RUN caddy version
# Mon, 29 Jun 2020 20:15:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e676deb3766189ea2b008f69205017c9ee31a77f9c7001fb5a07fb2e2d4fbb0`  
		Last Modified: Wed, 10 Jun 2020 18:09:48 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4ba576338ed5242ba3fb838ce5fa930abb61e22fc422ba46b260dbca773cb9`  
		Last Modified: Wed, 10 Jun 2020 18:09:48 GMT  
		Size: 4.8 MB (4772911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723eab0814ebbb502654a889ac99b52f2f7cb218a7164887ad0c9a1a5634d191`  
		Last Modified: Mon, 29 Jun 2020 20:18:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d3ac5a82f61292731263eecfe0635a4e0b486dd7f7f843a5cf9c1962fb54f1`  
		Last Modified: Mon, 29 Jun 2020 20:18:34 GMT  
		Size: 13.7 MB (13685965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18990846d9f6b2e03b43f0c42307982b5d13426a8d003425ce98e88c1ee61e9e`  
		Last Modified: Mon, 29 Jun 2020 20:18:30 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd85b14725d34f8e3d6505a3730098d0d983c7bfc436fab9f0025e28ea413c9`  
		Last Modified: Mon, 29 Jun 2020 20:18:30 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c83ec7d2b6fe2d3beb4121b8691686945da20d9398144840e2699dd7352378`  
		Last Modified: Mon, 29 Jun 2020 20:18:28 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7205b75fee4bcd79e0441081d0c18f4f16c9e3faddfbe44e9a2017d9c98e12`  
		Last Modified: Mon, 29 Jun 2020 20:18:29 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2d684094d65ac89815f73d6bb42fcc037bb91d14788f39d7c874f923010f78`  
		Last Modified: Mon, 29 Jun 2020 20:18:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d345ee36ca73380ffc59a00a9f9645c4be0f97bd3450083d5105bfb2456e5379`  
		Last Modified: Mon, 29 Jun 2020 20:18:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1399cf9fea037f4b40be192761883219e66d7fac0e8a7e53707b63894fd9a0a`  
		Last Modified: Mon, 29 Jun 2020 20:18:27 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abd79214efe888d78b44116335a0015f91de32819741eba80d9523b930ea548`  
		Last Modified: Mon, 29 Jun 2020 20:18:26 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1ac2c904ffff4f7f0d926f3fedbd61527aaf55aa38e88cde26c9d568962975`  
		Last Modified: Mon, 29 Jun 2020 20:18:25 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a4ea5a1055078abaa7e068c8d881cf36e81204a33175caff409d43aa0c9ce`  
		Last Modified: Mon, 29 Jun 2020 20:18:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6c57249f136d38f7aa1045a8956c4f5f4c3f50d93bfb010221f45219da7dd5`  
		Last Modified: Mon, 29 Jun 2020 20:18:25 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dec9ff0349ee91649d28733494db17d02470cf6a73f8268d7f3e717bb52f90`  
		Last Modified: Mon, 29 Jun 2020 20:18:25 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c09a8d6df681bb92ae4ee08eb66e50aa8636527ebad60c50ee3917dd252a97`  
		Last Modified: Mon, 29 Jun 2020 20:18:22 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3888338b94e4b7f8a0a2eeb0c1724e90d743bddbbda11b28ed6a436cc0acc571`  
		Last Modified: Mon, 29 Jun 2020 20:18:22 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6ef034637a0be1fc8331c80eceeaba597da0bda3d9bb9769fde9678f401e9d`  
		Last Modified: Mon, 29 Jun 2020 20:18:22 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e84984fd0f42956c1dc9d31717a9fada1dfdf8e2cb00ce952e2655bf25249ce`  
		Last Modified: Mon, 29 Jun 2020 20:18:23 GMT  
		Size: 298.4 KB (298450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b4fdef44f059a30624268d4a303dc4436aada1655b41b5380dcdf6a1b925a7`  
		Last Modified: Mon, 29 Jun 2020 20:18:23 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
