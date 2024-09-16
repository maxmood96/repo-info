## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:5c765150f1cad66afd76a99baa7eb92ebe37799952685505b6192eef5dde7db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:4acda14e03949ae6a31f8fe29045b1f0fa7f127c37fc515d2e2dea4206e0b822
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1508188895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420bddd2ab15c1ee37d912010ea1302c4def9599d720cc22623d11d2c020ea07`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Mon, 16 Sep 2024 18:57:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Sep 2024 18:58:54 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 16 Sep 2024 18:58:56 GMT
EXPOSE 80
# Mon, 16 Sep 2024 18:58:56 GMT
ENTRYPOINT ["/traefik"]
# Mon, 16 Sep 2024 18:58:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa3d74ba1831fb711d16207ff0850e7b5455481a01702b8e85b2c66519810b4`  
		Last Modified: Mon, 16 Sep 2024 18:59:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53a04da544c46a1869b2f51792dae30e80d94eb3b12d8ac1f23b4b0af3bdc1e`  
		Last Modified: Mon, 16 Sep 2024 18:59:06 GMT  
		Size: 46.0 MB (45991349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9117086cd7111174cba13ceaf5cce0ea454a94d9f8e7836af605dac272f88439`  
		Last Modified: Mon, 16 Sep 2024 18:59:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097831d10e229ccd002a44706677b423a9d5a8995cd28cf4858b42078993e584`  
		Last Modified: Mon, 16 Sep 2024 18:59:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5751a43928bbdd2d071e4dcecea76cbc2c2f66de7e00d0ba9f26574d2611ec9d`  
		Last Modified: Mon, 16 Sep 2024 18:59:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
