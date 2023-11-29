## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:4009a9c08e8ff3f3a8215cfc2bcce0355913c9800985c58828d1c7cba68572d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull traefik@sha256:3f007c45153ec0b2e3abe2b3c7c09b093532d0e198ef4b673e4ddd07bf87ea62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098146309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84386f59fd9c10dc0607ccebed700b43ed3f66ebfbc4b235398ca2a53bb6dce2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Nov 2023 02:37:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.10.6/traefik_v2.10.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Nov 2023 02:37:06 GMT
EXPOSE 80
# Wed, 29 Nov 2023 02:37:07 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Nov 2023 02:37:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.10.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba9e80c0146453b6de8f35aea2ae18481cf6436bd532c51c90bd2e049433406`  
		Last Modified: Wed, 29 Nov 2023 02:37:46 GMT  
		Size: 40.7 MB (40709104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54955fdd93b60b49068aadb447e1dbe066720ae5efaa7a315e4592abdd138b0`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463cbb8cb23bb46d13942b85ea410666ef2e97489fb170a77eeaa91dd2f7ae9f`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb9c1cd767d2004163dd2c4b6bb806605d40ff4f8fa90589edef410642f5e41`  
		Last Modified: Wed, 29 Nov 2023 02:37:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
