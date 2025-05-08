## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:ed3c0d9d70455b557db253fbb5bdc119d3fb419621a5ae381f3489ec1cbae4f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hello-world@sha256:d6e6504d7ec61ce1e15cd54d57838a2c036e25b2fb480026431cb67394a24b7f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190144889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7f5a332b02a3318f00c486150820a88ff07b04aab6eb00cc51d426f6b5aeb7`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 03:09:58 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Fri, 18 Apr 2025 03:10:00 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6908451bbaa87930c8e434a11632a47a055c5183c2267824d9e06dbf8cbad4f0`  
		Last Modified: Thu, 08 May 2025 17:49:13 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa3f6c7c371cc05ffeb51ab4a14006e4b907c90d370e4779ea8e0085f6d6b90`  
		Last Modified: Thu, 08 May 2025 17:49:13 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
