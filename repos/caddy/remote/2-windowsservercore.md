## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:7041f263b42ea139f8d28abf8bcdceb75640fa1880ce630de452f50e4838adfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `caddy:2-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull caddy@sha256:511b84158be2cd7321c48d2c248ebe03c682360a617220e5e6efde2ae35f9049
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3237639580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf8304f2d00f67ac24025f5912c0bbc52bc679f9fba5a2481e01cd8fbb27f6e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:26:29 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 24 Oct 2025 18:26:29 GMT
ENV CADDY_VERSION=v2.10.2
# Fri, 24 Oct 2025 18:26:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 24 Oct 2025 18:26:37 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 24 Oct 2025 18:26:38 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 24 Oct 2025 18:26:39 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Fri, 24 Oct 2025 18:26:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 24 Oct 2025 18:26:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 24 Oct 2025 18:26:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 24 Oct 2025 18:26:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 24 Oct 2025 18:26:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 24 Oct 2025 18:26:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Oct 2025 18:26:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 24 Oct 2025 18:26:44 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:26:45 GMT
EXPOSE 443
# Fri, 24 Oct 2025 18:26:45 GMT
EXPOSE 443/udp
# Fri, 24 Oct 2025 18:26:46 GMT
EXPOSE 2019
# Fri, 24 Oct 2025 18:26:50 GMT
RUN caddy version
# Fri, 24 Oct 2025 18:26:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31dc5fa5609c2995707af6ec67dc6547e4af2c6902ce37234453cb34ae55eadb`  
		Last Modified: Fri, 24 Oct 2025 18:23:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f22e1159424bd0c48407d5295d1584004fe417f968e2821a83bc343cb61937`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 359.5 KB (359531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff47303b59d8b51cd87a637990f7df714c0d24b4af9982f4deaa75a4b9fb9d5c`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bc0ebc080f41b45a756437cf7f7dfc9524ae355f5a278d948be9c51e530845`  
		Last Modified: Fri, 24 Oct 2025 18:27:19 GMT  
		Size: 16.6 MB (16565470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aba17e81acf421f5067f77f5aaa424a082e95315836cf119b352fea960706fb`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afbbe68b220bf1234499abc269ec1427c3c37ef2db8d08d37dc1aea628f6863`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb0a9254b84afc75b10f71a3e37c599a0bd0f677fb575bcae1a80498834a236`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e183220e8dd38cabaea4a7ddecb579018fd5aff1383464b4de7f96c41b588b`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3673787ad996e9d6d09a135e137c092114e5ce4da2d402e5d301c851dbf869`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1130791bf661d9da47198eb77182f17e9e197d542ed58e16f3ff6d0d7b8ca83b`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538a4a803af21e2050871be3db5c64aa44148be906c8879d116509ec794eeca`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b86feb90b91433c1da448a316c5a4dc4fa734223f80c8bb724a45518a8b4b3c`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf4f618cf5f1d94f8bba97662a4e6b4a9cd0b91c8fa079233764d8b721e3630`  
		Last Modified: Fri, 24 Oct 2025 18:27:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39338bfffa892aaa3d90627080d02f5a6abca9ff50e5322e89fd3f41c2ced6b`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a757a29a40240edd4061c65a659bb49bb9bcbba2fe793e154f985d849f5bcd2`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a54b439a880bea1f73230a6be24b6da2511c1c6562e870e001e644df63a901`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a19e3a9f41eebc2ea5690d8982003fb7b939771a135bb1be66e08129f3b39`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0cba82f3a971ab4bf656e57999909683bb2243576d3a7dafdb28045de71d98`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ca0af806ee49e618cc97aaa1ba0e78a2dec7c890939f865a93a17022a67a7`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 345.2 KB (345200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f689867372d3b724f298add438c5292f4ce29df04c080d520154a61b6366d`  
		Last Modified: Fri, 24 Oct 2025 18:27:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.4297; amd64

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
