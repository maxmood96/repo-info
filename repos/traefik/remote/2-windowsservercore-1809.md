## `traefik:2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:c668b316dcddc67b6960d0a17731b1bcc989c2d0304d7ecbce492467543042f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `traefik:2-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull traefik@sha256:ffd536312c7dbd43ef80842efe66178e3fb733af5a2b41f30e7474fa4f775441
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1947861369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b55e522386d7e8dbae7da9ca46e1d286407a1dc22e784312322b78a1ce533fa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 28 Oct 2024 17:57:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Oct 2024 17:59:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.13/traefik_v2.11.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 28 Oct 2024 17:59:21 GMT
EXPOSE 80
# Mon, 28 Oct 2024 17:59:22 GMT
ENTRYPOINT ["/traefik"]
# Mon, 28 Oct 2024 17:59:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d64adf8b3d8d3090e50ee4e43734e9a7dd17a5c460c9ce0a8fe8d87111d53d`  
		Last Modified: Mon, 28 Oct 2024 17:59:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dcec3bf39af0437e5af00884e939d2e9de4178dd3d198c1a3b3a73561f0f6c`  
		Last Modified: Mon, 28 Oct 2024 17:59:30 GMT  
		Size: 46.0 MB (46030921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f3b7c7562bd6c10f45102fe62e29f9b429f7ffe0434a9b6387bdd937d5e4d3`  
		Last Modified: Mon, 28 Oct 2024 17:59:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d6c116b5cde58cbc54a99f004a2c683f18c9e11487b82a78fdde75699a2392`  
		Last Modified: Mon, 28 Oct 2024 17:59:25 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615f9a7347bcbe8be3cc0000e684a411ce948eb144addcdefd503738f4dc7b72`  
		Last Modified: Mon, 28 Oct 2024 17:59:25 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
