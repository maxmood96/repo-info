## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:ada835bdddc816507b1dc073531cc6be783404d26562e982cdc0b61f5eb48c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull hello-world@sha256:ce952296ef9195493ed5f57f0885158e6396a40168aba82652d834dba507fa04
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198876806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30999e09fab20707216ba994673dc62b0f2c4a7bd48814ee8fbab2415dabefe8`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:52 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 09 Dec 2025 20:32:53 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4baeaff99dfe83701483a83ecdbbfaa8a9e81163f4a3b3249946ae9d0b98de`  
		Last Modified: Tue, 09 Dec 2025 20:34:11 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5eefab9fd61a4b5d8adc16aa9bcf9c8ef1f61d7a7d350364fab2be889c32c`  
		Last Modified: Tue, 09 Dec 2025 20:34:10 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
