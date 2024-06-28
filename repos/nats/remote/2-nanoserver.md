## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:d8ef048a0478de04fd69aed67045f9e0a3498e5b21737d6949d9f55512a43575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats@sha256:3088173a72ed6bdb8617e58772e28ea65bbc1c22a0407df35c408dffd9bff9b0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160844137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb42b3899eb57a01f61713f56274797e49d28cf8ff92770f3cd68c275ebbf9`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Jun 2024 00:19:03 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Jun 2024 00:19:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:19:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Jun 2024 00:19:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ec0a490db5fa23835f56b7cf9145b54661ae6b55dddc757f273f95b45eb7b1`  
		Last Modified: Fri, 28 Jun 2024 00:20:11 GMT  
		Size: 5.8 MB (5804528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0423c783ef9962598d614b4e7008e1ae06c2541e8e3c964abe28a43c293ad24f`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbe6f5c16ca5fa13cdde6b588d021ecae59dabb2e9454cb4b1776f599d33131`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f8f2602df06c6d97630e9b19afdcf9be119c492f29fb7a66cdc4bad743609`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8cd7e5db867da366c7ed8ad225e550c38304d0529e987a1491496f26a0c46`  
		Last Modified: Fri, 28 Jun 2024 00:20:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
