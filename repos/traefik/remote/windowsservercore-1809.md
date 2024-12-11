## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:7b8a05805dc9ccd74bb62fb82cde37173d43486d13747504dd524db10cdb227a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull traefik@sha256:72d4f8f339a40cd9576c6a8fe61ae4586f5c10277793c8029170f6c3978ac125
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2063710289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c6d73456c52d20ef26e9a1d0509bc9ab70b14cf21512696727700f7fa5acc2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.2.2/traefik_v3.2.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Dec 2024 20:35:25 GMT
EXPOSE 80
# Wed, 11 Dec 2024 20:35:26 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Dec 2024 20:35:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91e5ada0b1baa00eb4c0b646f0b25046b9dbcbf962a9d9bf3d0d793372ea1a1`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef119623a815b9d07b04d912ca2b4068619656c1af22ecb1e917797b2572900d`  
		Last Modified: Wed, 11 Dec 2024 20:35:37 GMT  
		Size: 49.5 MB (49534922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4638373717fc2a7b0a6699ab46b94b93482d31c13585f7fa3d5bc2df3a383a`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5a44bb0db5559777f90a9d5a923e813c491c2298ed0643db7bfc8aaab05514`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b24e9c386763acf4f7fce3b3265bbad44da03a18742aa2141067eb91ffa7aa`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
