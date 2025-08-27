## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
