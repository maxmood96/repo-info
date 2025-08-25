## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3ebb7e7a0141c5f1434331567920cb6803bcb77417482786ce8e21cc1efad8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:94a958d9c90c7cea6e6e84c782202f1e5897c8697724d9644523f5a1abdc84d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299042432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45263b5939455552936239df47ed52b4d2ffd98c70bc7fc53f0a732feb2faf1e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Mon, 25 Aug 2025 19:48:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Aug 2025 19:49:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 25 Aug 2025 19:49:41 GMT
ENV CADDY_VERSION=v2.10.2
# Mon, 25 Aug 2025 19:49:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.2/caddy_2.10.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('88347875f0cd4b5e26bb39cd1f359613f932d54158d560e03244004d1ba6e61aae0cd625ba7c913bd46df096ef973fef2249396b0bb81143414378cb4447aeb8')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 25 Aug 2025 19:49:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 25 Aug 2025 19:49:59 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 25 Aug 2025 19:50:00 GMT
LABEL org.opencontainers.image.version=v2.10.2
# Mon, 25 Aug 2025 19:50:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 25 Aug 2025 19:50:02 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 25 Aug 2025 19:50:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 25 Aug 2025 19:50:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 25 Aug 2025 19:50:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 25 Aug 2025 19:50:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 25 Aug 2025 19:50:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 25 Aug 2025 19:50:10 GMT
EXPOSE 80
# Mon, 25 Aug 2025 19:50:11 GMT
EXPOSE 443
# Mon, 25 Aug 2025 19:50:13 GMT
EXPOSE 443/udp
# Mon, 25 Aug 2025 19:50:14 GMT
EXPOSE 2019
# Mon, 25 Aug 2025 19:50:21 GMT
RUN caddy version
# Mon, 25 Aug 2025 19:50:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90c08ceb2f6836c5a3f96f4bad8e8dae29d69c0ff62712aa0ee85fdece7d76`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e16cc6e43f351f150e39d1deb349080d2aee23c4f090e6928593bdd436bc29`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 375.6 KB (375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8216fdfdcd9f3c9f4e8631a1452968429a39761a8afbfc5212b629e829fa1b50`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77619d61ae35572f741fcfc99f64cf94bf9f8e7e845d5b7ff8bdeac9a267f01`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 16.6 MB (16585526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be2940a1be8626d69d4989c5242c51df872e48fc73c90796f5ecadaadae3ecc`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5542ab361ebc21d84f57da33db4d258ad00aed29b1d447dcfae5924cc582fd3`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a44e84c943b052f910ad0d60a8d2cca96f2ee649668ba4b7492751c5cbcbd03`  
		Last Modified: Mon, 25 Aug 2025 19:50:50 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510d6bbdeed664c25b81861e9b783c232a4d92ab1c210db1bae2bd4b9713d05`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf01e3f5483d0c99e290501519b745bdf9e71464495dcc1fe9660a92a3ed7c7e`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d886c12cf2dac8fb10b9c163508d1bba0306d85bb21ba1b92f5307e97c46b1c`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca056ece9bd4889ab245be06455e524b39f10fa09998cf463a16d050b75989f`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a7e1bf734c16e0f65422db5c1617b0239eefb2bcff11552dbe64a89e9819b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9bb6a197fa0860c4f52a15b3549e03af2e9a59f7872fa11d48ae9dabdfd02`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba85439d7d71b7faf36607dd62109f751f6c508c7ef2b5ee22c692d536d510b`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512b8e1f1cb2a36feef7cb64d8c7b3614a6fbe351cec2caeabe75ece5558af6`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1967f7a6af31b437d48218909f883afb07c219f61a581ab6fa478bf7b204a929`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e8282889ddc2dec312519178bf2b335f33c4c53141abb24510c987fbf72318`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662df9b41df56fc076d30afcfd5882b4d14476611e901b2fbbe160d9befc15d5`  
		Last Modified: Mon, 25 Aug 2025 19:50:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952283a11250fcb4ef2c693549b682848d0f8e23490d751baceca24f5e528c1a`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 367.4 KB (367418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc983ad550d2670db2cdaab199ae85cc26d1e321e1be058c6d2e593022172f2`  
		Last Modified: Mon, 25 Aug 2025 19:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
