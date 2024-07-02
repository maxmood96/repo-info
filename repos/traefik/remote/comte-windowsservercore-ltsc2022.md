## `traefik:comte-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:1e283c02acaea60d41ac865fe5916b0b1dfdc7fa84af713045a93434f5efde6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `traefik:comte-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull traefik@sha256:a535d4da052ccdac83302dd9ac15f050dd0924d2fee82d2bd5560f3a978a962f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2164065474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52d177c78eff42397ac89b9a465572d5ff4573eb22a26a7f0e7adfa8018e0f8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:33:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 22:16:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.0-rc3/traefik_v3.1.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 02 Jul 2024 22:16:45 GMT
EXPOSE 80
# Tue, 02 Jul 2024 22:16:46 GMT
ENTRYPOINT ["/traefik"]
# Tue, 02 Jul 2024 22:16:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4326efd24d64d6a2efa78c581696b3d528dfcf784a3d6605e621e343b62e16`  
		Last Modified: Sat, 22 Jun 2024 00:59:51 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a567e0c8ef63ff2d4774febd7bc0dd8afc8fa44fc798cdcc369c911af77c3`  
		Last Modified: Tue, 02 Jul 2024 22:25:41 GMT  
		Size: 45.9 MB (45869739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0be02d2dfeb5a4a93829b99d4e07e9ad1c0206238a7b3f9f9f252293cd8135`  
		Last Modified: Tue, 02 Jul 2024 22:25:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72f6760d61f2999bf2aaf95f7d7be2762d490e4c895dfffe227522c1e960da9`  
		Last Modified: Tue, 02 Jul 2024 22:25:31 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dd9425e942c21dcf76aaf3d6bd87328d874dd6ebff86c27f9a71823087b9f8`  
		Last Modified: Tue, 02 Jul 2024 22:25:31 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
