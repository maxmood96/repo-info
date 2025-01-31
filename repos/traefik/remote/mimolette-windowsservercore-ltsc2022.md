## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:64515e12893b6f93d2bab5b87db2066db33ed3258fc26e5a2ce833bbb1ce46e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull traefik@sha256:67f305aadccd36733f2e92f065ca5a1fe17886070d822750eab2eaf1fcf58ed9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2309308724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0673bb46e0f0083d52fc0a0fd1f336f2f2038ad244c983ed4d8d78f1320bf5e9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 17:28:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 17:30:38 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.20/traefik_v2.11.20_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 31 Jan 2025 17:30:40 GMT
EXPOSE 80
# Fri, 31 Jan 2025 17:30:41 GMT
ENTRYPOINT ["/traefik"]
# Fri, 31 Jan 2025 17:30:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.20 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:de661d6b470ec1ca2b6513e88fb681de279f74eac0053f65bfc48cf12ef10d51`  
		Last Modified: Fri, 31 Jan 2025 17:30:44 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d362eb1c5ded7da5529f5c7a8209c60981680b6b61f0a8341457c86c86404838`  
		Last Modified: Fri, 31 Jan 2025 17:30:49 GMT  
		Size: 46.9 MB (46918266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10142110ca8e1a6de9278d28f379dd5051f98be77c0d6bd5b893d0a61f1f7a`  
		Last Modified: Fri, 31 Jan 2025 17:30:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e88dab9d67de78709ac9b5385b3987adc1edce33c11069220212106279e763`  
		Last Modified: Fri, 31 Jan 2025 17:30:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9f8945388de81af81a0235e31ef8e27ee3f06d87cc4caff8b2e2b1155c8304`  
		Last Modified: Fri, 31 Jan 2025 17:30:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
