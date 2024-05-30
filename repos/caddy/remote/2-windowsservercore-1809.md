## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d48df926bf363a40ecdc79c34c0a1fd25177d1ad25f3588dcc722924acd201a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:331f98665ae8c3c19e06c80a4ac528be9e42d5f6ef4f07526d3b9c0317d2dd62
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195882869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df2e9b1022c4ef5888c5b4c2e379a3033ce203dd51f9991fa4edfda2d02830c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Thu, 30 May 2024 19:53:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:54:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 30 May 2024 19:54:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:54:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.1/caddy_2.8.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d7d2afd6e9d47990b47194c2ca2a385fefe1c5381e0c98d41d799e9f9a797072916b3db17e7c990f792532edeab52cc0cfa399eb907a79b44e1d94d50bae089c')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 30 May 2024 19:54:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.version=v2.8.1
# Thu, 30 May 2024 19:54:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 30 May 2024 19:54:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 30 May 2024 19:54:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 30 May 2024 19:54:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 30 May 2024 19:54:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 80
# Thu, 30 May 2024 19:54:41 GMT
EXPOSE 443
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 443/udp
# Thu, 30 May 2024 19:54:42 GMT
EXPOSE 2019
# Thu, 30 May 2024 19:55:04 GMT
RUN caddy version
# Thu, 30 May 2024 19:55:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a775a3e39f1ad99f64b5d302a453e48892a168ad83545ea79828ce05fc17d3b9`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a159525188279005de2c4b3e93a19bd06213fbf569b7cd7319288fbc6d593`  
		Last Modified: Thu, 30 May 2024 19:55:17 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432f245e22af2896c3aca87c4f73d7674fc2b5e344e16246b21d445202f02f7`  
		Last Modified: Thu, 30 May 2024 19:55:16 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4836d91ab170c38372a4c2c0caa81aa33dd20c83416e92a8120ac04812617277`  
		Last Modified: Thu, 30 May 2024 19:55:18 GMT  
		Size: 15.3 MB (15275512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8341cbcd25b5cac7d2a90051c9330f785a38fe6608e4bc31d35b6d492f7e2e`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e67aaf2796f6f937fecb1050105b1fc623861e78135a9bad5c8000f3d4289f8`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44fede023ff106b0eb57121adae0ac84d9476cee30bad6432cbf7a031002d5`  
		Last Modified: Thu, 30 May 2024 19:55:14 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97c60c85c50d5420c8a864da925d9a1edb38e52badc8463dd7537b19f1b379`  
		Last Modified: Thu, 30 May 2024 19:55:15 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8eeb209a230a82796beb9c2b42b5af3694985d503315351b81d4d7ebda0bc1`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d7e77c436e404e82b630fb538bdc4728100ddb265fa7513a3447493e91286`  
		Last Modified: Thu, 30 May 2024 19:55:13 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1478799fab447a1b23697469e8fb60f66e7fa494b88bb82ca33e46d77791b6`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8d4f39558b7948bf40d7356b34ba0c59441a20d33248762fb524784cd51c87`  
		Last Modified: Thu, 30 May 2024 19:55:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b630cba67a2c9b1eeea93b352141c88aabc8655d55aa3af03aa213d966846a`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e209421d3ddaf36047e889423908ccb1d716840f0b9f35e3c72e142e57deae`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b28b1bb7e241a7746089e5f2e63fe0e8abd0df8b5581aa24c85d4868ba5b70`  
		Last Modified: Thu, 30 May 2024 19:55:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf1640d902923015360a9c057b78f537a1bed595f7abf9523f4950ab40cc78`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dba2c76e146dc0c9d4ead916534681e8f860b3bfd9315219858df31f7028956`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ad3235b0f7097a2848c0c7da57725721d99556fc10d32abe9914ea067eedb`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2f2e8e39412f5a4cc5c5cce938253f9153aa8ec9f526925c5a12f1a6fa4f0`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 360.9 KB (360894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a7b9ba45e6b19c6f9c001d6efea9f878b306a148a591b4f9c4208ad427d562`  
		Last Modified: Thu, 30 May 2024 19:55:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
