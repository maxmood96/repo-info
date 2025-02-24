## `traefik:2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:eee01092c3c60ecc7e0c9aa07551f7993162e9fdc422e32687d61f26f68212e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `traefik:2-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull traefik@sha256:a5d2ff8194f71d199e5858141f4c3b8663c71dc4a18950c93abc7ac21280b56e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183837647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c05afd3557e9123007ebb8fafb2acae1fa6abbd82d098c89dff496ce8136f1c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Mon, 24 Feb 2025 20:31:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 24 Feb 2025 20:31:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.21/traefik_v2.11.21_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 24 Feb 2025 20:31:53 GMT
EXPOSE 80
# Mon, 24 Feb 2025 20:31:54 GMT
ENTRYPOINT ["/traefik"]
# Mon, 24 Feb 2025 20:31:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b2ce3ab7bfdf85679b1fdf1663752fdef91a1c560d1bfa4f57661145332e1`  
		Last Modified: Mon, 24 Feb 2025 20:31:59 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86642fbe68d6a9f35d0c95874174452cde830c6229ab8c0860408291b35f52d`  
		Last Modified: Mon, 24 Feb 2025 20:32:05 GMT  
		Size: 46.9 MB (46923672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400560fd73ffa597a412d180c29dd767e3a794a75d3c214b0695ae54b77b99da`  
		Last Modified: Mon, 24 Feb 2025 20:31:59 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1510ecfb583c3451b32c1dbc379921456e99fb97e60b4077c428703217c3113d`  
		Last Modified: Mon, 24 Feb 2025 20:31:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e32a884f264263e33e0b013348f4b2c919391ad2d8faf70a557c03c235d73d`  
		Last Modified: Mon, 24 Feb 2025 20:31:59 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
