## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:a3f42f0b24b3395f1509d47aab73ab41f98a9b685cca98dda4bf668398ad625f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

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
