## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:2a203891b66309ab54ebe13061ab6f53e13fa186508eaee72c1af428ccbc6766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull traefik@sha256:66e891ac6c6673f7d10d457957a2d4ece7d9bdd774f1691cd06eb7d022f52dfe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164282745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085f8373d26b702313a979a98f003f9daf4385ddda92caa8e55ed46957c519b5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 01:15:13 GMT
RUN cmd /S /C #(nop) COPY file:821671f77390b8e204cb10fa63929da061450690e0c4bdca4cdd85b570cd0a98 in \ 
# Sat, 22 Jun 2024 01:15:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Sat, 22 Jun 2024 01:15:16 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Sat, 22 Jun 2024 01:15:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39788a8dce6271bdd79bdb0fe037977da8cbf1468f1652e8a02682a3c1107576`  
		Last Modified: Sat, 22 Jun 2024 01:17:18 GMT  
		Size: 43.8 MB (43779731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb3ec4fa80644938fb7a5ed74ddbaf88ed8e64ccc0384dbcfd2a9cef2592ab9`  
		Last Modified: Sat, 22 Jun 2024 01:17:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2aa3c6875713a563fea79c729c36b5ba627adbe6ef0e132be03806e294a8ce`  
		Last Modified: Sat, 22 Jun 2024 01:17:08 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd4b4ff9a5e5b275f5a870047cd464b8bd4887566a29dc59544e9cfc2fb3b41`  
		Last Modified: Sat, 22 Jun 2024 01:17:08 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
