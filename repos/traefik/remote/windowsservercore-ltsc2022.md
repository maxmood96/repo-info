## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8a1f531919f18f983d38943d3410b43ed86de6792729abec26d29c1dbcad7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull traefik@sha256:17dad7fb9fae4ffc80a7ba9559beb9e219a9595c8c515205ef32cd6a6c2a74a6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313647577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9838706f3461885fa4bd9d054c455e1ec8e4bd7d68bb0b9146afae0aab31c44`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:20 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.3/traefik_v3.3.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Feb 2025 00:37:22 GMT
EXPOSE 80
# Thu, 13 Feb 2025 00:37:23 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Feb 2025 00:37:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec713fc1bede7974d3bfbb5b5da53853328754ae579b6a62253f272e93c4b671`  
		Last Modified: Thu, 13 Feb 2025 01:08:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e8ef722ae51cb011faab5d30474df5f18281d07870c0b622d011508d1d1c8d`  
		Last Modified: Thu, 13 Feb 2025 01:08:38 GMT  
		Size: 49.8 MB (49784440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c08e50068627f9317497f5ef08a6d0f209ae5e2812223a3f82bc2a2c5590a`  
		Last Modified: Thu, 13 Feb 2025 01:08:36 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21efd253d3aae156b442366d4226a8d9b334baa96641b8b32e29fd787fe63b66`  
		Last Modified: Thu, 13 Feb 2025 01:08:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652bae56d79b9c12f4f1831cb4a6151469b4b55ab37b04847d3bbe946f0117b8`  
		Last Modified: Thu, 13 Feb 2025 01:08:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
