## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:432c69ff054b3323e57e42a5d4de85efef19c86812278513698af2bdb568dab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:53800b50675d1b603121a50daa255b8d9ab3563b7bb44d56ceb5e5d09eafaa97
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1625270848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49d96260c078b09fc30a8a16442fb4e463d7a0967ed4e0b786e22bfe2a4522d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Tue, 28 Oct 2025 17:51:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Oct 2025 17:57:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 28 Oct 2025 17:57:02 GMT
EXPOSE 80
# Tue, 28 Oct 2025 17:57:03 GMT
ENTRYPOINT ["/traefik"]
# Tue, 28 Oct 2025 17:57:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef75a6e44ccd8f645b5dc14c60e36661f236a4416c9a7e264e23426a1d866db`  
		Last Modified: Tue, 28 Oct 2025 17:56:32 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f01e39d82fd849b819a9557458065ac4b2d1b49d693efd2cfe2378af65bc21`  
		Last Modified: Tue, 28 Oct 2025 17:57:38 GMT  
		Size: 48.1 MB (48072652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84d66a65efe6bbbaf0b49ce4648ed6349de33001bfa51d140f40a32ed1d787c`  
		Last Modified: Tue, 28 Oct 2025 17:57:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a97b017d5cb2fc6996ae4ccb2f05f02a88e129830a9b6e05512d7479fdb7379`  
		Last Modified: Tue, 28 Oct 2025 17:57:34 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe87f4547c4f7d0ef0ea68484584e84899e1dcba91eb34112fda2f273a876d62`  
		Last Modified: Tue, 28 Oct 2025 17:57:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
