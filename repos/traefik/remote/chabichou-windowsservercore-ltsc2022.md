## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4622b051b24d946879937bdb34ae626d66151e694470bbc7844f581c49b41d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull traefik@sha256:21eead5dd52b314fafaa710dfcf7f30f503eba4ab2ab35412742a8dcf1ce1d03
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336195117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abb9cd5a0df859afc5a38ec07d9906e38a22a49342ab8e0065aa96e856188f6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:07:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:07:50 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.0-rc1/traefik_v3.5.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Jul 2025 18:07:53 GMT
EXPOSE 80
# Wed, 09 Jul 2025 18:07:54 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Jul 2025 18:07:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e706f9794b243fbece8bb79d799801d89605a7f12aebade7d7599997553203b3`  
		Last Modified: Wed, 09 Jul 2025 19:08:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b9d8b703e61d97ad92c595a89349b3086de1f27946f92b4a8118ae36aa435d`  
		Last Modified: Wed, 09 Jul 2025 19:08:22 GMT  
		Size: 55.6 MB (55586496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c79bea4a945d9225a8e387c633938b00d7507183b3acabb54e53f779d29083a`  
		Last Modified: Wed, 09 Jul 2025 19:08:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8503651de2a48229781eb58b1650359f1469c91a48120eb1f8fc798aa556570d`  
		Last Modified: Wed, 09 Jul 2025 19:08:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb197ad51088df950ff9b5070506e8b5c1219b379fa62116386f14fd88e67b2`  
		Last Modified: Wed, 09 Jul 2025 19:08:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
