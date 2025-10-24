## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:54411d27bc5ebfedf81e98475fdb0c6255c613ebacf9b8ce79115bce29c968b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

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
