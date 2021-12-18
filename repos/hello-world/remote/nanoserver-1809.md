## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:ba9fab71ed8d71593100f1af95f92a17c1583a995f16c7e81337ebd91c7d2ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull hello-world@sha256:46a21998cde47ca95633cab560e54b651aac3107cbb05bdc687ffac8563aa18a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102907065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f11cb1edebc4b4ac6aaa8429376a4c41b1f737ab1a46e8db3756f06d450aac`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Fri, 17 Dec 2021 23:50:52 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Fri, 17 Dec 2021 23:50:52 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ec96c890c1cd609fafa3a17ff5a65b5b81784e219da36c9e01f208a02bb3d4de`  
		Last Modified: Fri, 17 Dec 2021 23:51:17 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61969d07207047a09497abbc2a38b37547ef2f07e84734f41affdc0215cf4f1`  
		Last Modified: Fri, 17 Dec 2021 23:51:17 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
