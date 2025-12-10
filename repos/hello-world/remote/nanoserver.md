## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:071ab0242218e5ff125cfff8835d65375cf18d4b42e1df9eb0793a2af70aafe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.7462; amd64

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

### `hello-world:nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull hello-world@sha256:bd384cb998fddc3689dacf6d8971714572d529ff40ef94c294f9d963a2c34894
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126361204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e726fb2f74e5a885ba2b26c9bfd5b6bfbfcc4efebbeb8ab5c806e101a029775`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 20:31:03 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 09 Dec 2025 20:31:04 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f032cf60b93275d5e414ae5399172e24927a8db9c16ce206fc4c43ab19e32fc3`  
		Last Modified: Tue, 09 Dec 2025 20:32:08 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b7cf4439b052eee4164d6536e132dee6144721c3f1ce4e7c016275d3974b5f`  
		Last Modified: Tue, 09 Dec 2025 20:32:08 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
