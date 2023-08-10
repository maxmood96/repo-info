## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:d09c44a52494f8a46e63446ff6548c1ff4c014bcfde411af2be08a16aaf36152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull traefik@sha256:4568469987e3e8928331920fc3100297bcdf3ce8d1f998208d5f4b4fa233e8d4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2034898914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c005a8b967c7e373746cb652366496a798cbcf0aa9a63f1210454bf91b56225`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 06:06:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.4/traefik_v2.10.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 10 Aug 2023 06:06:18 GMT
EXPOSE 80
# Thu, 10 Aug 2023 06:06:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 10 Aug 2023 06:06:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43744a794561fe27107a46f14b914ca9540c12ee29b3c1243dcd4c82100023d6`  
		Last Modified: Thu, 10 Aug 2023 06:07:15 GMT  
		Size: 38.9 MB (38937883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f801ad8131c64b1c24725ddf353c716ba662afe19c4b9cc089ff7b98bb781`  
		Last Modified: Thu, 10 Aug 2023 06:07:07 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306822f1c9720da656db6b53c520a48a75e697a15100dd793a9c947c9a6db59a`  
		Last Modified: Thu, 10 Aug 2023 06:07:07 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd296541b6d7e1bd1b42998a4a0c479e5f86f77bd85d05320251b814dd9e2bd`  
		Last Modified: Thu, 10 Aug 2023 06:07:07 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
