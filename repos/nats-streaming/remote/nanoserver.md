## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:f3fa9bfcd019cde80a83f2a8e2f9e1e985b7c37692940a245be4adee5f0b17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
