## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:b439e96f5bdb87a129daa3c3eda6ef80b8c7009a6c522d76745407e2529b8ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull caddy@sha256:d44ca1e325c10210b4132e28ac908a52325d4d5214066d9923046586296a7eaf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289913418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd30c02543de6185b0366a3a0e7fb994d6820edfe53c277f4bd2019e097e88`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Mon, 21 Apr 2025 22:45:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 21 Apr 2025 22:45:20 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 21 Apr 2025 22:45:21 GMT
ENV CADDY_VERSION=v2.10.0
# Mon, 21 Apr 2025 22:45:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 21 Apr 2025 22:45:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 21 Apr 2025 22:45:31 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 21 Apr 2025 22:45:32 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Mon, 21 Apr 2025 22:45:33 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 21 Apr 2025 22:45:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 21 Apr 2025 22:45:34 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 21 Apr 2025 22:45:35 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 21 Apr 2025 22:45:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 21 Apr 2025 22:45:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 21 Apr 2025 22:45:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 21 Apr 2025 22:45:37 GMT
EXPOSE 80
# Mon, 21 Apr 2025 22:45:38 GMT
EXPOSE 443
# Mon, 21 Apr 2025 22:45:38 GMT
EXPOSE 443/udp
# Mon, 21 Apr 2025 22:45:39 GMT
EXPOSE 2019
# Mon, 21 Apr 2025 22:45:44 GMT
RUN caddy version
# Mon, 21 Apr 2025 22:45:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be7d3f199282fa66af2602d12480668f00aa263056282219fca5d03cbae37e`  
		Last Modified: Mon, 21 Apr 2025 22:45:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc40b9aaaab2324132ad41ce832a6f51671b10c6c1b46f51acc1983c1afe5f16`  
		Last Modified: Mon, 21 Apr 2025 22:45:50 GMT  
		Size: 356.7 KB (356740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10776fa98dda0c1eae1bda63456485d88dafe2130e5f8ab2a1ab94428d732669`  
		Last Modified: Mon, 21 Apr 2025 22:45:50 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f109ddea3d9571b6471a838e4e9d5ed66ff9107da91d377f0ea62a84400f269`  
		Last Modified: Mon, 21 Apr 2025 22:45:51 GMT  
		Size: 15.6 MB (15613990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfcd5a01204fe97d5eefde4e7a6c98f601614ba420b2ba8a28a92e90ea4cc2e`  
		Last Modified: Mon, 21 Apr 2025 22:45:49 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e25273ee5b969c4392368def4621dff96340df1b03346cf99d05171c0efef2`  
		Last Modified: Mon, 21 Apr 2025 22:45:49 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfe8d08c95291777d6204dc30a71a8a58860535ead3983bfe7f9d01171a329b`  
		Last Modified: Mon, 21 Apr 2025 22:45:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206eaafcec9647c8110e1127c762f4c163338cf422bf7281260d1754d688b6e5`  
		Last Modified: Mon, 21 Apr 2025 22:45:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6186ed0ab91e3fddd48f62f0d233ead51642ddfebb3289509aae0565e2b6cb`  
		Last Modified: Mon, 21 Apr 2025 22:45:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf60a2a27778bbb4b7e61016fcdb1767b94c676c5b1a7cb6b1074e8a4a1a25a`  
		Last Modified: Mon, 21 Apr 2025 22:45:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a75af895d1a4fcf75072488a7d866f1a18e7f31d022d46176f40fce2e80d31`  
		Last Modified: Mon, 21 Apr 2025 22:45:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0cedb0a35c060d315fdfd94da819df2f69e8e95661916fd159660fb7c1fc16`  
		Last Modified: Mon, 21 Apr 2025 22:45:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26c0443cabae9a60bd1081592d6d771bafa8425c97ec49f8b7024c6c3916377`  
		Last Modified: Mon, 21 Apr 2025 22:45:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a12bafa9eed53430a493ead2fd0878e4c5804fff96776403ed9945a75e61a66`  
		Last Modified: Mon, 21 Apr 2025 22:45:48 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f587853f722d8910ec015be652268dc42a8bda3ac222a806d2c606d0babf85`  
		Last Modified: Mon, 21 Apr 2025 22:45:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a4cab1c6947c6be9016f3bf4b43d1663288cdcfdb732e60d872a8f151fba98`  
		Last Modified: Mon, 21 Apr 2025 22:45:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae64dafdc61d18dc3c28d331c345410fe2f49ec98ffaf251fe33d631a9687cbb`  
		Last Modified: Mon, 21 Apr 2025 22:45:47 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a83a6bca7465edf1d51a6d71d103cc6d1b9c8024c6ecc8274c423288b3a81d8`  
		Last Modified: Mon, 21 Apr 2025 22:45:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52205c6f78665e28f012b25979f39a95b41e5a28cbc6ca6da17641478bff698`  
		Last Modified: Mon, 21 Apr 2025 22:45:47 GMT  
		Size: 338.2 KB (338250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecc8c59c20a978ea494fc1caecda58c6e950647852106afe31be1afc6056d88`  
		Last Modified: Mon, 21 Apr 2025 22:45:47 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
