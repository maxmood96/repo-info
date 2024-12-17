## `traefik:saintnectaire-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f611d7fd52f88eb33964620e46e1a5d39dad33d348a4d836e2f955a4c8f99b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `traefik:saintnectaire-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull traefik@sha256:f88058b63dac642dafe88d0fceb6ca06bb5650832803ad0231bf4a1722e24294
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2063899263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27b7660853dba7e6e3eb9ecadb264285863d7316254fc5298e8e8f46341ca36`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Mon, 16 Dec 2024 18:28:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Dec 2024 18:29:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.0-rc1/traefik_v3.3.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 16 Dec 2024 18:29:29 GMT
EXPOSE 80
# Mon, 16 Dec 2024 18:29:29 GMT
ENTRYPOINT ["/traefik"]
# Mon, 16 Dec 2024 18:29:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864ba24a2ebaff562553a8b14094c14c16c66974e105db20062af2a884241cf`  
		Last Modified: Mon, 16 Dec 2024 18:29:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73952a1476ef39b7138b0844f03f6f26d27f144e12b56eabeafca84011f81b4`  
		Last Modified: Mon, 16 Dec 2024 18:29:38 GMT  
		Size: 49.7 MB (49723899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3756194bdef113eec444c318ea32b10b85f1a9b76ce66302523a0e58f1a463`  
		Last Modified: Mon, 16 Dec 2024 18:29:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afab5b0f1ba149f87dede8c4e9d5a8f41fe5961dae3423753df83e0599ae3980`  
		Last Modified: Mon, 16 Dec 2024 18:29:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f961d2d7f8e87f86d1293b296ada65e0638952242c40b75eaa3b6b84b836a369`  
		Last Modified: Mon, 16 Dec 2024 18:29:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
