## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7e0cfd5d5536d1319ffb88ab383e6991c934b66756bf9673dacdaa4678490d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull caddy@sha256:9b35dcb50e10bdf6c5f55bb606a3512f5deab1c8ebbc93cd9b8ced47ed7eae56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000825067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2884654d5af8db74e7d9d2fe9a5eef20e64ebd4a7e54d44e15c329d8a5b021`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 22:06:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:17:05 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Mar 2026 22:17:06 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 10 Mar 2026 22:17:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('77db9ab02b0dbfc3a8b3928e1c88e48f2b328adcdb02affbc49442ce183cc901d1f4d2ce2a5d1dc897a318948133b1f98f209e1cad56b050bb98336c2ffddd04')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Mar 2026 22:17:15 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Mar 2026 22:17:15 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Mar 2026 22:17:16 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Tue, 10 Mar 2026 22:17:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Mar 2026 22:17:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Mar 2026 22:17:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Mar 2026 22:17:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Mar 2026 22:17:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Mar 2026 22:17:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Mar 2026 22:17:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Mar 2026 22:17:21 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:17:22 GMT
EXPOSE 443
# Tue, 10 Mar 2026 22:17:22 GMT
EXPOSE 443/udp
# Tue, 10 Mar 2026 22:17:23 GMT
EXPOSE 2019
# Tue, 10 Mar 2026 22:17:27 GMT
RUN caddy version
# Tue, 10 Mar 2026 22:17:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962b0d1ce3024ddc1b4e4285f5d1e219cdabd8ab83ce91d930dd591708b61b98`  
		Last Modified: Tue, 10 Mar 2026 22:07:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c27238def531c6c0c08dbe6d5b4324aa659a188939cdb229b34d1a296b89be`  
		Last Modified: Tue, 10 Mar 2026 22:17:37 GMT  
		Size: 498.5 KB (498494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1508502505dad83dd83e22a494555ea919a04bb6c882ce9287b5fe0bf8f09711`  
		Last Modified: Tue, 10 Mar 2026 22:17:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d980929918bec0106840059ba20149af010894084b748b86599eb1c4b2089da`  
		Last Modified: Tue, 10 Mar 2026 22:17:39 GMT  
		Size: 17.7 MB (17667998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675e1af5d3d2830905c5101bb63819ec07319d46d0519ced66308e57c8d12512`  
		Last Modified: Tue, 10 Mar 2026 22:17:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04bd2c2d77fc3ee055fd72ddbfc69c920675e2d5f27edabd7914f6014ce2fc3`  
		Last Modified: Tue, 10 Mar 2026 22:17:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecb19c1441402fdfe45a2aea8683ffe735e223a3838d0e95c1eed3e65696403`  
		Last Modified: Tue, 10 Mar 2026 22:17:35 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ce6fcb945c25e2f444f0276f86b9f70b1b3c82ab10fe4a3316ae3c18fa8942`  
		Last Modified: Tue, 10 Mar 2026 22:17:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28ad69a863f32f0b8ac2133153076cdfc3cf65c9ba7d040f4e6d024678d0596`  
		Last Modified: Tue, 10 Mar 2026 22:17:35 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffd9fdb7d32d6321e02f16abc61870f8ee639dd8bee585e888ea13b61951ff0`  
		Last Modified: Tue, 10 Mar 2026 22:17:35 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2c180153fac6a721534171b22fa783112720bd4433ca153549bf919cdb562e`  
		Last Modified: Tue, 10 Mar 2026 22:17:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d8f4a52530164892c04a65f63e1c29e726c99fe6a17ec43b8dcb947b1e64d8`  
		Last Modified: Tue, 10 Mar 2026 22:17:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce442c57bd16ca8ba08a584b9b3b808d40b3cf06b2e26ef61a815c24ba37eadc`  
		Last Modified: Tue, 10 Mar 2026 22:17:34 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44de9b0f357af0861da4828a75c84973bf878ab145cdcabd24a8b2d56700e42`  
		Last Modified: Tue, 10 Mar 2026 22:17:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b851256427e93dc0fced34bb91280335ac0d4053ef200d9f1a055afd895bcab1`  
		Last Modified: Tue, 10 Mar 2026 22:17:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f7162407db6ba09c46780d47e312e4e64982a6b4e65cb7fe3afaefc46b3dc2`  
		Last Modified: Tue, 10 Mar 2026 22:17:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafbc484bd6b17a9e154f0bf0fb00d702f346c5876e72c989e6c35b2dfeadc5`  
		Last Modified: Tue, 10 Mar 2026 22:17:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b6b0b9e8d04dec10ff8c67626fe6882657680d3d1cda3893c2ae1dcfaba7ca`  
		Last Modified: Tue, 10 Mar 2026 22:17:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108a6cb3d5e0fcb00f3c8258fa78e76afda23d255e2f54886cf5ec63f296674e`  
		Last Modified: Tue, 10 Mar 2026 22:17:32 GMT  
		Size: 354.9 KB (354890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1427d893b67e8b4a96c1491f2e0efa4b67b92c33b41b2851d0181633bfe1cdf7`  
		Last Modified: Tue, 10 Mar 2026 22:17:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
