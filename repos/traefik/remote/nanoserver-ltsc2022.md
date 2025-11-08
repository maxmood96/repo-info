## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:9ba619066561d8595c5910e9bda9cc2b676f8ca94094eb2d7f908ebab6753ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8428b2a417a3cf6d25b912471ce9b206b41ca0c7de760459311ab83500a5abb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171074558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c87aed50012d985b2ff0e00ac0aa60501ada4ccba1cfd43efacaeb6831b68f1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 18:23:43 GMT
RUN cmd /S /C #(nop) COPY file:fa7d458e5035cd7257a4fcca892af645f6a7bff0167a9a36ee2be323cba3aea8 in \ 
# Sat, 08 Nov 2025 18:23:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Sat, 08 Nov 2025 18:23:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Sat, 08 Nov 2025 18:23:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811af6cbc81fb1b41da2b7a4abbcd61444188d6fe668a8796dc8748c14107540`  
		Last Modified: Sat, 08 Nov 2025 18:24:40 GMT  
		Size: 48.4 MB (48387316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999e9b45a8c7d498c4316404374e593b225b45245b9c3836bc1242431b985dc7`  
		Last Modified: Sat, 08 Nov 2025 18:24:26 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5b4e5c40d7fd0b54fc80e75284e19fd9442702073eb957e33f0628e285ddda`  
		Last Modified: Sat, 08 Nov 2025 18:24:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d3ba691c74f6ec133df3c3e44686664b2fb36ff8c80d83256c9c55a80dc7a6`  
		Last Modified: Sat, 08 Nov 2025 18:24:26 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
