## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
