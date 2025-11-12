## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:60724e738c7ed9116b0cca972040b6aafd2762d2f572afaa54a40552a9fb62f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e2f55045c64078c084ef9e53f08adf1623aa8e844c0f61ac976e59ef978d66be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173790001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8318d8f6e397d73cc19da9686cd752741b871ca5e5f2833e0a36abe8a9cc2547`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:6cfeac02f7657e0f21bec793858fed4418e5818930327326190bd6ff11a7fa98 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae60a04a76082373387efad417e4554a5a8af770bbbcc040b0811829cdfbdb`  
		Last Modified: Tue, 11 Nov 2025 20:10:44 GMT  
		Size: 47.4 MB (47437742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36572591302f3f4ec803657efd9cf2a5635c524bf86800891e48499c6c83100d`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39e8d7bce4b204cc12e1d9ec388767ee42407e17c5751b6174c90b12e16df7`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ff038bfba1a92d3ca14cb7a8d0ee8597c094e3ef37614449e15e15bd0bd287`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
