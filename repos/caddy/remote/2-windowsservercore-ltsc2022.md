## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f53a52ba7ec244ce2186a5b31770729a5cb32d2149f4393d85537e159e83e195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull caddy@sha256:44f20ec51b71402b6b8277ea4c2da1d30339b76013c608682a1d34773bc3ab6e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289937043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b43e7689ba9c40bc52c17df841c24f8d4a12ebf22ed8a44c0586d10b9fc4368`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:13:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:13:21 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 May 2025 21:13:21 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 14 May 2025 21:13:31 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.10.0/caddy_2.10.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cb97adb2bff5de752e470486ae72d55a6ddcfe4bfa43f09ed849260955df7f61385ac1e2d28fc80458b6910d71fa38d4295bb0689263dcc1743f2050d847c2ad')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 May 2025 21:13:32 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 May 2025 21:13:33 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 May 2025 21:13:33 GMT
LABEL org.opencontainers.image.version=v2.10.0
# Wed, 14 May 2025 21:13:34 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 May 2025 21:13:35 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 May 2025 21:13:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 May 2025 21:13:37 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 May 2025 21:13:38 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 May 2025 21:13:38 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 May 2025 21:13:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 May 2025 21:13:40 GMT
EXPOSE 80
# Wed, 14 May 2025 21:13:41 GMT
EXPOSE 443
# Wed, 14 May 2025 21:13:41 GMT
EXPOSE 443/udp
# Wed, 14 May 2025 21:13:42 GMT
EXPOSE 2019
# Wed, 14 May 2025 21:13:47 GMT
RUN caddy version
# Wed, 14 May 2025 21:13:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3774c38aded90a32237b47099f5d0c5b4ae5907cff795e83cec47ab8da64234b`  
		Last Modified: Fri, 16 May 2025 14:42:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7299d406e42a4323e3ec0b297d9224f92280d1471de9f8ca7d5b39a57a57f63`  
		Last Modified: Fri, 16 May 2025 14:42:57 GMT  
		Size: 345.7 KB (345689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0430d40418bf59f5653799f54cd1cb259185675f09cd7622ad3d6ebdbe02ff2`  
		Last Modified: Fri, 16 May 2025 14:42:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901686b3434c3d1953133fa9543b31cff53651fea548d67a69d2a3cee980937`  
		Last Modified: Fri, 16 May 2025 14:43:00 GMT  
		Size: 15.6 MB (15601994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2e820ef0f10cc9bb789e73ef65a3b9976f5f71211e68ee81983c346ddc6542`  
		Last Modified: Fri, 16 May 2025 14:42:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db837c93884436b76f9a7684f6ece1697cc24198890423b8cb970545556947a1`  
		Last Modified: Fri, 16 May 2025 14:42:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba20387152e18221acd8b43eba572070f34cf3fd361351b8455757241f386ed0`  
		Last Modified: Fri, 16 May 2025 14:42:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150d0732b6d1945b3733a17e3e7a918361fc158f81e9e35981a5777b9961ccf2`  
		Last Modified: Fri, 16 May 2025 14:42:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61732a9c422acd496075fd26316432522a4ab232009a061fdfd90bf2374744f`  
		Last Modified: Fri, 16 May 2025 14:43:00 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a661e52a5bb9fd330fee6f444e50e6cb8e4bd7ac0c43b9de36c010eb650c75`  
		Last Modified: Fri, 16 May 2025 14:43:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18c885e2fec1e0155028271a3f76db6a07c9467e5ce95ce6b7d99e105b8a28`  
		Last Modified: Fri, 16 May 2025 14:43:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17121e3234fd9e657ff05b74dc9df64a1eebfe9ad69dbadca727bcc43e8e736`  
		Last Modified: Fri, 16 May 2025 14:43:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d08f95daa6a22a997e60826ca01bab1ef6a73ecbb7abe68afed40dc6f21b7`  
		Last Modified: Fri, 16 May 2025 14:43:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcfe1bded2693c2559aac6507e7759338ae55764b40d3ddc13cb127467ba954`  
		Last Modified: Fri, 16 May 2025 14:43:02 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8ba5617d8d789ee415761fc2deb49db082127b3ec5882dda3f4e220ee30411`  
		Last Modified: Fri, 16 May 2025 14:43:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801dfa8e565b6a764546cf59d37766031cabefae950bac71e00556d3181925a`  
		Last Modified: Fri, 16 May 2025 14:43:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868edfcff37e597842cd4c8e4a2ec1aea69b62b47887ff2c5c9869daf266e50a`  
		Last Modified: Fri, 16 May 2025 14:43:03 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc17f222d8403aec5c10c7e74eedc05c61aa532f5f5c96bb524ed903929089a`  
		Last Modified: Fri, 16 May 2025 14:43:03 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ace187b2921d578888456e562dbea6270eef3147e12138c151a878446adf8f`  
		Last Modified: Fri, 16 May 2025 14:43:03 GMT  
		Size: 339.0 KB (339040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d78a56066095c33c16c4b8f724545c3241d74dd931e62ff5501d1208b72aaa2`  
		Last Modified: Fri, 16 May 2025 14:43:04 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
