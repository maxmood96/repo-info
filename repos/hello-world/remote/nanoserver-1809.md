## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:b74d7f282076cfc1cdf65e5350baa9f0db8be54e8f3f4a46e3f9427b1c02cf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull hello-world@sha256:7fed95756fe4ebeb6eb1d82c2176e0800a02807cc66fe48beb179e57c54ddcf1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101378292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70be230f9d1771cbcec3973b66f16b2ec90d823fb59826d9b7f5abd2bd8d68ac`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 May 2021 11:54:57 GMT
RUN Apply image 1809-amd64
# Wed, 12 May 2021 12:23:36 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 12 May 2021 12:23:37 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b9043d31610e0dfa43b1afe286f8918b6e3bf69ece50f44424b29d48f20aa662`  
		Size: 101.4 MB (101375240 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f304f50f8f74f0c6884dfb4fcb1ef139fe5836dbaa2b62eaacf119ad1a241e71`  
		Last Modified: Wed, 12 May 2021 12:23:53 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5367767660eced82c59d8fecdc3828ae5ad22032e06276eeb0368b77adb210`  
		Last Modified: Wed, 12 May 2021 12:23:53 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
