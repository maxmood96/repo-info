<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250504.0.344409`](#archlinuxbase-202505040344409)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250504.0.344409`](#archlinuxbase-devel-202505040344409)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250504.0.344409`](#archlinuxmultilib-devel-202505040344409)

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
		Last Modified: Thu, 08 May 2025 17:05:15 GMT  
		Size: 161.6 MB (161572423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53740aa99073ca367479dd64dee910d0d8ad6e03b48785038e52e252a17fefe`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
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

## `archlinux:base-20250504.0.344409`

```console
$ docker pull archlinux@sha256:69b59e60bb8594d8c4bf375e9beee186e4b3426ec4f50a65d92e7f36ce5e7113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250504.0.344409` - linux; amd64

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
		Last Modified: Thu, 08 May 2025 17:05:15 GMT  
		Size: 161.6 MB (161572423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53740aa99073ca367479dd64dee910d0d8ad6e03b48785038e52e252a17fefe`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250504.0.344409` - unknown; unknown

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

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:39c081e4dc9daf0ec65d013fa78f18b0003452002edbd01baedaf87efa66a9cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:edf6fa73a2df016545f2de3f583aaa55b5af04f208880101670f33509bd97c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286273018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ce695d356a0214533f6c3a01351d0d68fbe7dc3b0b2d2a0b5fc58ef53e73e8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:a4fd439567a9d24ca8781db745416caee4677d04a13f9d195223ae578eb21671`  
		Last Modified: Thu, 08 May 2025 17:21:36 GMT  
		Size: 286.3 MB (286263812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa4fcb1f89a3a7ecd401cce432f2b61bf7af1974ca9d8671fb89ad5d9224771`  
		Last Modified: Thu, 08 May 2025 17:05:06 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bbf0b33f53312c2ed65cbb6670515e5c6d3355143e1668dfa87caddabc481af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06e04ab7564cfc139eafb2a2a11dd3f3faaa082bfaa622ca76bb040357f3dc`

```dockerfile
```

-	Layers:
	-	`sha256:1b572c6fb90d2c20c4d7595612d9d5f172df82c824fbe5a0aaf1026bd5cdcc8c`  
		Last Modified: Mon, 05 May 2025 17:14:28 GMT  
		Size: 12.0 MB (12026280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb1c679a672423b2a482e59e3e2ed08816a5aa1f631bd21c02002458febfca0`  
		Last Modified: Mon, 05 May 2025 17:14:28 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250504.0.344409`

```console
$ docker pull archlinux@sha256:39c081e4dc9daf0ec65d013fa78f18b0003452002edbd01baedaf87efa66a9cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250504.0.344409` - linux; amd64

```console
$ docker pull archlinux@sha256:edf6fa73a2df016545f2de3f583aaa55b5af04f208880101670f33509bd97c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286273018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ce695d356a0214533f6c3a01351d0d68fbe7dc3b0b2d2a0b5fc58ef53e73e8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:a4fd439567a9d24ca8781db745416caee4677d04a13f9d195223ae578eb21671`  
		Last Modified: Thu, 08 May 2025 17:21:36 GMT  
		Size: 286.3 MB (286263812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa4fcb1f89a3a7ecd401cce432f2b61bf7af1974ca9d8671fb89ad5d9224771`  
		Last Modified: Thu, 08 May 2025 17:05:06 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250504.0.344409` - unknown; unknown

```console
$ docker pull archlinux@sha256:bbf0b33f53312c2ed65cbb6670515e5c6d3355143e1668dfa87caddabc481af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06e04ab7564cfc139eafb2a2a11dd3f3faaa082bfaa622ca76bb040357f3dc`

```dockerfile
```

-	Layers:
	-	`sha256:1b572c6fb90d2c20c4d7595612d9d5f172df82c824fbe5a0aaf1026bd5cdcc8c`  
		Last Modified: Mon, 05 May 2025 17:14:28 GMT  
		Size: 12.0 MB (12026280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb1c679a672423b2a482e59e3e2ed08816a5aa1f631bd21c02002458febfca0`  
		Last Modified: Mon, 05 May 2025 17:14:28 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:69b59e60bb8594d8c4bf375e9beee186e4b3426ec4f50a65d92e7f36ce5e7113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

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
		Last Modified: Thu, 08 May 2025 17:05:15 GMT  
		Size: 161.6 MB (161572423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53740aa99073ca367479dd64dee910d0d8ad6e03b48785038e52e252a17fefe`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

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

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:adcffcfea1c51f5eec3c4148eeaaed1ac97d679e9b25f0bd0ec4e22c13f48c8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:88ee1f24b14bc630da17d6dd53a6db50c79c1ea5e53596d2e0c55f5d935a51ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337450182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c68b54b5dfb52d74e02d11581f0577772c742313566db82cb8cc6086cd737e5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
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
	-	`sha256:a5e319f88d304e0213ee6c6ae459d746be69c6ef8cad6865299d35887f760047`  
		Last Modified: Thu, 08 May 2025 18:11:15 GMT  
		Size: 337.4 MB (337439881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5510fe49e46a4f921e21993c2caf96ecba65b6b58d1ce0c57681969c098510af`  
		Last Modified: Thu, 08 May 2025 18:11:02 GMT  
		Size: 10.3 KB (10301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a65d55931814a0f691ef7d7647dd1fd180734235ce6affb9b8b1007d6a35965e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12306626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec5d6a911da22bb86057ce9f722660343cdadd2f5e2c4aa0734f11509db80a`

```dockerfile
```

-	Layers:
	-	`sha256:c19a59b5ce9192c347f7ea77e44239b3ed06e441fa8b286adb21a00c7eed0894`  
		Last Modified: Mon, 05 May 2025 17:14:29 GMT  
		Size: 12.3 MB (12294815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e64278f3ade57a2949068a02551b1800b42334ff052856754dc969cdc5bd0b0`  
		Last Modified: Mon, 05 May 2025 17:14:29 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250504.0.344409`

```console
$ docker pull archlinux@sha256:adcffcfea1c51f5eec3c4148eeaaed1ac97d679e9b25f0bd0ec4e22c13f48c8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250504.0.344409` - linux; amd64

```console
$ docker pull archlinux@sha256:88ee1f24b14bc630da17d6dd53a6db50c79c1ea5e53596d2e0c55f5d935a51ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337450182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c68b54b5dfb52d74e02d11581f0577772c742313566db82cb8cc6086cd737e5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
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
	-	`sha256:a5e319f88d304e0213ee6c6ae459d746be69c6ef8cad6865299d35887f760047`  
		Last Modified: Thu, 08 May 2025 18:11:15 GMT  
		Size: 337.4 MB (337439881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5510fe49e46a4f921e21993c2caf96ecba65b6b58d1ce0c57681969c098510af`  
		Last Modified: Thu, 08 May 2025 18:11:02 GMT  
		Size: 10.3 KB (10301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250504.0.344409` - unknown; unknown

```console
$ docker pull archlinux@sha256:a65d55931814a0f691ef7d7647dd1fd180734235ce6affb9b8b1007d6a35965e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12306626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec5d6a911da22bb86057ce9f722660343cdadd2f5e2c4aa0734f11509db80a`

```dockerfile
```

-	Layers:
	-	`sha256:c19a59b5ce9192c347f7ea77e44239b3ed06e441fa8b286adb21a00c7eed0894`  
		Last Modified: Mon, 05 May 2025 17:14:29 GMT  
		Size: 12.3 MB (12294815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e64278f3ade57a2949068a02551b1800b42334ff052856754dc969cdc5bd0b0`  
		Last Modified: Mon, 05 May 2025 17:14:29 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
