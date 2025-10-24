## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:72b4d90c0c4cdf80c0b7b6af089fc6d4f92fb03e969cc7f8076590d864946210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull hello-world@sha256:960de3c5314cccc653a6f5e3d726e13b27f0ab97da841e4f15d56f0d4f2eb4cd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194032230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0187546a511a719273b170440b53639a70894422d904614a3c939ba029b79f1d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 18:09:31 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Fri, 24 Oct 2025 18:09:32 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280d7d96301291bc9842ac40c89a59de721705b0d627a6bdb38a45b4b1e7d340`  
		Last Modified: Fri, 24 Oct 2025 18:10:53 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b1f622854dda365402cb1b986f33fb862bf3d99bb05c84bf9a0d32b2054a99`  
		Last Modified: Fri, 24 Oct 2025 18:10:53 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull hello-world@sha256:fe5dda0eb196f0964e50d32f807c7d61396c8286fb42ce9b96881147653747d2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122686941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe8bf1bdc45d5e6f7c14224234c0696320cf7e06520c0524c122af2150d0b66`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 18:09:08 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Fri, 24 Oct 2025 18:09:10 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3498c9ab48b6d9ccb645ca29a02667d56b64f74617f8f16c3f695d39a2de1`  
		Last Modified: Fri, 24 Oct 2025 18:10:45 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2802b61b918b54c8232238b89e8b00319688d1471a95e7648f97097d1eea8fc5`  
		Last Modified: Fri, 24 Oct 2025 18:10:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
