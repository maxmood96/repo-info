## `traefik:saintnectaire-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:bcf6a9d3b764ec6c8ae88a4ab3a88db75b5225ab169b7bef1ea1e990df5ded2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `traefik:saintnectaire-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull traefik@sha256:6c05e2f1e7fc60952c8df4ad28acb60a01f0e300b518255c779741bf684899d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329429927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b22860ef39a6ea218038612dc125339115fd34404c2aa18edd32c654aafe57`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:54:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:54:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.7/traefik_v3.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 May 2025 20:54:32 GMT
EXPOSE 80
# Wed, 14 May 2025 20:54:33 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 May 2025 20:54:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd66635f3a4806ba2199fd151e361aa26b0800954dafcd2af396c6146cc2a94`  
		Last Modified: Wed, 14 May 2025 20:54:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f597a49b87d9295fff5ddcbb288071fd4681bdb31417ab1d32f2658789a03ec0`  
		Last Modified: Wed, 14 May 2025 20:54:45 GMT  
		Size: 55.8 MB (55796635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82e4ab8ba2a7a0ed5e87ca37fa51128ba418316fe379fd2c5fc281157f28a96`  
		Last Modified: Wed, 14 May 2025 20:54:37 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604c8d4d05c40b059803e8b1c270e3971e365862b5d20efeec423d133e1b4b8d`  
		Last Modified: Wed, 14 May 2025 20:54:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3eefd3b9a49820fec3dac6b3016d414da30f29e36bf7bebb5441413ce7c0db`  
		Last Modified: Wed, 14 May 2025 20:54:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
