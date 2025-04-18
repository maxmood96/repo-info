## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:14db7bf66738c140eeca7fffa469e9c417358911f5ef0092ce86e5eec29d4860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull traefik@sha256:9b159551a7673a001a4b596c7f12709f2c6e12cf7a4d301121c2c82f6e58af4f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328610531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f66d4c5757bd1e956b3719a386858ea13cfe1d2d6eb5dadc6e1aa72d364325c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:17:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:18:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 18 Apr 2025 03:18:12 GMT
EXPOSE 80
# Fri, 18 Apr 2025 03:18:12 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Apr 2025 03:18:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead673993ccef304337c5903e57a23fb12c5668ceadc533deee43f0d83d54f73`  
		Last Modified: Fri, 18 Apr 2025 03:18:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528021196fd8fabd97e7fb516fb939d6430a33c71dd52cc6c037f58c4a9f4879`  
		Last Modified: Fri, 18 Apr 2025 03:18:24 GMT  
		Size: 55.0 MB (55022861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15f8d838fb3cfd253f5545abbc283cc40eb71ffef3e1a125adbd9588283d918`  
		Last Modified: Fri, 18 Apr 2025 03:18:17 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfd374ca868cf56af5764d2c33615e2252b05a0cd8a00464890149f5619bd32`  
		Last Modified: Fri, 18 Apr 2025 03:18:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b7c84ba3651142941cb951a90338608c8d8e4e33374e1ae83b7377dbe49c0e`  
		Last Modified: Fri, 18 Apr 2025 03:18:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
