## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:101f6b637d2a2e39f61952d173e37a2f5c61d079bd121d96654433972010501c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

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
