## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:aebdd1b1687e091bfce577add323a128c073b5f79af51f23731662b7b5cf9b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `hello-world:nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull hello-world@sha256:0b17a530fdd0e8684881b63c438df2aaeb46007b7e77c38849e4673f9788c4fb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196670941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59fdb5fdb01a6a77bdac2f7b50b0bb50f2d65de4bc7180f1c1964ecff8ee722`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 22:09:47 GMT
RUN cmd /S /C #(nop) COPY file:22c7ae19fd4cf03d26e9cf1357869206bf69101c4233df05ad5f8fa29b73cde4 in C: 
# Tue, 09 Jun 2026 22:09:49 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c28e3c357614599fe7a4aeec98c41370f6590a1ff0604415a2f2f0ca95e1b18`  
		Last Modified: Tue, 09 Jun 2026 22:09:53 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2e4e8bbf2a44bb5dc18c759f1c7402625f81bca2e6d32480262ad66349fb69`  
		Last Modified: Tue, 09 Jun 2026 22:09:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull hello-world@sha256:cb7a9f2d231a3f1c93227767970df3a53621a08e5ef7dcf39d76c2641ab630a1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124000387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d05c5c0c2835542782c1d1859fa25da5f59069f7b3ed452edc49f42bcc2692`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 22:06:57 GMT
RUN cmd /S /C #(nop) COPY file:9fca1d3c77d0758894ceeb7952e49e3b465b238dc4943832e9436b0ce84d8ae0 in C: 
# Tue, 09 Jun 2026 22:06:58 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1ccfd3f345050494d641d679284224b2e09337cafaa19feb8dff1150225759`  
		Last Modified: Tue, 09 Jun 2026 22:07:03 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28146915d6e33ee35127783b01a40faed677e34f318b4b9d0b7c44ae57e1417`  
		Last Modified: Tue, 09 Jun 2026 22:07:03 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
