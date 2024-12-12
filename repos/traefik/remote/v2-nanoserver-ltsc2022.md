## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:b331481e5979240517afd5da437300d4bd8d0036a734ca2a6fac5e4fc625a946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:8969a2088c3a157b79648cb31d95a9d681cb83692251c2673ebf3585474f7a9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166771602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37ab39777525cb7e92873f8065f8dc8f95552287286fe002462ca54db017d73`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:48:59 GMT
RUN cmd /S /C #(nop) COPY file:87185b296a51c23ba51e7f85f6c018d23e49d0fe423b2b39373ae759fd25a245 in \ 
# Wed, 11 Dec 2024 21:49:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Dec 2024 21:49:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Dec 2024 21:49:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.15 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ba3a747d308a93dae78ecf48587e9546ea0205baf76b87269f308afd1ff00`  
		Last Modified: Wed, 11 Dec 2024 21:49:12 GMT  
		Size: 46.2 MB (46167189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edb9be48c9f5bdf411fef0a73f81282e309532385462299233a7702ea21c2dc`  
		Last Modified: Wed, 11 Dec 2024 21:49:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b625d3f63089175ba5ee7d4d486919ce604c119fad95b2faad9c63e74d582a`  
		Last Modified: Wed, 11 Dec 2024 21:49:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd20521ecca56b197cddfea86d8d98781d5fe2102b1b32fa67ebd1bebf3b86be`  
		Last Modified: Wed, 11 Dec 2024 21:49:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
