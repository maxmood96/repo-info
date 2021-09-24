## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:6130f3021a163a22b1f0ba256bb2699c9a4ed30369086c8a4fccff5544206cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:71c153413bf49b38806c3ad0c2a85c117380534d5d8587c9e930ad7061197323
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107323878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8917f61d9feda334e63e3bb8a7406359fccecff0aacc392edaf7b993af8e1f33`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 24 Sep 2021 18:18:25 GMT
RUN cmd /S /C #(nop) COPY file:e8e5cb48daba80f34796952e26cc4058ca5809e456780e196277b4f6b98248b9 in C:\nats-server.exe 
# Fri, 24 Sep 2021 18:18:26 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 24 Sep 2021 18:18:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 24 Sep 2021 18:18:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 24 Sep 2021 18:18:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a89e42bde9eba1e3c234a1b0fa3c923f6980959a141c870e6d8b49353b89c52`  
		Last Modified: Fri, 24 Sep 2021 18:22:59 GMT  
		Size: 4.6 MB (4613776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef71520d14dc0a4fa2ff138a03b2e1cba90e07a07e5d8a4095bf4939e740ecb4`  
		Last Modified: Fri, 24 Sep 2021 18:22:54 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd964bd5c073449877455885b3d3466daa9f611ce0979ea4c4fd13f8d586721`  
		Last Modified: Fri, 24 Sep 2021 18:22:54 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f529e09f796786e8eefc1792f39c3dcad6a7fb167fa5ead20c40310f632810`  
		Last Modified: Fri, 24 Sep 2021 18:22:54 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a619e9f3c2ad169084d8726e34725b9a6f47e3a0cbc88a2433a04b76b32e23`  
		Last Modified: Fri, 24 Sep 2021 18:22:54 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
