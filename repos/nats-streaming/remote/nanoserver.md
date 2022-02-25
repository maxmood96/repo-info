## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:8b491322c8ffd9bf3a1601284c03e767da655c349ab692aeac5e48c237c9ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats-streaming@sha256:869d74ad56522c6b9a695cd1db6d5c2d5789b67ac3abc60ef7486db75c5db40d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110269675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5932d54e1864e9f49901b4c39dfe687232bf2b59e8ecfd3242b36ad57e523536`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Feb 2022 02:20:56 GMT
RUN cmd /S /C #(nop) COPY file:e7d7513784103e13d5583158634b243440959de7cdfaf3602d16eec752946fe4 in C:\nats-streaming-server.exe 
# Fri, 25 Feb 2022 02:20:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Fri, 25 Feb 2022 02:20:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Fri, 25 Feb 2022 02:21:01 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5030a6d1fb6074f83ecd43d63329d1ce9e47ce7abb822efe4b048525348294`  
		Last Modified: Fri, 25 Feb 2022 02:21:56 GMT  
		Size: 7.2 MB (7177970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68877bcb599a81befa9c6441501d142f7669207fa0787cee6e74f4ae3cb5aad`  
		Last Modified: Fri, 25 Feb 2022 02:21:55 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91344cbf81e04fb8ef879b3a388d8fcaa65d3a70106bd7f96b8954c9564cee32`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab42220f2fa6e2a4c6b6d10260b5cd783c0ba3cfdd4ff423484667ee782017e`  
		Last Modified: Fri, 25 Feb 2022 02:21:54 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
