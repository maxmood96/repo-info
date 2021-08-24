## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:48cf68b8b3953e4be638025543a554887b3e713c643625dfb498b3ddaa12f654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `hello-world:nanoserver` - windows version 10.0.17763.2114; amd64

```console
$ docker pull hello-world@sha256:07ec39351767b7d0453681761b5a7e1bbc98b71243ad5db8481af4700f7cc06e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102744045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28fe36778ca0922caa485b2e9806ccf9d54b01335d864b982c01ed44d818b57`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Tue, 24 Aug 2021 21:25:14 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Tue, 24 Aug 2021 21:25:15 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:05195f776ba0409999d1706c657306f4211968e517659c36ba63f31fdc7be28b`  
		Last Modified: Tue, 24 Aug 2021 21:25:27 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25ffb73067bcad016459a12d2377ae89ce1c2c2e7ab4d4e86598a31915009e8`  
		Last Modified: Tue, 24 Aug 2021 21:25:27 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
