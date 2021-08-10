## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:a89668ac3ed7efc673020decb0aae522701c91eddd726017cdbdd3456c1bb41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull hello-world@sha256:878de8c32aeee732d7920efc309afb94290b94ecbf6bca540b93f4f008056540
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102728640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b3ffb9ef8150b301fb9b06900f278b584e1029d4b749acc8d0f12f1ee6994`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Tue, 10 Aug 2021 16:57:19 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Tue, 10 Aug 2021 16:57:21 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:df42b97aefe3dbe977a4768c070df2231401cc96cec6e2c0484967215da7b5a1`  
		Last Modified: Tue, 10 Aug 2021 16:57:40 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6629793555fbbf230817f584f77c6ab4f1444cf7c73594fdcdb23cac36f724f`  
		Last Modified: Tue, 10 Aug 2021 16:57:40 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
