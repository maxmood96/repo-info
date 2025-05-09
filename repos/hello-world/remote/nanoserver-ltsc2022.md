## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:29d5bce0dd1e339887605d84ce5d1902adb95c1a88fc45e6aa0061d1b09e0f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hello-world@sha256:7a74da18f0e142334209634df1d0e8b7c423884cc16da82a8fde7426c44b92e8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122541860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455f68eb8b42e993433af79229d279932e9e5a856d0f71d328fc1db05f1e01b`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 03:09:12 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Fri, 18 Apr 2025 03:09:13 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dc116d63f2ec540b4e898c60abcadae4da7009ee12bd270b5cae20f0087787`  
		Last Modified: Fri, 18 Apr 2025 03:09:15 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3000f9622770d846efa587e7788c5a86f9de8ec512f0e8737d2619914d44a7b9`  
		Last Modified: Fri, 18 Apr 2025 03:09:15 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
