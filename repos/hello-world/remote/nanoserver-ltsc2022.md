## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:863c112f63e7ef7e952c251cea13bd8970c1044596efc50f381ef2633e321f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull hello-world@sha256:06a89fb00097b4398c84a7ddb00b3d9fd220780d1a22ae10d0d40ba00d6d98a0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120772105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd32b7d762aa63c4eac3278f9e25b120553b089fdb74f95b698cb187620846d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:55:26 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 10 Jan 2024 23:55:27 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2e859f92b483fefffb388d625fab1cc8a14abc8a19fa85b61389a4845e89fa`  
		Last Modified: Wed, 10 Jan 2024 23:55:29 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ca34449f381e2e48667fcc9b8f5f5d24c1666b827d725b0d1965c31941af8d`  
		Last Modified: Wed, 10 Jan 2024 23:55:29 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
