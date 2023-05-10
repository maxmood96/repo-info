## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:f44e44eeed62b743f9625e68d81eb0603999fec0aa72f50ac0443585c822efa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull hello-world@sha256:85481f9fb05b83c912dfdec9cea6230f2df24e5dfde84a23def8915cec2519b5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120004383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9647def08f81a1e7f17be1e9f175de0dc2e89faee67abb632b23678d0ae5c3bc`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 05 May 2023 12:52:54 GMT
RUN Apply image 10.0.20348.1726
# Wed, 10 May 2023 01:52:45 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 10 May 2023 01:52:45 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:7d382efe6974b94c05000b6a95c1fd28e1b8bb3e81cc4592b2aa1cc46b90192c`  
		Last Modified: Wed, 10 May 2023 01:48:23 GMT  
		Size: 120.0 MB (120001338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5676adddfe3e97c749846cda04c1436991b6553980159199d45214f9e7b5b2`  
		Last Modified: Wed, 10 May 2023 01:53:06 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9037cf3c1764807c2d209c5a0b76957c9a1a0ea151831dcb516fcf5ebd895ce8`  
		Last Modified: Wed, 10 May 2023 01:53:06 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
