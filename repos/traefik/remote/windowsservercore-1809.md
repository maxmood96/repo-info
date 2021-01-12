## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:7ddeaf69613b70a74bb37ad6740a7a83f687fdfafe1fd0d631723b6e58366881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull traefik@sha256:a0a847a17eeb7195804847135e9bcde0570bdb79e29a472354ef9a270395606d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2425403409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d104a60b508dea4dc3b4ca89e6cca399659968cf553877c38d19329b9a00bd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Jan 2021 00:18:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 12 Jan 2021 00:18:07 GMT
EXPOSE 80
# Tue, 12 Jan 2021 00:18:08 GMT
ENTRYPOINT ["/traefik"]
# Tue, 12 Jan 2021 00:18:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804b57540c9a58f8b6da0daa5017460b1e91dc7dce31ee90ae003fb195b59e66`  
		Last Modified: Tue, 12 Jan 2021 00:19:31 GMT  
		Size: 34.5 MB (34524361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a570ba9586ca385a7918f859bdc33499ce6a5cb27192ac49980576b880a2d`  
		Last Modified: Tue, 12 Jan 2021 00:18:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021043d918ba617c94fd0153d6fe22d888f2dc6f9c53bc46b4744c1fd25b3819`  
		Last Modified: Tue, 12 Jan 2021 00:18:52 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b986b073809f6901559d4e81505f86073faedf5f1d9ff4dfd90b335114f4e83`  
		Last Modified: Tue, 12 Jan 2021 00:18:52 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
