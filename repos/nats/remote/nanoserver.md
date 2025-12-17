## `nats:nanoserver`

```console
$ docker pull nats@sha256:e3f11ca827549acc0b7087d277bb9a9d27a06d53d8ed9ebf3017e4de574d1407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `nats:nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull nats@sha256:5ade3b8097e2c50045d7cc5b9916a1321e3f818b0f69cc7a634875e82710b5d9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683da254fb63f0c8cc5b83a6a6886eb0b42cb4d1d93a9428bb4501e1916755e9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 20:08:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 17 Dec 2025 20:08:32 GMT
RUN cmd /S /C #(nop) COPY file:ec94fa0a8d5bdb04f4e8f7e8ecc10a64d72990dc4ba8ddff1a8c14d23473ba63 in C:\nats-server.exe 
# Wed, 17 Dec 2025 20:08:33 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Wed, 17 Dec 2025 20:08:34 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 17 Dec 2025 20:08:35 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 17 Dec 2025 20:08:37 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4379c3ab1892caff9ef2f09d2151fe9c94acf23b255c7d428856217a4471cc26`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed88622b97e1e8bc58e7e06c582dabc0960f88c7867718f137df1317df14a43`  
		Last Modified: Wed, 17 Dec 2025 20:08:51 GMT  
		Size: 6.8 MB (6770883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7f74d617f9673094225d8b877378420e0abe0f0d053a55b42227c4e0372eb6`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f18ccfaa70090ed55b2ff35289f33e2afda0692a803f7d03dcb5feb802997c9`  
		Last Modified: Wed, 17 Dec 2025 20:08:51 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1199736a2361291ce2d46dd331a637415989e45930d7911bd7e1938535b12ada`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed3a3fa4f1b13762dd50df7e973f336fd8d84b4d13104f77f04454e3e7615b4`  
		Last Modified: Wed, 17 Dec 2025 20:08:50 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
