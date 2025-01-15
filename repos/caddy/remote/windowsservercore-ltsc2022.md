## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:d4063265e08f8b386dacf3135383e115c35da9b15b0c1431cd4c72c3071a830f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull caddy@sha256:328df8f31a21e0b7e32a575b06e9bc83247e3091e3ae56ae9faf3f81e1b6a075
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278121731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f763b5faa4397f33f90ea1259aed2de31586837c3493c20749632be35a1f3841`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:43:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:44:08 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 14 Jan 2025 23:44:09 GMT
ENV CADDY_VERSION=v2.9.1
# Tue, 14 Jan 2025 23:44:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 14 Jan 2025 23:44:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Jan 2025 23:44:18 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 14 Jan 2025 23:44:19 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Tue, 14 Jan 2025 23:44:19 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Jan 2025 23:44:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Jan 2025 23:44:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Jan 2025 23:44:20 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Jan 2025 23:44:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Jan 2025 23:44:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Jan 2025 23:44:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Jan 2025 23:44:22 GMT
EXPOSE 80
# Tue, 14 Jan 2025 23:44:23 GMT
EXPOSE 443
# Tue, 14 Jan 2025 23:44:23 GMT
EXPOSE 443/udp
# Tue, 14 Jan 2025 23:44:24 GMT
EXPOSE 2019
# Tue, 14 Jan 2025 23:44:28 GMT
RUN caddy version
# Tue, 14 Jan 2025 23:44:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41da47a392dd2dafe03bbdf18cf803f3f53bf0cb0af8ba64f600d8118f3cc40`  
		Last Modified: Tue, 14 Jan 2025 23:44:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916a6ca3ebfdd4995fbe79029ff05aebe4472636982d1bfbcbcce432634c6116`  
		Last Modified: Tue, 14 Jan 2025 23:44:38 GMT  
		Size: 358.8 KB (358788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee00c3ab56d0fa62c32184fbecced1d5d0c4dbabfc2f02ae4f4148a18be5588`  
		Last Modified: Tue, 14 Jan 2025 23:44:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3a9b71010621d96291dc62d7ac2d8542685772c6f0bd3e3251b133d5e0b0d6`  
		Last Modified: Tue, 14 Jan 2025 23:44:40 GMT  
		Size: 15.0 MB (15009121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f481b6efeff16464c3d06720a4d6f88ca723398135f85cfa3325036b1397896`  
		Last Modified: Tue, 14 Jan 2025 23:44:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2212bb704fd12a26dec74b9ffc0cba06f0a6c910867d7fddb311b55a687a6f3b`  
		Last Modified: Tue, 14 Jan 2025 23:44:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a114c1adec46e9859600ef679ce596a5bbab3e78d446a19ba66b4f084ded8`  
		Last Modified: Tue, 14 Jan 2025 23:44:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da07af58489a139b46442e4ff6dfb39cc54f3c58b020a3a032993596f2a1448`  
		Last Modified: Tue, 14 Jan 2025 23:44:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879c9abd8bb0ab149e48e2da3c64229355030a98078e938f3fae4427ac335b62`  
		Last Modified: Tue, 14 Jan 2025 23:44:36 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413819c228a2e084baf5f67a8021d72d71c45ed2cd7461cb5c27d485af8d0d88`  
		Last Modified: Tue, 14 Jan 2025 23:44:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273bf77c93335873f4393a779d5b925529c457ad8274652aca0fbec4862d3612`  
		Last Modified: Tue, 14 Jan 2025 23:44:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df24b243b0f18408bc12d55bb43b4e1edc3897e2dcd5f2c32e1666412c1105a`  
		Last Modified: Tue, 14 Jan 2025 23:44:34 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d60ec2b9f4e55a9791c4c0b59014180826007473dba12468c0bfa15381df69`  
		Last Modified: Tue, 14 Jan 2025 23:44:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ceb683f6c6407ad03d3f7e8af4928cacf76e84f52ba35bce4ee4f8c624bb03`  
		Last Modified: Tue, 14 Jan 2025 23:44:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbde5c09e99e47cea69480be69a0da81ba08d7e4d7f7e40fa05b42e9a087bc5`  
		Last Modified: Tue, 14 Jan 2025 23:44:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fb72218d0886df3f3671b67e9518b3f95bc3c8321e01f67fa7d11a8750505d`  
		Last Modified: Tue, 14 Jan 2025 23:44:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f61e8b22bd8939d407b0f0a8310ec2a1dead67a2f56200105b05082b3955ee5`  
		Last Modified: Tue, 14 Jan 2025 23:44:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdd76f8960b5d36c51ac201820f2cc91ed16aedfa4db9a5b9510881be8563cd`  
		Last Modified: Tue, 14 Jan 2025 23:44:32 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf9680716eae998633c5218ad416bcd57855406bf27689b448a10972d603267`  
		Last Modified: Tue, 14 Jan 2025 23:44:32 GMT  
		Size: 346.7 KB (346689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60daa00c4f3e0df67ee78a01d997e33f5ee213ff84d457ff2e3ba9ba35d7be95`  
		Last Modified: Tue, 14 Jan 2025 23:44:32 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
