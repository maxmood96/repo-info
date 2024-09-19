## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:071d0ec28a4e0b3d22e9a566f875a85176a810cef3b118b14afdbd1c040bacc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:3fdd5d00badc7659a534e81c49b2fc073b8157caf0e8db4931450715af5bb99f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1508201272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14f1c2e6f41f99ccc298535dee284d51d05019f8989fcdc6fa461d8d4c364fb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 16:56:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 16:58:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.4/traefik_v3.1.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Sep 2024 16:58:12 GMT
EXPOSE 80
# Thu, 19 Sep 2024 16:58:13 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Sep 2024 16:58:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86cf17fdbeb5764ee1edc878b3287cc6c7a517e3a4cba6bb3fb34931f2a3ab7`  
		Last Modified: Thu, 19 Sep 2024 16:58:16 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3a398880bdf79ec5f4f81ab874c88f67dc420b19697d6a5c5e2953687eb482`  
		Last Modified: Thu, 19 Sep 2024 16:58:21 GMT  
		Size: 46.0 MB (46003716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225ffad84e0e576a2f6b6f52204d18f5212acefef4a97ddccca92385066286ad`  
		Last Modified: Thu, 19 Sep 2024 16:58:16 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fd5867f78fd5d12f3b944735a7681f262d7e32c51eaea30fe6dce149c1c410`  
		Last Modified: Thu, 19 Sep 2024 16:58:16 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3ab68cf4b4209b7b76eea98fabc41bbb16d1dadc47da0cc3f0b973e1c87db`  
		Last Modified: Thu, 19 Sep 2024 16:58:16 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
