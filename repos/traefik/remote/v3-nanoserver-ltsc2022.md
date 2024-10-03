## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:1443add40fdc2f1a650f1d94824ffb94f07b60f036e4d351f7e7a20efadc4ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:f3194c289cb663880b291afbf05594e955469e1f2796dbbeabb0db6b954d4336
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166022749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1c815c0d5b99acc809f5dee05c21ca1a2553b65b56f432fea6c569ee136e4c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Thu, 03 Oct 2024 00:58:34 GMT
RUN cmd /S /C #(nop) COPY file:cf79ad93554c9371fa2365d20c4b4961c6591fa14cb598ea0e40091584b936fe in \ 
# Thu, 03 Oct 2024 00:58:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Thu, 03 Oct 2024 00:58:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Thu, 03 Oct 2024 00:58:37 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009e082b02ff94751264025a95f25ff1bdf1c7ac9b75e5bbfef9f2bc668b5e3b`  
		Last Modified: Thu, 03 Oct 2024 00:58:45 GMT  
		Size: 45.5 MB (45510103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa5a84fbffa511cf7655c4c06debad4121e4ac5d2f97be0e7210d7c2531060`  
		Last Modified: Thu, 03 Oct 2024 00:58:40 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf680b79f2ddf54c8c417d16fada5b1b1a2e13a420ffe37c0b902907d336ae4`  
		Last Modified: Thu, 03 Oct 2024 00:58:40 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aae033020393fbf2b44d7e37dcac58bfbd557aa26bd085146b1103d3312fe0c`  
		Last Modified: Thu, 03 Oct 2024 00:58:40 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
