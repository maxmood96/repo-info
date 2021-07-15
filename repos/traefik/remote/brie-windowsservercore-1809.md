## `traefik:brie-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1c8a42e2baeb9bddde749c870a7358e27f7741967657c1e56f2f7ee6f766e65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `traefik:brie-windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull traefik@sha256:964801d74811184c560d846c28209ae6bb71c806f6caa61c23d5a05339b6614d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711616027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66254fc5f1c391011d0d22c96ab5802abe887137893f4e0e8ad45e107b4523c3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 02:41:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 18:23:54 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.0-rc2/traefik_v2.5.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 14 Jul 2021 18:23:58 GMT
EXPOSE 80
# Wed, 14 Jul 2021 18:24:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 14 Jul 2021 18:24:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dd3b24b55401566ea01a5005138a23766b6b6408c2276b7ebd097da01de80897`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cda26684f7afbfa917c5f6e75fa059b813158344ca5442ba212f025a8130e1`  
		Last Modified: Wed, 14 Jul 2021 18:28:00 GMT  
		Size: 26.2 MB (26163913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8105225b2b79a9ccf0b79667c4145afc9fe9eaad7f3186bf7a12f28c303754ab`  
		Last Modified: Wed, 14 Jul 2021 18:27:29 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94248e22f8579475e8e026a8a4a562fbe56b50a9042fb935f416a46518915462`  
		Last Modified: Wed, 14 Jul 2021 18:27:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928d7d2278ab8bf5f8437e895747fed10368bde8d8f3bf183cbeb2e004bfd23c`  
		Last Modified: Wed, 14 Jul 2021 18:27:30 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
