## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:8bb14335a7fe847dd37927681763f44b3c646703380ad376de9001101f07f3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

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
