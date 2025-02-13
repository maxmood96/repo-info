## `traefik:2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:df54deb1d14fc69f806f2738ccb12087772aa0ef5caee7ff83c1ba658e066934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `traefik:2-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull traefik@sha256:bd3ccc686c59474c7f0d6e7d838718d3f4b4ac73a61a78f689379e8f4b3d44a8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183807306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cc5866824a91d68623ac10ba80edff966ba9b355aa09c5d4cc173236295688`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.20/traefik_v2.11.20_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Feb 2025 00:34:21 GMT
EXPOSE 80
# Thu, 13 Feb 2025 00:34:22 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Feb 2025 00:34:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537e7920c259232148710eb5dff9008d455847defd556e42a4fa967a0b153d20`  
		Last Modified: Thu, 13 Feb 2025 04:10:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b43979542ce70c76db0b4bd5e01655ea94a0bc83e2afd673b521511b8373c1f`  
		Last Modified: Thu, 13 Feb 2025 04:10:18 GMT  
		Size: 46.9 MB (46893329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c491f5b4c8f36ea423ff8fd476714d891e4bbfe6939921e6eda8eae3776f6ab6`  
		Last Modified: Thu, 13 Feb 2025 04:10:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c84ddd53a781088aa17429f4185555ff611a2ef4b69097f17ac375d78fd960`  
		Last Modified: Thu, 13 Feb 2025 04:10:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83156bec52132dd95d51a490b3f2112ea1351ce95d20b1f2898c204ad783b5f6`  
		Last Modified: Thu, 13 Feb 2025 04:10:15 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
