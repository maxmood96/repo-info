## `hello-world:nanoserver-ltsc2025`

```console
$ docker pull hello-world@sha256:2c7c1e0501285adddc340920c0f021add7aed7dd57617869b202e64d2c764750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `hello-world:nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull hello-world@sha256:8624e61fae32dc716d33d40f9c075b7245246180a1969c81f4f66b8a3b0c7a32
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206305038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee339c49b8580808010e086f1004ea95f2be73ed8081539a8f4165ed901f2602`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 18:43:08 GMT
RUN cmd /S /C #(nop) COPY file:1ae3735b36d6b3fc6ef1fd1d2d12badf8f42ad5660d983c9a406cb560633ed37 in C: 
# Wed, 12 Mar 2025 18:43:09 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee25e6b4b5ae8dd36fe3e922969584cb067b792f3982c7c9bdb41e9f1e0bcfc5`  
		Last Modified: Wed, 12 Mar 2025 18:43:11 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd5076e2b282441244beee4e4a150361623dd814ad5c8d43a7768ebd2dc5e14`  
		Last Modified: Wed, 12 Mar 2025 18:43:11 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
