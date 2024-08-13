## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:0c6aef1999f18f35a919f56c55c2a355fa14db78a3a05cc4b8c931d8b8229616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.2655; amd64

```console
$ docker pull hello-world@sha256:583785327c8bbe47925af2b9c0e784b82d714ece537abcf7f11a2cae3a0e7467
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120557701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0334a00320be1c1edf8e90c4a1797768bbddb0f91a8203b8fea8ff3b1e7380`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 20:02:38 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Tue, 13 Aug 2024 20:02:38 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e72f72584f3aeef79b49b7ccf62e4baa7daed7f22c45767a71234f413990e5`  
		Last Modified: Tue, 13 Aug 2024 20:02:40 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d6b6cf885c9eaaf687b2a048b2eb4ef599667738473f15e5bfcfbaa72988d`  
		Last Modified: Tue, 13 Aug 2024 20:02:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull hello-world@sha256:22d2e99f3bd1c5f6706995d3d76aa53fe25c49d6cd1e4dbfdd452d37b8d93fe5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155085886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22694920b31fa7cbbbaaf903b97cfe62a4949caae00f4756ec673d6a329d008c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 20:02:36 GMT
RUN cmd /S /C #(nop) COPY file:ab292695e43926d678c546efb98c5def57b169554a9718789f6d597045bc2114 in C: 
# Tue, 13 Aug 2024 20:02:37 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3888db953df238ded741089e208af46b29c213ce4d09ceeee40214d9047f22`  
		Last Modified: Tue, 13 Aug 2024 20:02:41 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab866df638435514bcf8a48e17dfe5f9cd1b591a8f6c509c4b566972b3605459`  
		Last Modified: Tue, 13 Aug 2024 20:02:41 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
