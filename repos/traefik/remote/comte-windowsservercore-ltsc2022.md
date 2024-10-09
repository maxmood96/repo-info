## `traefik:comte-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:004503efc92b63bee391436dd2977e4a7afeb12d583f58b1a2b39c878318aa2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:comte-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:0158985ca09714f9d385dabf16a0fb25aff1e683d3675d0a81cc9436a134e443
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1508199109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3352f4919f6f81f03982f1c5c03b8c3640a1580580dd055c50985e8cad9947`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 17:56:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 17:58:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.6/traefik_v3.1.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Oct 2024 17:58:05 GMT
EXPOSE 80
# Wed, 09 Oct 2024 17:58:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Oct 2024 17:58:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6170413ffe3920a0f50fb33bfe147b42150bdbb66787ed4552d9ebde69ddff1`  
		Last Modified: Wed, 09 Oct 2024 17:58:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a6eba59d8c6287a3fd89a8a829f6a17f2072aee241ef56f7358c57c74e020e`  
		Last Modified: Wed, 09 Oct 2024 17:58:15 GMT  
		Size: 46.0 MB (46001557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede76eecebeea8482b5f9e730d3e65c6b5d8bf6d8bdf0fd48e5e44471876f9c7`  
		Last Modified: Wed, 09 Oct 2024 17:58:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4abd9b969f3e1f738daccdf980c6352dccf6d903a25e8a57dbef14ce5dc9b3`  
		Last Modified: Wed, 09 Oct 2024 17:58:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d542f5e9bd5fd871936b66c37776d40ff5db65a6e1d291214fb07cddc2e89`  
		Last Modified: Wed, 09 Oct 2024 17:58:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
