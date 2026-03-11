## `caddy:windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:f0fa12df097f62a853c8b7484c3bc7a5cedc5edd13dbd94ffc461c03cef03e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `caddy:windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull caddy@sha256:9444d032b8d3dd61baa76df0696efa8d76f1891490b4c5ea6a1339893ee49d8d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2099610650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8052cbbea9e10807663d77e042c4250aa54fc3442bb3c3bb749aa5a7b9237d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:58:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:09:39 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 10 Mar 2026 22:09:40 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 10 Mar 2026 22:09:48 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.11.2/caddy_2.11.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('77db9ab02b0dbfc3a8b3928e1c88e48f2b328adcdb02affbc49442ce183cc901d1f4d2ce2a5d1dc897a318948133b1f98f209e1cad56b050bb98336c2ffddd04')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 10 Mar 2026 22:09:50 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 10 Mar 2026 22:09:50 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 10 Mar 2026 22:09:51 GMT
LABEL org.opencontainers.image.version=v2.11.2
# Tue, 10 Mar 2026 22:09:51 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 10 Mar 2026 22:09:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 10 Mar 2026 22:09:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 10 Mar 2026 22:09:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 10 Mar 2026 22:09:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 10 Mar 2026 22:09:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 10 Mar 2026 22:09:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 10 Mar 2026 22:09:56 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:09:57 GMT
EXPOSE 443
# Tue, 10 Mar 2026 22:09:59 GMT
EXPOSE 443/udp
# Tue, 10 Mar 2026 22:10:00 GMT
EXPOSE 2019
# Tue, 10 Mar 2026 22:10:05 GMT
RUN caddy version
# Tue, 10 Mar 2026 22:10:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d2b4cff819a0193a1ed730d21d0aef289588a757e37392a2ca29e9e3776fc4`  
		Last Modified: Tue, 10 Mar 2026 21:58:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889b12bb3c1a296811904d112b40fa45a9172953a8eba1cec5ff3d8c599a5b0c`  
		Last Modified: Tue, 10 Mar 2026 22:10:14 GMT  
		Size: 366.3 KB (366311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb592c2a437a27641e5c621aef8df4a72f10fa08b7d925828dac1404d5e8d7`  
		Last Modified: Tue, 10 Mar 2026 22:10:14 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e635aab77ab660cbd30208bcb12d41a9d4c6c7e35e069eb3a2668e749d9dd6f`  
		Last Modified: Tue, 10 Mar 2026 22:10:17 GMT  
		Size: 17.7 MB (17675771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a25f629fe6f2b1de85d1e0488d6ef6ad22e22e393f3fc0c579904f9fdb53511`  
		Last Modified: Tue, 10 Mar 2026 22:10:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1d9fd1b7bca0bca0011c86b82029872eb3a4c4ed5e60da09fd5ca548597bcc`  
		Last Modified: Tue, 10 Mar 2026 22:10:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362c72f4b6977ab5ef7662a9fb84d36b05228c32f46279921d856174e5b3006`  
		Last Modified: Tue, 10 Mar 2026 22:10:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f0f5337e16945581cbebfc7bcb07d8f978de21d17018be3b2779460ec153ab`  
		Last Modified: Tue, 10 Mar 2026 22:10:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd03ac9b6f5be2391ca83eb066042409de7d102200ecdd0b0b08cdfcf521e7`  
		Last Modified: Tue, 10 Mar 2026 22:10:13 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711d77321c950e9548bad670778b420e4cdb0dc9d058e548cf200d0b3fb1fdbe`  
		Last Modified: Tue, 10 Mar 2026 22:10:13 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1793a4bb77a579d7e20ddfa76007fa01d5fd9bf35b48f5337e393489dac3e239`  
		Last Modified: Tue, 10 Mar 2026 22:10:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c314b1770ba39c70ff1436b2d13befb89fb7285bfa554c0bd47f0ae9bc79ad`  
		Last Modified: Tue, 10 Mar 2026 22:10:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef30378cc27f9e21035c6d9aa442dbfcfd35e99ddce3c08ff35056d61dc2201`  
		Last Modified: Tue, 10 Mar 2026 22:10:11 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e523cc5fd695d84129ea1fcf074dcc3facef5a7e31a72ec603abd5a7576976a`  
		Last Modified: Tue, 10 Mar 2026 22:10:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be951e802fe5ff3da39e78bc40ee3114f1cb417c9ddf4f4438ba7158374c080e`  
		Last Modified: Tue, 10 Mar 2026 22:10:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92918d37afd52b4b9d0fe5a0661a8a96b3c2d31293639e144e283b3963d606e0`  
		Last Modified: Tue, 10 Mar 2026 22:10:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7540dd7a8e8e9df74020c48845f3c51cfb25d19140a2266199559fd858ba2f`  
		Last Modified: Tue, 10 Mar 2026 22:10:09 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea67c11e8ef813b3135574755cf5ead7aef387b6e26db729552d5e700542ded6`  
		Last Modified: Tue, 10 Mar 2026 22:10:09 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2289b28c0e659641d5db2acdcf9da0cc0dc8def15d3214aec86bc12b4ca1b5`  
		Last Modified: Tue, 10 Mar 2026 22:10:10 GMT  
		Size: 350.2 KB (350187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13894d70cb841914c45fd9c50e1f3dfdfd3c3e8c4e195acc045e5492d603e390`  
		Last Modified: Tue, 10 Mar 2026 22:10:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
