## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:0e8cb96bf051cdf3db7bbc415bf1ba2bea9c1192a1005e55dcc6074fe71eaf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull caddy@sha256:2c2b2cee149cf16c7a5e73056128c864b9e4ecec264c94da750e6cb9efbbb70b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1790373055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3612f2107a3cbf6f6483ca6ab233e9cfc4bceed17e966aedafa1afc405080d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 May 2023 23:19:11 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 17 May 2023 23:19:12 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 17 May 2023 23:19:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 17 May 2023 23:19:38 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 17 May 2023 23:19:39 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 17 May 2023 23:19:39 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 17 May 2023 23:19:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 17 May 2023 23:19:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 17 May 2023 23:19:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 17 May 2023 23:19:48 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 17 May 2023 23:19:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 17 May 2023 23:19:50 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 17 May 2023 23:19:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 17 May 2023 23:19:51 GMT
EXPOSE 80
# Wed, 17 May 2023 23:19:52 GMT
EXPOSE 443
# Wed, 17 May 2023 23:19:53 GMT
EXPOSE 443/udp
# Wed, 17 May 2023 23:19:54 GMT
EXPOSE 2019
# Wed, 17 May 2023 23:20:09 GMT
RUN caddy version
# Wed, 17 May 2023 23:20:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773e7289297a0b670dd0f5b459e443d0fc67abfb369f11bbd6b9443350ca64e5`  
		Last Modified: Wed, 17 May 2023 23:28:46 GMT  
		Size: 465.9 KB (465938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94af1d117cf76c9b6562f1bf3bb48068106a82dd2f1337feb41d90c77db77ab9`  
		Last Modified: Wed, 17 May 2023 23:28:46 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b8a45cf51a4263ef838742c93a2c11d2a9503240c858bffe2fbfd7ad01ec49`  
		Last Modified: Wed, 17 May 2023 23:28:49 GMT  
		Size: 14.6 MB (14615239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c4c68a46692cb9e7c9359ed822b2a67e50a90b978a45f2279bb84d764ee162`  
		Last Modified: Wed, 17 May 2023 23:28:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c9b768fff03f66352a27dae03c8444b146313c11096f83f580e2b541475499`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532f4b22d25a67fe100c3530f29074d3f3405213dd63f45d4b49376cb265c0a`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d798b31fccdd732e7d90632a5935e62d21822df0c7d76391503e0fe1c584526`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd5527e7c7321520aa3e9f8652c3e10918cb8b88cfa5fe5f47caf8930cb03ad`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6581610a4eeffb57b8289ca72c2fe7e34e2719a97b819bd3422156d0d5611e`  
		Last Modified: Wed, 17 May 2023 23:28:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19fdcf10e626d335dc37d46bdb8e0f84d6a1b3e6d431ae68ad05080beebe08`  
		Last Modified: Wed, 17 May 2023 23:28:43 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343daf867b19c635e13ad92d4343f1ba1742005df62e0be0634dfd3852472831`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debb6649a6130da8389dc7046c8ccf4f2137238de5f6b7862bfb6c19d339acb7`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5320194029403b147910476f029af57fd84deded14e1cc5cc50487fb657a18eb`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159258e57541ba556d195797c078d89804128bb14f4ff8fa91626cf81720e5b2`  
		Last Modified: Wed, 17 May 2023 23:28:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2a7b4b8871c0cda5d19f702ba1b0cbbb8a6b32f6a30767da107f20a2402875`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b857a3a45246a5bbb59fdfe43bc40b06f7e738e6b3d0ecf05ab3208773b4a46`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edcd27ca1e9f7c57518df882d84a4a7220c32187184b74909056355ba5f8f7e`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fc296cd3515b886a31e9f122eba2e9132ae76437ef43a124fe6ebde52a30db`  
		Last Modified: Wed, 17 May 2023 23:28:41 GMT  
		Size: 288.1 KB (288051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cf4a5a2e6444ddce694b57e8588d1bda0e8ed08cd034125b6277ea824ff6d4`  
		Last Modified: Wed, 17 May 2023 23:28:40 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
