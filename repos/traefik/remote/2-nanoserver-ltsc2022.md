## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
