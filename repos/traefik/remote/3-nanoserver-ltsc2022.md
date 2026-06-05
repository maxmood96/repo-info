## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:8b8c14f129756727440028de02007e8ae023ca1e245feb492d3fde5b3c31d5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull traefik@sha256:cbc9fcf6ca35a6f3b69c7fb2b57e13a98bd7907d822a5ea0fa62289c4a00ced8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176229954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4703670ad0cd3669e57fe70dfd084f2b2ad2bc1299235bc7278bbc66e3867eba`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Fri, 05 Jun 2026 18:13:14 GMT
RUN cmd /S /C #(nop) COPY file:e6aec65eb5ab28dafbadd75287019158eef99295696a4efafe63533d7351ebac in \ 
# Fri, 05 Jun 2026 18:13:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 05 Jun 2026 18:13:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 05 Jun 2026 18:13:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769739cba9542ed5d439300075d41d0c112f1b0c4ecb96650f886f760721042`  
		Last Modified: Fri, 05 Jun 2026 18:14:01 GMT  
		Size: 49.2 MB (49187970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e66e313f80769ab91948280805d1d68e37dab9d5802445a6f130b8bdd618bab`  
		Last Modified: Fri, 05 Jun 2026 18:13:25 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535984791782c746b684c0d5d7afbda73853fd2b33e1933b3f5777b7859e67af`  
		Last Modified: Fri, 05 Jun 2026 18:13:25 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5fe6cc4502c23e2c36c79b58facce9a1d7225ac1eaef55e7e190d231c192d8`  
		Last Modified: Fri, 05 Jun 2026 18:13:25 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
