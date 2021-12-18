## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:d759e98428350fcbbe433305b6a6924c0783a54242c78d8b860c86cc066cbcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull hello-world@sha256:4f2d0f8b33a9b02060f61c85e247a79d7ce386b065bb7b00f7dbd2e072df7fc2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117228805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d446e6097f89d6b11a45127c18c7844db98c5e20d93e8e9dfdc29140863a7de`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Fri, 17 Dec 2021 23:50:45 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Fri, 17 Dec 2021 23:50:46 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d24add324b4827853695d32e1828d65b5b4875708e0e3e52b2d9ab7ed6456a40`  
		Last Modified: Fri, 17 Dec 2021 23:51:11 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa028ea82a4b91120f1e32988e49ea5a4c2a84b291bb63d07453053685966f3`  
		Last Modified: Fri, 17 Dec 2021 23:51:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.2366; amd64

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
