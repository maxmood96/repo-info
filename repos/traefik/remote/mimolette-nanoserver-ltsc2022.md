## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
