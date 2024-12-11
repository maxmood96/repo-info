## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:6e24782780819783fc6a496335734903f226f9ba8bd607bf24a9986705fc1f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull traefik@sha256:6ca13e933fdb9fa8dd4fcf7d44275ad94fd0435858b9658d14de0b435db70653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169517542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008ef70436d042afb280736441f0c79814258e5691b09bb37523351b65dadf83`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Tue, 10 Dec 2024 21:08:04 GMT
RUN cmd /S /C #(nop) COPY file:a4119dd5079022aea22363901b7dd6f116b350cca29b6618e55d06fc15514ce9 in \ 
# Tue, 10 Dec 2024 21:08:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 10 Dec 2024 21:08:07 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2024 21:08:08 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deab2faa1bbd13753d63f77c8ac358d8bb9152aed46ff0f06e77efce8547483e`  
		Last Modified: Tue, 10 Dec 2024 21:08:17 GMT  
		Size: 48.9 MB (48909510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02abb067afca497d74a28c21ce4870748122681636196ade70812181790181b4`  
		Last Modified: Tue, 10 Dec 2024 21:08:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b78e787149cf7de3bec84512d9436064aa3169400f5840552cb8152f4f063e3`  
		Last Modified: Tue, 10 Dec 2024 21:08:10 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cad704e9a6650085369ace679ff24586e5948fe79a344fe158a9dcc29160cb`  
		Last Modified: Tue, 10 Dec 2024 21:08:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
