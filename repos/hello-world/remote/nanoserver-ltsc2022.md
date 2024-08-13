## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:dd72d85efe397656e597ba9d1069451d5aabedd07996b2b65ba1de0780ef8224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2655; amd64

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
