## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:708247ec9df5fe168117b0a7f1e75c8e3e3d88a19ed35b7ba49ab611fc222e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull hello-world@sha256:0c2ccdb11489ee191e87a8b56efb724915b76e91b1907dd1279c30e6d1878e5a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (103017632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b29f50d39bbc02e868d9fbd1d664435b7d831ecb54b2e92bfd1bd3f2bc66b88`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 20:48:57 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Tue, 11 Jan 2022 20:48:59 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6a7a45351f0d35d3015a23e2b621cacc416d30540c7006ec26f9b48d1acaaf5a`  
		Last Modified: Tue, 11 Jan 2022 20:49:23 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536f5f58b451eb0054a1082a298cbc56130dcf021d91c38c7c42f05c5c38a5bc`  
		Last Modified: Tue, 11 Jan 2022 20:49:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
