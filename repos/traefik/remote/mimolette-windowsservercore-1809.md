## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:96004a3171b53e9a00cfa63e243381c38cc4f24f2110d77bb1b27438f35b0cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull traefik@sha256:c87d79c995c96b54af070950a7dd977ec45ca31d7b5fe5e80821d30626a3963f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289608263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b4fc59381f0faf65f469d9419798f50077f0f323c5594b738593f90229024b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 19:36:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:56:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 13 Aug 2024 20:56:18 GMT
EXPOSE 80
# Tue, 13 Aug 2024 20:56:18 GMT
ENTRYPOINT ["/traefik"]
# Tue, 13 Aug 2024 20:56:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff016dbc7255d05f8f8e1599a5a13062173c7235efe1e9c1bcb59176beb33ccd`  
		Last Modified: Tue, 13 Aug 2024 20:28:42 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09fc42d7577972a3495ce17896480d0c8c0a8f6bd14e97aa392c0c471293941`  
		Last Modified: Tue, 13 Aug 2024 20:58:36 GMT  
		Size: 44.4 MB (44399439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60748cb1b86686bfb9774559f2c8c50f54d962cf3c5f51b1d9dd6c9ab0ecb49`  
		Last Modified: Tue, 13 Aug 2024 20:58:29 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa2513901d81431dc71aaef8854d14f5e8749046050f1f865d8b93e07d9fb25`  
		Last Modified: Tue, 13 Aug 2024 20:58:29 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9ab1c334efed2f2697c68c4f515525a746707871098fa05ed51ef41ef649e5`  
		Last Modified: Tue, 13 Aug 2024 20:58:29 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
