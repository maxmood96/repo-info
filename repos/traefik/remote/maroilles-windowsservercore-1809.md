## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:28a158cbb1f498399673e62f4b77b5fc6abf59324564397ef0b7c19430ca8cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull traefik@sha256:44fc6778ad6b2ddb0bdcddb9561019c5fc9595c265060a07291a12f4cbe49b44
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291142670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4919c09dd96ca89d1f3b47d479f9bf17813c7f78fa7762a1a58b29b97ed5375`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 23 Mar 2020 21:32:24 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.23/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Mon, 23 Mar 2020 21:32:28 GMT
EXPOSE 80
# Mon, 23 Mar 2020 21:32:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 21:32:30 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d0b00e8e040906f3d887b30e678e40efb35c177517d3ab7885312a259fc4cd60`  
		Last Modified: Mon, 23 Mar 2020 21:33:27 GMT  
		Size: 25.8 MB (25801749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b74468fd780764620b22dd13d3c2ad380a2f4b8038f52ed9bea45b29c3e5b`  
		Last Modified: Mon, 23 Mar 2020 21:33:22 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac07893895096293dc66362aaef0ba3fa38751d015265b3c1df0cd9122d7531`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3023a9d8dd0513c3a0f98d6ff8af04fad6fb178de50458b5a9c75acf3963721`  
		Last Modified: Mon, 23 Mar 2020 21:33:21 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
