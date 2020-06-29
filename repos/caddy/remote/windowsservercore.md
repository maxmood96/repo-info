## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:197b83d529db3ebae4b13cb9079006ad0016f9964e1f1cad639679a2c214af7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64
	-	windows version 10.0.14393.3750; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1282; amd64

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

### `caddy:windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull caddy@sha256:c9cc0726f345f76e464e535e972374668d02c30c224057e4f82e4186ae942ba6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5758382605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150ecdbd7cbd511f1549e36fab065abcf44446cf7fcd58e45ceef61df883bf2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2020 18:04:40 GMT
ENV CADDY_DIST_COMMIT=1ae255dd910fe0ad14aeec27eabe4f526bf423ab
# Wed, 10 Jun 2020 18:06:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/$env:CADDY_DIST_COMMIT/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 29 Jun 2020 20:15:40 GMT
ENV CADDY_VERSION=v2.1.0
# Mon, 29 Jun 2020 20:17:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.1.0/caddy_2.1.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('360bade38fea4d0e87bf00f2dc0c7e7b4434bb020af49d189b2c424246710bf6a3074e486ef2c3d6994473bcd62393302a1a704c215b4e323eeaecbfa359a533')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 29 Jun 2020 20:17:05 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 29 Jun 2020 20:17:06 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 29 Jun 2020 20:17:07 GMT
VOLUME [c:/config]
# Mon, 29 Jun 2020 20:17:08 GMT
VOLUME [c:/data]
# Mon, 29 Jun 2020 20:17:09 GMT
LABEL org.opencontainers.image.version=v2.1.0
# Mon, 29 Jun 2020 20:17:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 29 Jun 2020 20:17:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 29 Jun 2020 20:17:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 29 Jun 2020 20:17:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 29 Jun 2020 20:17:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 29 Jun 2020 20:17:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 29 Jun 2020 20:17:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 29 Jun 2020 20:17:16 GMT
EXPOSE 80
# Mon, 29 Jun 2020 20:17:17 GMT
EXPOSE 443
# Mon, 29 Jun 2020 20:17:18 GMT
EXPOSE 2019
# Mon, 29 Jun 2020 20:17:58 GMT
RUN caddy version
# Mon, 29 Jun 2020 20:17:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22985925139cd6a6e83b6eb5286a8a6e1053a5c6ddd9762f34deea2aa6bcaacc`  
		Last Modified: Wed, 10 Jun 2020 18:10:17 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43c028d6768e901bc64b3edb7e2e5f72050d3ed78ea4e7337fe85725d250c15`  
		Last Modified: Wed, 10 Jun 2020 18:10:17 GMT  
		Size: 5.4 MB (5404509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58d77a8d67f842374c3e60732465a9aaddfd9ce2b054b39aac0b7f2a420d0f`  
		Last Modified: Mon, 29 Jun 2020 20:18:56 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f76df30f6b9698ddedad69790139a9d2cf4fc871763691861f8aab018ac8ed`  
		Last Modified: Mon, 29 Jun 2020 20:19:01 GMT  
		Size: 18.7 MB (18718943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf3b4f088973e051021b74d9b9f795a9f2c8c71f7ae83e83f0cd6e95343f562`  
		Last Modified: Mon, 29 Jun 2020 20:18:56 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef3ce431d20a03b531eadce4cbe5680aca6c4ee4e24d70578687c89963b41d1`  
		Last Modified: Mon, 29 Jun 2020 20:18:55 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091019db4f4b75fe37b7b7ce991db4c4b02422388f836be3c4eb7c51159208b3`  
		Last Modified: Mon, 29 Jun 2020 20:18:54 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e080558fbf5cadbed8b34080d8bad08b45fff65ab533d87a24639d3ba6fd837f`  
		Last Modified: Mon, 29 Jun 2020 20:18:54 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc66481244327f616ca39ffe8c4b596d1aa9b7d778aa717e75b0b8f4a4c06350`  
		Last Modified: Mon, 29 Jun 2020 20:18:54 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f6e5557d697d57716bbf495fc701cef5b9073dbe5646f64fbbb0b8207fc07a`  
		Last Modified: Mon, 29 Jun 2020 20:18:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e238dae9de9d36d2c73796aa4c2a29645bbd5239ab47082579ccdc42e76244d8`  
		Last Modified: Mon, 29 Jun 2020 20:18:53 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbccba413742cc92bb8c53edd613f0be0250226ae8465165c5bc4e25a0c79a0`  
		Last Modified: Mon, 29 Jun 2020 20:18:51 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911208ad8ab28008b96820a6251bee291bb5840e23ec782b1bbafdfe8019e08c`  
		Last Modified: Mon, 29 Jun 2020 20:18:51 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2440198b129a0383b522e8b349ec26d2b66b1b33c422df3c3933be7c6591f661`  
		Last Modified: Mon, 29 Jun 2020 20:18:51 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa72d9c6b7293c4d60c48fc5729c6f3a7eaa2f8276c8cba94bbb20edab126354`  
		Last Modified: Mon, 29 Jun 2020 20:18:51 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a35778894255e6ba11c0d42ca54c80e69279c8777b609c7366208de7e0ac4c`  
		Last Modified: Mon, 29 Jun 2020 20:18:51 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b99c2dfe7b1a527300bd8de8147e159f8ecdbab796e7a71c7dd3e2df8cf216`  
		Last Modified: Mon, 29 Jun 2020 20:18:48 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9969646e605208d0301ec4741756dd6257ac0991ed01bfde817b513b8e7a9e19`  
		Last Modified: Mon, 29 Jun 2020 20:18:49 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2919689d5a48dd6e4ef39397ffed789e7ff54451a9abaadbc274574a363256e`  
		Last Modified: Mon, 29 Jun 2020 20:18:49 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfa5d572d4b3ac461e8246a58be6e84431cc733d430cb532e99e83af335ded3`  
		Last Modified: Mon, 29 Jun 2020 20:18:49 GMT  
		Size: 239.7 KB (239740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90df7192caf1a86dbf2f53b57375af83ea514b4128fc8040808368b6ae7fd815`  
		Last Modified: Mon, 29 Jun 2020 20:18:49 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
