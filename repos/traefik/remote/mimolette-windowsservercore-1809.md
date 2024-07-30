## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:118f90a6a5ea846a9daa041a7059ab0c7f47b665514568ac1ce3a27f12b0f39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull traefik@sha256:c96d5bc8e67f258e089399c2f95356dd08d70b3de8ec72d05fea9821dcb016bc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2282852248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287000caa9461839fd3da6ad54da5e5231d5828058ffdf92d6a3cac091fa21ea`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Jul 2024 19:20:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.7/traefik_v2.11.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 30 Jul 2024 19:20:52 GMT
EXPOSE 80
# Tue, 30 Jul 2024 19:20:52 GMT
ENTRYPOINT ["/traefik"]
# Tue, 30 Jul 2024 19:20:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396e1b977f1ec2790de6e1bcdd9b0272d3ab46f70fdbef2ae277b7f99b83d0b3`  
		Last Modified: Wed, 10 Jul 2024 17:26:34 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d46b3def76a8b37e1d6f8e66f095e1e4cdd8aa07a8d44b064c6ea776369a69`  
		Last Modified: Tue, 30 Jul 2024 19:23:50 GMT  
		Size: 44.4 MB (44417508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91735e503c5500fa3a352f8a5fc671fc7cceaa055b06ea61151d153310a1da42`  
		Last Modified: Tue, 30 Jul 2024 19:23:41 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad30dd2eec7aa4626101392a2c40ead5ddec539ca04f277efa4d5fd15863bb7b`  
		Last Modified: Tue, 30 Jul 2024 19:23:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd4f344021d75e4c722b3b08edf6752903be4615604ff3c0bb5fb6fcfc2ef4c`  
		Last Modified: Tue, 30 Jul 2024 19:23:41 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
