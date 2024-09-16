## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1841a32aa05571e7e9b16a275b8be80fa7209c69405b5dd88cf446ba7d0bd207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull traefik@sha256:ae789310517366e4e50f533a1ec8e221e54e93dcc735a623cbd77cd435544888
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1764697872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e130ae8a9b7e7b1e28a87d7ab3bb6118f25981ad160fa5d7b013b5361d94d8d3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Mon, 16 Sep 2024 19:00:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 19:00:35 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.9/traefik_v2.11.9_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 16 Sep 2024 19:00:37 GMT
EXPOSE 80
# Mon, 16 Sep 2024 19:00:37 GMT
ENTRYPOINT ["/traefik"]
# Mon, 16 Sep 2024 19:00:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bca96e7a78931d895aaf73336a9bcb29dcccfba004799b78626f2b12bd9cb9`  
		Last Modified: Mon, 16 Sep 2024 19:00:43 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f374502b196b11ee9607252fc69dd7be58b3e39246b0239d84a42761a0a643`  
		Last Modified: Mon, 16 Sep 2024 19:00:49 GMT  
		Size: 44.4 MB (44424316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f8f7493160a8aeb4c4d43892d193461605e6413233e3b44a4801db9f978825`  
		Last Modified: Mon, 16 Sep 2024 19:00:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7287f75e6e52bb907690e9285692e3f313899c3317714a708dee4f90f4bbb56b`  
		Last Modified: Mon, 16 Sep 2024 19:00:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771aac5a7ddb4e67d4ca89cbf2e0b9a1b55deab920d34a09ff73527789f748af`  
		Last Modified: Mon, 16 Sep 2024 19:00:43 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
