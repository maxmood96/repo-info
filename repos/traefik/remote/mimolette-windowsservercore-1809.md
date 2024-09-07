## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:ef814f43bdba4128e711813c3ba68171a5eb17c624723abd7ca32802cf25922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull traefik@sha256:b226a9537937c7887d5203cf23f558d4c21d6a3e99ca1144c2a62c1b23f9bd26
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289676661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42545f8247f19406cbb1b97c924b6ba74553bc9e8d3a56815f2ccfaf029f1ffb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 06 Sep 2024 20:59:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Sep 2024 21:00:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 06 Sep 2024 21:00:42 GMT
EXPOSE 80
# Fri, 06 Sep 2024 21:00:43 GMT
ENTRYPOINT ["/traefik"]
# Fri, 06 Sep 2024 21:00:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d9731856039331f789c9b6d545d44cf1423d8bff843366fea349a2410896a030`  
		Last Modified: Fri, 06 Sep 2024 21:00:48 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b95b75282ffb18100eba2b499642f01c71e73a18c0b418a94585b75850786f`  
		Last Modified: Fri, 06 Sep 2024 21:00:53 GMT  
		Size: 44.5 MB (44468037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524750f170c0db3a3d900787278f1d1815b7466e8e9ec670514081b8b4dde261`  
		Last Modified: Fri, 06 Sep 2024 21:00:48 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e363ed8c966eeec220e65961baead256be1c84a5f35d0bf07558048d61e7b045`  
		Last Modified: Fri, 06 Sep 2024 21:00:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8e4c7a04fce9d21d81807525c0a9e0b220609f46d764433276b47ae9d2fd43`  
		Last Modified: Fri, 06 Sep 2024 21:00:48 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
