## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:bec6d833d997a3f7907dcf6277c11aace4920b1cbec9d1c266b027090f5c9004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:4fd23b30773310c1866efb523855f75da65dfe093adf2514a4e7b38f2be186ee
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224675880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4202423ff1eb50447f16c7f7ab55cda36166b163e0be89c05c218cd9931f21e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Wed, 03 Jun 2026 18:01:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Jun 2026 18:03:06 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 03 Jun 2026 18:03:07 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 18:03:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.4/caddy_2.11.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cd5ccfd86a4b40732cf715890d0dca5bf3f63adefec5a7914de85adf240c60ce7e5d2791631b88ef9758e46b23bb1730e020b9c5d696889740b284ffd4788e35')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 03 Jun 2026 18:03:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 03 Jun 2026 18:03:34 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 03 Jun 2026 18:03:35 GMT
LABEL org.opencontainers.image.version=v2.11.4
# Wed, 03 Jun 2026 18:03:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 03 Jun 2026 18:03:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 03 Jun 2026 18:03:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 03 Jun 2026 18:03:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 03 Jun 2026 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 03 Jun 2026 18:03:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 03 Jun 2026 18:03:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 03 Jun 2026 18:03:46 GMT
EXPOSE 80
# Wed, 03 Jun 2026 18:03:47 GMT
EXPOSE 443
# Wed, 03 Jun 2026 18:03:48 GMT
EXPOSE 443/udp
# Wed, 03 Jun 2026 18:03:49 GMT
EXPOSE 2019
# Wed, 03 Jun 2026 18:04:06 GMT
RUN caddy version
# Wed, 03 Jun 2026 18:04:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d009066146e2b8d6f07be8fc134922887ca07ed2a2856837e11098a81e2420`  
		Last Modified: Wed, 03 Jun 2026 18:04:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01355b4d9be23fc9a91f6e41b7b7f642d3a22ca6aa67fb4bab8e9f7372205b98`  
		Last Modified: Wed, 03 Jun 2026 18:04:16 GMT  
		Size: 399.8 KB (399824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8d0ae10d8aa44c72bffdb92baa04a10ff623355d68fda27652c170a4ef10b`  
		Last Modified: Wed, 03 Jun 2026 18:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584eec3b1be54f40c462ea65663d0004987e944408b4c6220d76c50fbf3658ca`  
		Last Modified: Wed, 03 Jun 2026 18:04:19 GMT  
		Size: 18.0 MB (17969325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3517ad2ecf856d415502b47ea74f793b8f23ad57ed9e8a989bd48ec308ee5d5b`  
		Last Modified: Wed, 03 Jun 2026 18:04:15 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2aed3098964739430dcfb0681cb8d3c9ff66270b7ff180c104faeb69eca4d3`  
		Last Modified: Wed, 03 Jun 2026 18:04:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9c72d10db1a6db7a7e567ad278fa24331db5299e8072f5941bfb1602993e9`  
		Last Modified: Wed, 03 Jun 2026 18:04:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5218c6e91fa8f2c89090f066e1de88df3283f46e7a5e16b6eb1a3fe5dc62d379`  
		Last Modified: Wed, 03 Jun 2026 18:04:14 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d393d593f70b100d9e93fd5746bc28dfb78bb5f15ad03bfbfe3c2eb6353975`  
		Last Modified: Wed, 03 Jun 2026 18:04:14 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b8e54d73d2276f9271a919037d01a2be2f292619c0968e7b6017ec5856bb35`  
		Last Modified: Wed, 03 Jun 2026 18:04:14 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0ecf308771be68e6f23dde2d508e1a4110bbdca0798d23343f98ef7592758f`  
		Last Modified: Wed, 03 Jun 2026 18:04:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcf258469e960bb9f6226e0255e8d1e9a314867d02135ee8beaccbaa5381a8e`  
		Last Modified: Wed, 03 Jun 2026 18:04:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6548125d157ee3d37417e7bb194b826d06dd3686fd2f7264f92343297703ba7f`  
		Last Modified: Wed, 03 Jun 2026 18:04:12 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce223ae6884faa1857e297eafd4d775b13e3d190c736e76ca375a82b942f8c`  
		Last Modified: Wed, 03 Jun 2026 18:04:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5caef6555fb089b809e1df2249fd722eeee7b1585c289b9c44388a661abc99`  
		Last Modified: Wed, 03 Jun 2026 18:04:12 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f80e0b929845cc7dc7c7c6c298e3e3fb35caeeff7018513485a8a35ba57010a`  
		Last Modified: Wed, 03 Jun 2026 18:04:11 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dca27f896945a02229e4692049a1948f347a24e4111f5067c39ca057e18596`  
		Last Modified: Wed, 03 Jun 2026 18:04:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5006ec5a544ad8b2c71486cf916fd98e341b3bd02b5948f2cd3b63cc5a986cd1`  
		Last Modified: Wed, 03 Jun 2026 18:04:11 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea30aee55cc38743e75c82b9b95238330889617a05907833417ccee96b4f13`  
		Last Modified: Wed, 03 Jun 2026 18:04:11 GMT  
		Size: 343.0 KB (342992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697917b73989875dc97696e2e59c596ca9d01ee1f22ca32e804d7019ad6ca533`  
		Last Modified: Wed, 03 Jun 2026 18:04:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
