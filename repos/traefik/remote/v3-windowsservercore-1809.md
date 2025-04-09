## `traefik:v3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:cdcc24d861d7e3d1348a4e36f260b3ad09c0cec1960e2024cbb3c20591784daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `traefik:v3-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull traefik@sha256:1cbdfcab70311d1dcf889582645fc939ebb395d8b12b8a02412f001bc67cb0e1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206693530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a6af12764bbf5ffcedc36c600ab6c72e4a1f91490027ddea1f261b0354e74`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 31 Mar 2025 17:30:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 31 Mar 2025 17:32:38 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 31 Mar 2025 17:32:41 GMT
EXPOSE 80
# Mon, 31 Mar 2025 17:32:42 GMT
ENTRYPOINT ["/traefik"]
# Mon, 31 Mar 2025 17:32:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8144930ece773181006c1f7c2f56cb82d3d87df943c54562cd85aa86f0359148`  
		Last Modified: Mon, 31 Mar 2025 17:32:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b9b62afcb5ba91ca651b5e896eb6f256dce3b074e7885a4d64f7a63520dcbb`  
		Last Modified: Mon, 31 Mar 2025 17:32:52 GMT  
		Size: 55.1 MB (55053743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bd08b542e115de46881b6b3f7464be507482c6b46b2065e71959fd2deeaf55`  
		Last Modified: Mon, 31 Mar 2025 17:32:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf5cb693f1d21dd74ae33de67af38bfd60423b8949af1f732bf079ab0e509c8`  
		Last Modified: Mon, 31 Mar 2025 17:32:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91446490af70637e30c7ce387abbfe8b5c31d1a6c8083da14982d1371a367b8`  
		Last Modified: Mon, 31 Mar 2025 17:32:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
