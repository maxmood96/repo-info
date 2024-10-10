## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d0959ecec7205b5c563d76c3460e332bd1f148ad1ad5bb2aab4808f58babf74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull traefik@sha256:461723d2d3efbd770aeb8c768c885a76d3ef4ba4736a36120f57fabdf4409060
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1946397617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9ddbcaefaa10739aa85ac7e00cd32aa3fe51f6f7d4d4727a2cf56fa6bb957d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:07:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:08:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.12/traefik_v2.11.12_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Oct 2024 23:08:04 GMT
EXPOSE 80
# Wed, 09 Oct 2024 23:08:04 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Oct 2024 23:08:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.12 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3137e967526bf9716b0e8bc922a4e37b20658a81bc86c8752a08dccd8f47cf67`  
		Last Modified: Wed, 09 Oct 2024 23:08:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0f3a730bc33354c5f37e559d466ebc1d85a1cba228229d7834d6ba64c076bd`  
		Last Modified: Wed, 09 Oct 2024 23:08:15 GMT  
		Size: 44.6 MB (44567175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4030d6f779ce2f61dc12b19eab28ac360c2d2ce173165a330cfbf7acf6bde5fd`  
		Last Modified: Wed, 09 Oct 2024 23:08:09 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eba232e969683adeb4ba4867e5a54079507aa5691ebc6a2bf924a6f7478c2f2`  
		Last Modified: Wed, 09 Oct 2024 23:08:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fff5a34317972e0c469929f413789d2f485b586c6785e1c57a70dfe2762512`  
		Last Modified: Wed, 09 Oct 2024 23:08:09 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
