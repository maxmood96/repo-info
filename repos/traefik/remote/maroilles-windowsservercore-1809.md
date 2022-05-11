## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a07bc9e1c23a8aea5a3aba48bbc075c3da3c5808aec1b177ff02686e407a7e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull traefik@sha256:409130d91fbc0358647a6c76902bdbb381917458dbba5e1b708d2cf349165982
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527038215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba63f98fa60e151dbfa2aeeb320019986a8644a21dbe1aaa3271db5d30b1a59`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 18:44:13 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 11 May 2022 18:44:14 GMT
EXPOSE 80
# Wed, 11 May 2022 18:44:15 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 May 2022 18:44:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4855f4a147e4a46d47f2c6fd99b86646844ad214cf11ba9cd365f0f17f0826`  
		Last Modified: Wed, 11 May 2022 18:46:23 GMT  
		Size: 23.0 MB (22976712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a1c70612f452f4df618632922a10afa962409fa89a5730cccb22cabb054ae5`  
		Last Modified: Wed, 11 May 2022 18:46:17 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857221245c4f0e2826adbe4632333050cb275e3798b22c512e6a05227cfaecdd`  
		Last Modified: Wed, 11 May 2022 18:46:17 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903aa8403bd64b1d753c81fcd69f266fa3e4298268cce3e3b1255ccbee1ee9dc`  
		Last Modified: Wed, 11 May 2022 18:46:17 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
