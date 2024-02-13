## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:f7a50aee3fdde8ae5aded88d0fd58aa317935ca72713ed0242bd7809a52ca570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull traefik@sha256:11af0932b812b0e766efaccb987c14ed57124d9a27d21f3f5a8a288c38b2bcb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111970705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c58c6f589458150087243450e772d2f48ee302060a0f2643320c385f090ed1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Feb 2024 23:20:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 12 Feb 2024 23:20:08 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:20:09 GMT
ENTRYPOINT ["/traefik"]
# Mon, 12 Feb 2024 23:20:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3e182650f59b900de51ded3bfee4017bab649d21de3f8341d68e7f796aee9`  
		Last Modified: Mon, 12 Feb 2024 23:21:25 GMT  
		Size: 42.2 MB (42242650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423e3dfa116da7e393dd48909dd95ea29060058784705fe4f1c9f6604693da09`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8afe44f0fa3239edbc49d366a7f03f1d76be21abfddc9db48f31b6348890ae`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8f8c0f5fba9a08bf883b01678de16eeff3672d6dad6182f8bef0eb23331a60`  
		Last Modified: Mon, 12 Feb 2024 23:21:16 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
