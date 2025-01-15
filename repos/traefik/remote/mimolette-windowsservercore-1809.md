## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7ef32163233f1756950a814b11ded0873aaf242a7d0c9a5b29b37fd38aed12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull traefik@sha256:2da871af654d6713bf4786296996ac0e20896848a03a74ed381fc658b86fe8eb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169113340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642cf818683cd0129342bf1e28256c923dc23752ade29f56857ccf8478e6ab49`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:35:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.18/traefik_v2.11.18_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Jan 2025 23:35:27 GMT
EXPOSE 80
# Tue, 14 Jan 2025 23:35:28 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Jan 2025 23:35:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.18 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6d5c6332c64f42aa0646fa760beb75a0d1eb77d24e970ba9b9caa9e0a5cb52`  
		Last Modified: Tue, 14 Jan 2025 23:35:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4c4d20656d623e8f069a1b7519f9fe5bfa4934a54a597cadf0b834991e5ffe`  
		Last Modified: Tue, 14 Jan 2025 23:35:38 GMT  
		Size: 46.9 MB (46895862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb4bb8c9130c39b92fda6d791b7eeefbfcf350c7e6ea3d3f4ac0c000706c432`  
		Last Modified: Tue, 14 Jan 2025 23:35:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9193ce97ca985b757b14452ed7050c5fedf0d679dbc968a35ddca38bca8888bd`  
		Last Modified: Tue, 14 Jan 2025 23:35:31 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb77b3c0b6817b7e1e32ae0eca83e993d5e96c7f731e5533d342846f1cc212c`  
		Last Modified: Tue, 14 Jan 2025 23:35:31 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
