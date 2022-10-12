## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:a07fb469f7139a756e0d33384b3b44b5cf476b1fe5e7a6239863265fb6422952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull hello-world@sha256:7aef5136b6c5aa5cb38b504f3c5d1aa61b6ec6db2565ae81d705c10b49241167
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118205899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0eb300498435cbaa827ae2a85900e920dd9528c0a253ae6a07beb7b5fae99e`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 12:39:47 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 12 Oct 2022 12:39:48 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:38fa349577729651ac1fc3ec785f908719a8100da5f5ba9bd3f549411061f583`  
		Size: 118.2 MB (118202895 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cb2f9654ae65bd4aa50f3463f2d053025144322b599cc6506edf94170f1f170d`  
		Last Modified: Wed, 12 Oct 2022 12:40:11 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc05f03f8ab022e18841de9561dfccb6f6df66bd58150f7d0add0dda8f875a3`  
		Last Modified: Wed, 12 Oct 2022 12:40:11 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
