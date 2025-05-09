## `archlinux:base`

```console
$ docker pull archlinux@sha256:69b59e60bb8594d8c4bf375e9beee186e4b3426ec4f50a65d92e7f36ce5e7113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:7bf13b5de35200fbc4e64f74b7b74782d1068bc4a7019381d2983ea3b71a1f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161580789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c2117862d04d95c551515deee031a56b589fa1d13f4223858a351c75f427a9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=20250504.0.344409
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.created=2025-05-04T00:08:01+00:00
# Sun, 04 May 2025 00:08:02 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 May 2025 00:08:02 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250504.0.344409' /etc/os-release # buildkit
# Sun, 04 May 2025 00:08:02 GMT
ENV LANG=C.UTF-8
# Sun, 04 May 2025 00:08:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53e65e421f390a4ddef417d1c5ea3e02bb1e98c8d2a12779335b0d252f2a0311`  
		Last Modified: Mon, 05 May 2025 17:13:57 GMT  
		Size: 161.6 MB (161572423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53740aa99073ca367479dd64dee910d0d8ad6e03b48785038e52e252a17fefe`  
		Last Modified: Mon, 05 May 2025 17:13:54 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:4db6649f7e3ffed2be05272e2c83987d7d43f4059167fd3c1d71766d683eb362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8177457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d621a467d1ec2908bf6c75381b3bdf03b7723923ac5f85a49d4ec7e7f496046`

```dockerfile
```

-	Layers:
	-	`sha256:7787c22739917a182ebd717cbe4dbc838ec4d80d09ed03def0833ae18a880f0b`  
		Last Modified: Mon, 05 May 2025 17:13:54 GMT  
		Size: 8.2 MB (8165485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10a0529c9495987f40e35f37d84f2651652a6b4aed686e99be931eeb2806b5c`  
		Last Modified: Mon, 05 May 2025 17:13:54 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
