## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:f1ff3df355d0e034ce51d2c214c131813651457a2cfdd8a80e9bf32c069238dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull traefik@sha256:3364bcafba31b7a83e5a270c371ac02291e010c41f0c42f9c74b775a51fbb8d3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312181615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61516a459e1c9e446ef9e9e918ac2c287796461db294660eb682d969768ed63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:33:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:33:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.2/traefik_v3.3.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jan 2025 23:33:32 GMT
EXPOSE 80
# Tue, 14 Jan 2025 23:33:33 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jan 2025 23:33:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f05150add7104eef38bc3af5245ab84eabc8e91ed5825ed687d77a951c9643e2`  
		Last Modified: Tue, 14 Jan 2025 23:33:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30d4414f9489ec062c3e858b17e745634359701b8c848fdccdc30bbc4185ab0`  
		Last Modified: Tue, 14 Jan 2025 23:33:44 GMT  
		Size: 49.8 MB (49791214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4872ac25441e907cbd414d28191ecc6542b66d3da8a052b41b343d3d5b831c1`  
		Last Modified: Tue, 14 Jan 2025 23:33:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dc31d99af03a6eeecafad581e0bacf9861484495bcbec56355c0f25c1e1f7b`  
		Last Modified: Tue, 14 Jan 2025 23:33:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a452c97b9e598f9310f65c1a5f4fde2cc8c8248bc49953c52e5a91e05321fcb0`  
		Last Modified: Tue, 14 Jan 2025 23:33:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
