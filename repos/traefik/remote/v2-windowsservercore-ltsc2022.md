## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:07974aa6e10733b59c357ec99b45126338c335f5d93b5dc99618ce2e401e3f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull traefik@sha256:400e1fe89f804c68730166cd8cf7708de8e8d796e5b1b626eb154b9042a55425
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2322123841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95c0209386f4754733ff66f09255d04ddac96a23c4a2d5ce3ad2a5a1d5305d7`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 31 Mar 2025 17:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 31 Mar 2025 17:29:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.22/traefik_v2.11.22_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 31 Mar 2025 17:29:19 GMT
EXPOSE 80
# Mon, 31 Mar 2025 17:29:21 GMT
ENTRYPOINT ["/traefik"]
# Mon, 31 Mar 2025 17:29:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.22 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4595e220c95ba72e8d94c241f9b92d1e5f77ae594ccbedc301dcf34bf62107`  
		Last Modified: Mon, 31 Mar 2025 17:29:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7529b3a046cde3c0998b64bbf78a08cd34a48964220aa1c0b1404b5bef4bb7`  
		Last Modified: Mon, 31 Mar 2025 17:29:32 GMT  
		Size: 52.2 MB (52177542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6248950bf0f3eb6291570e867734eaf42cd09be95882981637037e6309cc5cc1`  
		Last Modified: Mon, 31 Mar 2025 17:29:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb3b5411ccb096a7fda3112fc9fd46a3bdb3ebda3204cf82bd9b89c6383885`  
		Last Modified: Mon, 31 Mar 2025 17:29:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfcb93fb4727e0a82ff5cc1676cb06979dffb4572f1f93ecdf98b0fc9ef63d7`  
		Last Modified: Mon, 31 Mar 2025 17:29:26 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
