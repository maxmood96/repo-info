## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:1c3da22f34a4281d2570f5d31abd6a784acbd55cbc3fdc88b8f260b1531daed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:b8c74ebcb6be3b58b1d4376364ba2c49589dff49d6d612836134ae959a599aef
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1506645323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3e2e5ca66935458ea82f0d799a9f9c4e88b8dee081c7594abea106b2148819`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 16:56:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 16:56:45 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.10/traefik_v2.11.10_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Sep 2024 16:56:47 GMT
EXPOSE 80
# Thu, 19 Sep 2024 16:56:48 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Sep 2024 16:56:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad97a5d3de5031b4ed54d5e82e485f4fed90fafaa5711ac7ea24b1a93328e9c`  
		Last Modified: Thu, 19 Sep 2024 16:56:58 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c3d1a280b95879393de8d735a89137666dc9665056737b32d584b64961e351`  
		Last Modified: Thu, 19 Sep 2024 16:57:03 GMT  
		Size: 44.4 MB (44447755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3d8d494e07b22a1f1a956bb760839227d7a013f6c09ffe5bf78fbc994260bd`  
		Last Modified: Thu, 19 Sep 2024 16:56:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d597293ffb1a91e33b40ee42a2323e268ea782f8390de1783c31e5c7e7e9c8`  
		Last Modified: Thu, 19 Sep 2024 16:56:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9521ece3f06e8b504d79c3ffc79e138eba7deebda8782837e70233fc1d29df9`  
		Last Modified: Thu, 19 Sep 2024 16:56:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
