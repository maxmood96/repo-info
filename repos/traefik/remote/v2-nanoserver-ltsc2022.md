## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e185bddfaab8e25c819fb7aedbceffe6bd0cf56a2eb4753d10c465d66651489a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:344ffad50a2a7ae1a673a7a010a152ec444db4d2e6eb19ff0a3c82c84e08d57c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166768269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c1ac2ca68d818c75fca2b94e32a18b62ec881bbe150e622fd3265d0a2e55b6`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Mon, 16 Dec 2024 18:28:31 GMT
RUN cmd /S /C #(nop) COPY file:37f474eb9bc5dae068b4b1f193466e9d558012439d1659a86250ee9b0f22d119 in \ 
# Mon, 16 Dec 2024 18:28:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 16 Dec 2024 18:28:35 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Mon, 16 Dec 2024 18:28:36 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.16 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39418fd39b8962a3bf6899397dbba951e07ebbe2ec4c2dee8fd30e593f0f39d5`  
		Last Modified: Mon, 16 Dec 2024 18:28:44 GMT  
		Size: 46.2 MB (46163874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a847c4159b6bf260842711f2d9205137967c813905fe74ea89ada1412b5f54d4`  
		Last Modified: Mon, 16 Dec 2024 18:28:38 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9444dfa615084ddd29287c2999bafcc66af67aaa4a7418cdf1d41b5aa9c4247`  
		Last Modified: Mon, 16 Dec 2024 18:28:38 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cd4764f92f8ead03cd5c7ae8dea994a12538c9fae4ee0c21fac62a6febd8b9`  
		Last Modified: Mon, 16 Dec 2024 18:28:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
