## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:1e378d508ee9f870fbe59f71b9d6630c38a3d6f49dddefae3a9e51f370b3dfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull hello-world@sha256:3522a799ae11b49426f6a60b3fcf3d249f21fbd3dc1dd346d8a49fe4f028b668
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104387036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85cba3cbe8963848476bf9c94a986bc929a290a01dd5e378ba0364c50cdaf7a`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 01:52:50 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Wed, 10 May 2023 01:52:51 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4067ea6171984d517ffbfbfc1b9a6e5fa4cc931a5315d953e9b8697524a5aaad`  
		Last Modified: Wed, 10 May 2023 01:53:12 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0488e025553d34358768c43e24b1954e0056ec4700883252c74f3eec273016`  
		Last Modified: Wed, 10 May 2023 01:53:12 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
