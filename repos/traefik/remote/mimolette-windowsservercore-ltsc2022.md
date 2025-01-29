## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:9a744d66d04c80d680edc17fe62ef20cdbc47e23b07f5acf0de4e252baef678d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull traefik@sha256:58687fee2c63018337f2739d948aab091fbe452af020e6138e3ec2a8f95d0c01
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2309281834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e11ef1099b724045811838cca21f80cd3ed7f38fb4a415f480145ced4750249`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 29 Jan 2025 17:26:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Jan 2025 17:27:38 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.19/traefik_v2.11.19_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Jan 2025 17:27:39 GMT
EXPOSE 80
# Wed, 29 Jan 2025 17:27:40 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Jan 2025 17:27:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.19 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a85f61dfd57dbeb40c8f358b6533233d71e87f4da7717b77dac86aee976fd54b`  
		Last Modified: Wed, 29 Jan 2025 17:27:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c824ca0340c8770b9c14d019f9eeff2001a3ba2068dfdaba71c2ae9989130ee`  
		Last Modified: Wed, 29 Jan 2025 17:27:50 GMT  
		Size: 46.9 MB (46891460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c05ef67e4f9712c8e9e0d99ac57728f8dbe2fd9a2b9ea171ce6cc394637aeb3`  
		Last Modified: Wed, 29 Jan 2025 17:27:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ee1802d1bd7d38ee49b391fe430668f3612e6ed27f95c49d09c7dd65ee3dd8`  
		Last Modified: Wed, 29 Jan 2025 17:27:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305404b9e0d6c95a1f0aac27cf11fcde79ea63157a32bded845d077109210a3c`  
		Last Modified: Wed, 29 Jan 2025 17:27:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
