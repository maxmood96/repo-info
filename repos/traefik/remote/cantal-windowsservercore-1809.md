## `traefik:cantal-windowsservercore-1809`

```console
$ docker pull traefik@sha256:924895fe18d5e276bd784bb1453de6e64802a7bd1d36c8995db8c63b4daf9e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:cantal-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:6ce87750417b85819c39ba50b0ac140ead81c63533980fccad4fc5784ae221bc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289603103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5df0dbddf8d272cfa2060ea91765334084f996347f54642d665aed86436d9f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Mar 2020 21:16:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.7/traefik_v2.1.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 18 Mar 2020 21:16:26 GMT
EXPOSE 80
# Wed, 18 Mar 2020 21:16:27 GMT
ENTRYPOINT ["/traefik"]
# Wed, 18 Mar 2020 21:16:28 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f895641955abb2113ba9240580f2939d45b9894b338288688fd40f2ce00a7b`  
		Last Modified: Wed, 18 Mar 2020 21:18:25 GMT  
		Size: 24.3 MB (24262121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb28b67cb9e14124f26d200b48383b0e0a60e98231985b600293edeb82fecd`  
		Last Modified: Wed, 18 Mar 2020 21:18:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d69bf59e2ab83f1d466d9da6922c2e4706ccef4e4f28f42161ce68fd8c80879`  
		Last Modified: Wed, 18 Mar 2020 21:18:20 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c75bfdfeed7d42f654d13958eeb8364ab195ac927c2e9f5f904968179ab151f`  
		Last Modified: Wed, 18 Mar 2020 21:18:42 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
