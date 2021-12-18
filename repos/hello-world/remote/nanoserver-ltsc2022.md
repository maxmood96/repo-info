## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:065f073b74b0f2780743842b3a3ecd7f44fa32122d07575392eba7120935aed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.405; amd64

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
