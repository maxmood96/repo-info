## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:d10f0658f146b95d0074a4049f5e70ef2a71309ec915accea72c08acbd150277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats@sha256:c7c3008b235ba7371658005fce3b99cfcc3e20604e0615b8817c17fe3be19f25
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110067654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073d374029e934d9326ad3a424679d8fb28d99ebcdc0f62bea25034ca3e5ae2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 09 Nov 2023 23:18:12 GMT
RUN cmd /S /C #(nop) COPY file:dbbf376643d913f572787dfa3a580d012b8bc2c35e2734d995eec070a00ee72a in C:\nats-server.exe 
# Thu, 09 Nov 2023 23:18:13 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 09 Nov 2023 23:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 09 Nov 2023 23:18:15 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
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
	-	`sha256:6bdb3c80faa7a9b87096f6b91694eb3403487feb0fec4acb53c66627dc4ac577`  
		Last Modified: Thu, 09 Nov 2023 23:19:18 GMT  
		Size: 5.6 MB (5596996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a6c4993f5bb38761ec70e523e232652cf2c44d6124667a0ba51bf6d5a6a71a`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d5c7c41494b9e7b4970fd59ce28bec611cecba9285d585c671054641204980`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7c5ecf8f67cc47df2c34b09fcb0007651a3a83db35a6bc1b2e7ebb256336f`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c94799892c4a046bd59f9299b44616f27658d4afbd6e1bfae9e323c5088926`  
		Last Modified: Thu, 09 Nov 2023 23:19:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
