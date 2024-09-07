## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:20d51eae87b7b4bdb79092d4324db2fd3596230140e9b4b0c31e37d3ca936fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull traefik@sha256:05f4051af2d5551dbcf25cdd977fc0e4b73edfbd17d69378f8132006630c1fa3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291264114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2af8136b8175d1beca35d74f29ecbb8422718d02ede08af03b9d072350f6d25`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 06 Sep 2024 20:59:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Sep 2024 21:01:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.2/traefik_v3.1.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 06 Sep 2024 21:01:30 GMT
EXPOSE 80
# Fri, 06 Sep 2024 21:01:32 GMT
ENTRYPOINT ["/traefik"]
# Fri, 06 Sep 2024 21:01:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f4bd3a7ea81610492227b42617a56fc7782dd82e38fc78f210edf9c1820250`  
		Last Modified: Fri, 06 Sep 2024 21:01:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65bf1589830d4dbf3a2d261e0abbb410c129d918741c4bc1c3405187969c7f3`  
		Last Modified: Fri, 06 Sep 2024 21:01:41 GMT  
		Size: 46.1 MB (46055677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d69061135316e816ba538a92a787c2ebecc0aceb51673f93ab365a1e87b5853`  
		Last Modified: Fri, 06 Sep 2024 21:01:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2804a5889fcf065a155106e0c4d9bef732dbc356c83ade8005da5251a5bb7ccf`  
		Last Modified: Fri, 06 Sep 2024 21:01:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339258a6694696a52583805fc136439c4fb3df166adf1dede6839f14aa4d44c9`  
		Last Modified: Fri, 06 Sep 2024 21:01:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
