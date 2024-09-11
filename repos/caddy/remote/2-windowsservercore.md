## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:c7e3394ae09f30a3259f8d8bfab5c03b8e323fe9f94d8d807f83966b6cbc19c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull caddy@sha256:f0c7cb9d0feb72bf9cb00258f13d280a7b5700f3ca76e604944bbe60e2156f4f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1478200406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37961ff6de96648df38b482ba5680b4b7db1e9d1a822260e16596ebf9086c801`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:03:35 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 11 Sep 2024 00:03:35 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 11 Sep 2024 00:03:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 11 Sep 2024 00:03:46 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 11 Sep 2024 00:03:47 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 11 Sep 2024 00:03:48 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 11 Sep 2024 00:03:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Sep 2024 00:03:49 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Sep 2024 00:03:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Sep 2024 00:03:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Sep 2024 00:03:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Sep 2024 00:03:52 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Sep 2024 00:03:52 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Sep 2024 00:03:53 GMT
EXPOSE 80
# Wed, 11 Sep 2024 00:03:54 GMT
EXPOSE 443
# Wed, 11 Sep 2024 00:03:54 GMT
EXPOSE 443/udp
# Wed, 11 Sep 2024 00:03:55 GMT
EXPOSE 2019
# Wed, 11 Sep 2024 00:04:04 GMT
RUN caddy version
# Wed, 11 Sep 2024 00:04:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7d135f12216ff9fe5d015abc6f9c7517bd893cafbc125e0eb3a9eba51d907d`  
		Last Modified: Wed, 11 Sep 2024 00:04:11 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c4c052039f30c9f755667052544421de67acb336b250fbf78533b114f1fd70`  
		Last Modified: Wed, 11 Sep 2024 00:04:11 GMT  
		Size: 367.4 KB (367406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3142315d203eb0aabd40033242fdad54ae2a1cbbe94a60094fb22e4eb3fabced`  
		Last Modified: Wed, 11 Sep 2024 00:04:11 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5c5afe1801682c0a5ebfde45db6c5a0a64dd49e75432e930966198c9b91138`  
		Last Modified: Wed, 11 Sep 2024 00:04:14 GMT  
		Size: 15.3 MB (15263446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d2aca8d94a09cac06b204caf1ad5c8a9f693bc771a86466142e0aff9239a49`  
		Last Modified: Wed, 11 Sep 2024 00:04:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de00b29eb8b1e09743367deb0c96ff5be07239b9228c0e23a41db9a7a734ff0`  
		Last Modified: Wed, 11 Sep 2024 00:04:10 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfe3f5075a0b03ceca75cb41e20a8c77a48e28060195a9c645f983c91337c4d`  
		Last Modified: Wed, 11 Sep 2024 00:04:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453db4248984a28df29def4df37723827f1c57145413f939229d25f75efc47fe`  
		Last Modified: Wed, 11 Sep 2024 00:04:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a5e1ddbb187d6c30eeaa16669ff8da1d4a447638dd39f7ed1366d0bdd12f2`  
		Last Modified: Wed, 11 Sep 2024 00:04:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc75ecbb1d0605d7fc34ef9b111d52cc46b7858faba5320a65fe0359ee418e8b`  
		Last Modified: Wed, 11 Sep 2024 00:04:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0019a054a2ad995e0e38819b7f9c0a0caa225287074a8a7f8ad050d1444b3a68`  
		Last Modified: Wed, 11 Sep 2024 00:04:09 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e3bcf7e2688b71fde0814fb6c66ac815fa89abeb859a36634ea02d5b53edea`  
		Last Modified: Wed, 11 Sep 2024 00:04:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5669bc60a7dbed10845de4507706139bf1e06ad6c7cc378cfb101ffff431e6a`  
		Last Modified: Wed, 11 Sep 2024 00:04:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6f99080d173c036f102720743e5829334a649b465a626af653dadcbfc9552b`  
		Last Modified: Wed, 11 Sep 2024 00:04:09 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd496adb7ae3db0b3b46e3cfd9070ecad7dced7d6649ec2aa6f877683300af5`  
		Last Modified: Wed, 11 Sep 2024 00:04:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2200b05485e3cb5e5807497c2107a0b5bf5fbb311561af0d31201d251df36a`  
		Last Modified: Wed, 11 Sep 2024 00:04:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfcf43ea1cc2ba6aebf65a1654577e685820a595e3dc28b693f1c1b2436c7ec`  
		Last Modified: Wed, 11 Sep 2024 00:04:08 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5fe6b7ba879ef4faf858ced135dd893500bd516af395548d42a92a495d9b06`  
		Last Modified: Wed, 11 Sep 2024 00:04:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ccbe4b0e3c32fd4b3e8d02433930db383cc667daf6d89fbeb5d65dbfebf68`  
		Last Modified: Wed, 11 Sep 2024 00:04:08 GMT  
		Size: 354.8 KB (354816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850bb3c9a5c59497e57bec08340b8ae2a4e08cd01cd98686dd2cd4800ff20bd8`  
		Last Modified: Wed, 11 Sep 2024 00:04:08 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull caddy@sha256:6ef24a6d9551d1fbae028a9dab9740ceb1947f10aa800855490faf459833f4c0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1736224286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55560c5e54a49402e0b1b3dd00933c864f5e8fa4cc51d78ffe4f540fef3a1abc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:04:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:04:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 11 Sep 2024 00:04:26 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 11 Sep 2024 00:04:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 11 Sep 2024 00:04:41 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 11 Sep 2024 00:04:42 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 11 Sep 2024 00:04:43 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 11 Sep 2024 00:04:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Sep 2024 00:04:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Sep 2024 00:04:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Sep 2024 00:04:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Sep 2024 00:04:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Sep 2024 00:04:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Sep 2024 00:04:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Sep 2024 00:04:49 GMT
EXPOSE 80
# Wed, 11 Sep 2024 00:04:50 GMT
EXPOSE 443
# Wed, 11 Sep 2024 00:04:50 GMT
EXPOSE 443/udp
# Wed, 11 Sep 2024 00:04:51 GMT
EXPOSE 2019
# Wed, 11 Sep 2024 00:04:59 GMT
RUN caddy version
# Wed, 11 Sep 2024 00:05:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc78673b28608b4878843c6c93288be40e2dad4b4e0a5b7eff4e9242df48a13`  
		Last Modified: Wed, 11 Sep 2024 00:05:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8755626da63b0d7bfd91ff3dbdf6a3aa6fbcdaf7e3fc04c7bb4f999c5623fda3`  
		Last Modified: Wed, 11 Sep 2024 00:05:06 GMT  
		Size: 347.4 KB (347400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7682cfb7bddb18af019b1ec9c2f12b64df74048803cfb98fe8b6f98cffa25aa1`  
		Last Modified: Wed, 11 Sep 2024 00:05:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e0b30f073377c668b9504f1801e1e4b7924b87162ba3e3953290d3349385c6`  
		Last Modified: Wed, 11 Sep 2024 00:05:07 GMT  
		Size: 15.2 MB (15248514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1085320a66fdf0a04b69313ee21f60d94092ab0ddc970fc2196c0fde432f9`  
		Last Modified: Wed, 11 Sep 2024 00:05:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3786891fb52122a29a5191e4b28e2897635d30ad737f40088f9921c417cd0986`  
		Last Modified: Wed, 11 Sep 2024 00:05:05 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e18c00fc12bce225ac62c0929b61cf3f84bc9ba289e7696bc579147c9010bd4`  
		Last Modified: Wed, 11 Sep 2024 00:05:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38d90a8f5c887e005ee238b949e2a74acd1c439c91973d4489016b9b67affa3`  
		Last Modified: Wed, 11 Sep 2024 00:05:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a25cd7854c42cc533264f3196a58d6a71f624238658c3f4a2422e61028e9a0d`  
		Last Modified: Wed, 11 Sep 2024 00:05:05 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f441a196289264a3aea9998611d01f926c731717a6b2256f4ae6d849228eec0`  
		Last Modified: Wed, 11 Sep 2024 00:05:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798a5619bcc075b123a8bf041658668c680f5a2aee5bb8e59cc625d4e45f4680`  
		Last Modified: Wed, 11 Sep 2024 00:05:04 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e8ffbb43f5adb6c537daa8f7a6453bf53461fe850935c9825361a11043325`  
		Last Modified: Wed, 11 Sep 2024 00:05:04 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e2a9a85d8ed0d9cd122a00c0c4e4f8f096049379811fbdf7308f13f4578285`  
		Last Modified: Wed, 11 Sep 2024 00:05:04 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d2b7a5e5cb8a779e314fb643d279a97de0a0172b78db4395175da9426eb37`  
		Last Modified: Wed, 11 Sep 2024 00:05:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae847c573f4272fccd098028694dec4a3e0c2df1ad337f26939b77df0fdbb004`  
		Last Modified: Wed, 11 Sep 2024 00:05:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b297af192f4d6188c95945c9b55472bf4dc2b52f4338d3e01843a79cf856ee0`  
		Last Modified: Wed, 11 Sep 2024 00:05:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398433b545d362f30537f0724be073b79378471b9b9ecf3488fe661081f4bb2d`  
		Last Modified: Wed, 11 Sep 2024 00:05:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318b51e3fe6937349755d44929232ff591d7a31b8a6bdb507c57a5c96978866d`  
		Last Modified: Wed, 11 Sep 2024 00:05:03 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ac1950aeb7297efa91294d50ca1568c50150ec5dcff20201e717e238e02f37`  
		Last Modified: Wed, 11 Sep 2024 00:05:03 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bd0596d387ec4d9934c37664c96fdc4434d2df5978d4bf5984763320fcd88c`  
		Last Modified: Wed, 11 Sep 2024 00:05:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
