## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b95cd83b4ef718ea88bbf9b3d7294a8b916164b371e9d3f974a97f828ec1acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull traefik@sha256:541ae1e9789c9a89a79af3959c5afede30785a974710f7007fdd50280e0ae7e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176209098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3158cd91dc12ac21cdca4294322f3c01e38465ffda73dcc835073561afc38d28`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Wed, 22 Apr 2026 18:10:30 GMT
RUN cmd /S /C #(nop) COPY file:b35e689974aa5ed08c9a6cefce22de9abf653d6b1a0454599b5fa6bee6072c32 in \ 
# Wed, 22 Apr 2026 18:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 22 Apr 2026 18:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 22 Apr 2026 18:10:33 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61210426a3adb80fddfed5b1620d52d7a123eedc1020e231811b256593b1dd8a`  
		Last Modified: Wed, 22 Apr 2026 18:10:44 GMT  
		Size: 49.2 MB (49249973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5e43185b4205ffe97eceb011cf43ca5e5850c53db1b161145526d3d7e95bd9`  
		Last Modified: Wed, 22 Apr 2026 18:10:37 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace3a8aa1b605bfd8ec267f7c7df21133f0e2d4d5a6743fb5d8002b67b96f25e`  
		Last Modified: Wed, 22 Apr 2026 18:10:37 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008e8b258c8b17d6eeab65ded25f27b99e956a2558fd740801dfb6bfd7ab310b`  
		Last Modified: Wed, 22 Apr 2026 18:10:37 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
