## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:e2592ac7f8a0ec2f7bb7903e471dd9f947e03018d49ea14174d7f443ebe3c611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2227; amd64

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

### `hello-world:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull hello-world@sha256:741e985f49fc0777c7cb5d3a0018a303e6180b4b4a55b782906b716b24c8183d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104594159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5274654dc3e47cfb4314fdf6c0317c74bece1fd669987020e21b994b1dbcd658`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 23:56:11 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Wed, 10 Jan 2024 23:56:14 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1304b27db90c80a187cd20ffe7f0976ccf18928e2fd1c9379825166b2cacd5`  
		Last Modified: Wed, 10 Jan 2024 23:56:18 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b7cb9bd34cc785c5cbd8b8e3924d8b027a9629a20e976f70008085100d6e01`  
		Last Modified: Wed, 10 Jan 2024 23:56:18 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
