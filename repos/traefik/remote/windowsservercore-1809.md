## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:a469fcdb7481c955407299e937c5b6cb5c203f6d7cc71c76932b0f41594ee652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull traefik@sha256:0fda36d6a58507d81a2c34a79738e3e19ab72b1c3f63316fb0ea4505eb500b09
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499488628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3650b9ad832bb235bd53c735995b7542b8bf3dd3dd4cdd9a82e38c5ff8d23c44`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 21:28:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.8/traefik_v2.4.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Apr 2021 21:28:43 GMT
EXPOSE 80
# Wed, 14 Apr 2021 21:28:44 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Apr 2021 21:28:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a93cd244b1a7725d26281629f3d234056508569c464f5dea5b03ccbde91bb0f`  
		Last Modified: Wed, 14 Apr 2021 21:30:37 GMT  
		Size: 29.7 MB (29729029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7bb23c17022bf3359394806bf3c61d486089608895251ff7a5acfd7ad96a9a`  
		Last Modified: Wed, 14 Apr 2021 21:30:28 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb84fdded1774834fd927e9a9f74098955381bfeb1991c90d23188e9f2d4bf95`  
		Last Modified: Wed, 14 Apr 2021 21:30:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b1c96a0690beee17c07772a87933a00a71ff757191a2e22ddb4b54488a8000`  
		Last Modified: Wed, 14 Apr 2021 21:30:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
