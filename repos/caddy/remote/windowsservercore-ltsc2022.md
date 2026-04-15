## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:523a0a22c7a1b90e6afdeecdd3c841d8cd908f9592a6d0eda8edb36755b18a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull caddy@sha256:b8df27c06cfdbe2fa4590d2de484278aad4f969b053b9202c91a5072a6b73787
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088751785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e017579baae316e73869e6a36c53d38e7fbe1e4c0b536c6e356c548f7d9e3723`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:03:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:28:36 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 14 Apr 2026 21:28:37 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 14 Apr 2026 21:28:48 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('77db9ab02b0dbfc3a8b3928e1c88e48f2b328adcdb02affbc49442ce183cc901d1f4d2ce2a5d1dc897a318948133b1f98f209e1cad56b050bb98336c2ffddd04')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 14 Apr 2026 21:28:49 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Apr 2026 21:28:50 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 14 Apr 2026 21:28:51 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Tue, 14 Apr 2026 21:28:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Apr 2026 21:28:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Apr 2026 21:28:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Apr 2026 21:28:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Apr 2026 21:28:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Apr 2026 21:28:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Apr 2026 21:28:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Apr 2026 21:28:57 GMT
EXPOSE 80
# Tue, 14 Apr 2026 21:28:58 GMT
EXPOSE 443
# Tue, 14 Apr 2026 21:29:00 GMT
EXPOSE 443/udp
# Tue, 14 Apr 2026 21:29:00 GMT
EXPOSE 2019
# Tue, 14 Apr 2026 21:29:06 GMT
RUN caddy version
# Tue, 14 Apr 2026 21:29:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7859559f7e482ab69f3dddf83b05a23fb97e6c47cc09bb11f9f91ea0b96dbf26`  
		Last Modified: Tue, 14 Apr 2026 21:05:58 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d2bd12f91f97f2185947a6c6616993b9dff74580c85224a5af1d7d96c71cd9`  
		Last Modified: Tue, 14 Apr 2026 21:29:16 GMT  
		Size: 501.5 KB (501474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb54b9bd5755e8e8265a0b7668bbeca0d7ff399477a75b0404682b7a3c7fa8d1`  
		Last Modified: Tue, 14 Apr 2026 21:29:16 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f194135d2550722e1d0b5cdb4f6e37c1bd909280f808b282d49b4af5ae574dad`  
		Last Modified: Tue, 14 Apr 2026 21:29:18 GMT  
		Size: 17.7 MB (17669467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cda0ad7332ed66bf920633ff8248f57fdfbd8a9526aa68a856eab403fa56e9`  
		Last Modified: Tue, 14 Apr 2026 21:29:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791860b8e0f97359a0021293450cf4ac33e732f2d66b1525a543968beb59fd65`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6fe46198f0322a89913f7b421d8e8380d40fe26601d7965c0d5e611935c19`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7391a402eb516f6f19a3a37d11feacf19bf3efcd7ceebd9af7a1420bbaf454c4`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2f73748f041ea7e7a9fb3f0f7591f82957afe40830a5a0791e14e70b4bf06c`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eec5cc013166f15da87d6404c9d4360f7ad9f017d13e5a8d687128b6cd3b0d`  
		Last Modified: Tue, 14 Apr 2026 21:29:14 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def61174716aaa0c6879c3b2eba76348b2ebc16c7d9475981ff5d6005f504325`  
		Last Modified: Tue, 14 Apr 2026 21:29:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7506def56d28e15862f644d66a37ca310b2af0e67b40dd9c6fcc595db98aae`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29669880bfec5f126f10670df165ea26dde25d0b4a5b413ada63363deeee0c62`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3514521d0494397ad76515629969965baead98a0d17c674804de5f55b7f0bcd6`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d95600f6fee4100d97188239dac7eabd1586d0e2adaf937df6ab2a88dacee20`  
		Last Modified: Tue, 14 Apr 2026 21:29:12 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43921159c6d617ff0a0e8aa7187f357153ddf2fc53970d4b37542983bc392d0`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549a656bcbd3cb99a7bcee7b3f0d9b6a98976e42fc63a96df98a1d85f215baa4`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e971470b949722b894566989b0b0fc2e4ccc9158199c44ef6898c92d35d0ea7a`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e247fe332f0242556386843c3436148b806e7fd290c3b07ec7e8622f788b80`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 347.3 KB (347257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35776271f71d5561051d257aad8ee5adcacca3bd040eb8379b9fb0078f60ee2`  
		Last Modified: Tue, 14 Apr 2026 21:29:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
