## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7396d39104c37eb2f106d2812bb23723fcd0fea48aaa764d59d94a216b2aeefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull caddy@sha256:4103063078caea5d276ec70b716e08f05a4344223aa7ca43c380d8052a4d0a25
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1594632257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d3d302006e677da247236a5b4e223b870873a3a7009b6f03201f4e29e6bc05`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:28:08 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 24 Oct 2025 18:28:08 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 24 Oct 2025 18:28:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 24 Oct 2025 18:28:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 24 Oct 2025 18:28:19 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 24 Oct 2025 18:28:20 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 24 Oct 2025 18:28:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 24 Oct 2025 18:28:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 24 Oct 2025 18:28:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 24 Oct 2025 18:28:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 24 Oct 2025 18:28:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 24 Oct 2025 18:28:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Oct 2025 18:28:26 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 24 Oct 2025 18:28:27 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:28:28 GMT
EXPOSE 443
# Fri, 24 Oct 2025 18:28:29 GMT
EXPOSE 443/udp
# Fri, 24 Oct 2025 18:28:30 GMT
EXPOSE 2019
# Fri, 24 Oct 2025 18:28:36 GMT
RUN caddy version
# Fri, 24 Oct 2025 18:28:36 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63801865414a7519f369b97117c89482cf5ec3a2c24518d9b1567e21a444d45f`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 503.7 KB (503690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c9bc6efff5ef640878dc132d61ab85645047b02c654dbd3027e4d91c337e64`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef23ab9d7ba6a5598081b351ea287d2ab3490662a162cfcba940724ef5d3978`  
		Last Modified: Fri, 24 Oct 2025 18:28:58 GMT  
		Size: 16.6 MB (16569612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6ef754059c32d94e2a8515d7b0e9d37daa73a6d9969a8a1890c1de67d77d95`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf15aa81a797b9a04cf8b21df338a2e3a0bddd8311972df5d075deab42359527`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f082bf5e374733fece2e2adee759e598cc4804f66ddf7cea9cc8c3832dd71a`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faee987b3103e0c66662fa00853c1720975e97b7a8ad34e4fab593db468a3a5`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c243d775460eb2a76f7a5fef43de5cc27137272dc4e1ad0cfbc6cea747f88ab`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3d7685c1de130472555a690e901971996975203ba3d2a901dc472afcf02b56`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c56198e0afacdb98ddf70e0079ee101c6a8d11580d5608e2d29318eae8b94c`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45036d11faa98a02132586482b417401e869d9c740790434f07036efaa4ccba5`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a77a3f72c72487865116cd3cf1fa650c4b5b6deb331ace78e09da11f57aea1`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7982aeef9ed7b35098a698643ba0e938503754a27c8af97ca02c8570f0faa75`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03542f5e7c7d4e0f21e5669db7b82386f2c401c123962e84039fbff779756337`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523d315cae7ff85b5379ae3b0d0275b9f2f4b79ee4917a4df77ab279c6911ec`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf2f62c7e14199d0a741485515793e6c1a9b66c6f99deb9a715e83837f412f2`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40878058b0ce693b9ab9203cc9759ab504a2be6c3f4ce48d0143710e758ef1`  
		Last Modified: Fri, 24 Oct 2025 18:28:56 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4fa9bdbb68dca559e5f306b20aa043a48881b49bb341ab8e422f94fcf206ec`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 343.7 KB (343666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffce132442e46b1aa7ed1890ad1221f0fb255fcb2e1dd134857957536981f35`  
		Last Modified: Fri, 24 Oct 2025 18:28:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
