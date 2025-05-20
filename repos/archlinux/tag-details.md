<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250518.0.352066`](#archlinuxbase-202505180352066)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250518.0.352066`](#archlinuxbase-devel-202505180352066)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250518.0.352066`](#archlinuxmultilib-devel-202505180352066)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:c0965d07320c79ca2e3a1cc9e303757f6b0055aa0437571523f5eedf78b15690
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9fa258bd0dfa27b6993d28acb34832a3f94d9ef61d3357c8c73117508b17b21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162330911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8174adfffde89ff3606b3c9753a9697d1870fef607c25c859c75f1e53258d4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:99a048503a97044f04b8022dcfd166a9e0637b56ea0e41796323764dd2eb2749`  
		Last Modified: Tue, 20 May 2025 01:48:27 GMT  
		Size: 162.3 MB (162322547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fed4f35c8e48a595faf53bcb00201ec2e1e71c970b61ffd550806f06d9f5aa`  
		Last Modified: Mon, 19 May 2025 23:01:52 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0df1ba58b6cabe7c32dda56cd616d58a212c1ada0afb9477bc5b4e7eb780b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8180810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dcc064dd1543e1948df36b4d48bbfa2be02230bee38acfb546ba8cfbd9ffe0`

```dockerfile
```

-	Layers:
	-	`sha256:ed126e2bed0c7303d11f28253eeed2c730c5d1865aae101051e1dec326c113d0`  
		Last Modified: Tue, 20 May 2025 01:48:18 GMT  
		Size: 8.2 MB (8168839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330cc0794d0c91afa2f316bdfde947ddf7af56bb1ee4b19babef53802ebbf922`  
		Last Modified: Tue, 20 May 2025 01:48:18 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250518.0.352066`

```console
$ docker pull archlinux@sha256:c0965d07320c79ca2e3a1cc9e303757f6b0055aa0437571523f5eedf78b15690
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250518.0.352066` - linux; amd64

```console
$ docker pull archlinux@sha256:9fa258bd0dfa27b6993d28acb34832a3f94d9ef61d3357c8c73117508b17b21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162330911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8174adfffde89ff3606b3c9753a9697d1870fef607c25c859c75f1e53258d4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:99a048503a97044f04b8022dcfd166a9e0637b56ea0e41796323764dd2eb2749`  
		Last Modified: Tue, 20 May 2025 01:48:27 GMT  
		Size: 162.3 MB (162322547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fed4f35c8e48a595faf53bcb00201ec2e1e71c970b61ffd550806f06d9f5aa`  
		Last Modified: Mon, 19 May 2025 23:01:52 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250518.0.352066` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0df1ba58b6cabe7c32dda56cd616d58a212c1ada0afb9477bc5b4e7eb780b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8180810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dcc064dd1543e1948df36b4d48bbfa2be02230bee38acfb546ba8cfbd9ffe0`

```dockerfile
```

-	Layers:
	-	`sha256:ed126e2bed0c7303d11f28253eeed2c730c5d1865aae101051e1dec326c113d0`  
		Last Modified: Tue, 20 May 2025 01:48:18 GMT  
		Size: 8.2 MB (8168839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330cc0794d0c91afa2f316bdfde947ddf7af56bb1ee4b19babef53802ebbf922`  
		Last Modified: Tue, 20 May 2025 01:48:18 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f44a86aa1626ff15535a1f442f73c84e3319b6e420e6176118ad11f7e401378a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6413de4bb40c6c97e123f5e891790fe00997cd7c23167d43f80c9a5d3881a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287033912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a5211731e9cba4e31d1832e7d36d31927738b6895fa14440fe6d7cf8d053bc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:19e3d5faef4b620e1ec0e4b4de82122aae646a54d343f04ad69171021e3b66b2`  
		Last Modified: Tue, 20 May 2025 01:50:14 GMT  
		Size: 287.0 MB (287024711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad70d5d372d9f7670b6c2fba64439a2e2f61a07a7d6e7ad4cac20ffd1317f7`  
		Last Modified: Mon, 19 May 2025 23:02:35 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c4a1f95d9c45869f5338ae8558ec11b12af727a5bcd8074c46fb82d4beb62cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12041406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb95f4b99020eccdbb70256c6d0462c1559824987c699d3e3840e7d85b24e7b7`

```dockerfile
```

-	Layers:
	-	`sha256:f933c4c9dbbb10d2a33ebfcc6a4fff177ab27e31fbed3a233e42be180f15db28`  
		Last Modified: Tue, 20 May 2025 01:48:21 GMT  
		Size: 12.0 MB (12029652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43f79935b373bbc3e71f16fc18782ca266826631d0f926e8db844f369fc0924`  
		Last Modified: Tue, 20 May 2025 01:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250518.0.352066`

```console
$ docker pull archlinux@sha256:f44a86aa1626ff15535a1f442f73c84e3319b6e420e6176118ad11f7e401378a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250518.0.352066` - linux; amd64

```console
$ docker pull archlinux@sha256:6413de4bb40c6c97e123f5e891790fe00997cd7c23167d43f80c9a5d3881a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287033912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a5211731e9cba4e31d1832e7d36d31927738b6895fa14440fe6d7cf8d053bc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:19e3d5faef4b620e1ec0e4b4de82122aae646a54d343f04ad69171021e3b66b2`  
		Last Modified: Tue, 20 May 2025 01:50:14 GMT  
		Size: 287.0 MB (287024711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad70d5d372d9f7670b6c2fba64439a2e2f61a07a7d6e7ad4cac20ffd1317f7`  
		Last Modified: Mon, 19 May 2025 23:02:35 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250518.0.352066` - unknown; unknown

```console
$ docker pull archlinux@sha256:c4a1f95d9c45869f5338ae8558ec11b12af727a5bcd8074c46fb82d4beb62cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12041406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb95f4b99020eccdbb70256c6d0462c1559824987c699d3e3840e7d85b24e7b7`

```dockerfile
```

-	Layers:
	-	`sha256:f933c4c9dbbb10d2a33ebfcc6a4fff177ab27e31fbed3a233e42be180f15db28`  
		Last Modified: Tue, 20 May 2025 01:48:21 GMT  
		Size: 12.0 MB (12029652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f43f79935b373bbc3e71f16fc18782ca266826631d0f926e8db844f369fc0924`  
		Last Modified: Tue, 20 May 2025 01:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:c0965d07320c79ca2e3a1cc9e303757f6b0055aa0437571523f5eedf78b15690
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9fa258bd0dfa27b6993d28acb34832a3f94d9ef61d3357c8c73117508b17b21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162330911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8174adfffde89ff3606b3c9753a9697d1870fef607c25c859c75f1e53258d4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:99a048503a97044f04b8022dcfd166a9e0637b56ea0e41796323764dd2eb2749`  
		Last Modified: Tue, 20 May 2025 01:48:27 GMT  
		Size: 162.3 MB (162322547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fed4f35c8e48a595faf53bcb00201ec2e1e71c970b61ffd550806f06d9f5aa`  
		Last Modified: Mon, 19 May 2025 23:01:52 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0df1ba58b6cabe7c32dda56cd616d58a212c1ada0afb9477bc5b4e7eb780b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8180810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dcc064dd1543e1948df36b4d48bbfa2be02230bee38acfb546ba8cfbd9ffe0`

```dockerfile
```

-	Layers:
	-	`sha256:ed126e2bed0c7303d11f28253eeed2c730c5d1865aae101051e1dec326c113d0`  
		Last Modified: Tue, 20 May 2025 01:48:18 GMT  
		Size: 8.2 MB (8168839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330cc0794d0c91afa2f316bdfde947ddf7af56bb1ee4b19babef53802ebbf922`  
		Last Modified: Tue, 20 May 2025 01:48:18 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:3e0d60696c5547a50a2973ec087409a3712c17e2c4cd28c241efa29f70912884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3a13e725e9531e9b08a7f331b052ff266dd60d1c9ec1571544242858bf5a7519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338178797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2146ba73ddcf422fa9452e57c4ea9418427554ec25183a2d919ed34cc29397`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a21012c4ba1bc77de8e0135b54df240569dbf6ba848c9a05c8822b96015d4de8`  
		Last Modified: Tue, 20 May 2025 02:15:19 GMT  
		Size: 338.2 MB (338168487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2bbbc3a5c161afb5a25216d65ddbbaef0cc7b5e23ca7db4b74842eac0e1b72`  
		Last Modified: Mon, 19 May 2025 23:03:12 GMT  
		Size: 10.3 KB (10310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d7a37c0f32aa814e26f8e96d9d13e3e4f27db2499c6818d163556dfc1b4fda44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc28224d6ece19e3fc13da89edcd4a7b7445485ed32eb1ee4aa27f70c0556f6`

```dockerfile
```

-	Layers:
	-	`sha256:180cdd09d1b2721b993e70e5738471bcdf86e0e7439a6fe9f42c4fa94005de04`  
		Last Modified: Tue, 20 May 2025 01:48:25 GMT  
		Size: 12.3 MB (12298541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b2cf4b73a011536f69028e0a27896a6e4e8ff5b8c55b82935cd1150cbd8589`  
		Last Modified: Tue, 20 May 2025 01:48:25 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250518.0.352066`

```console
$ docker pull archlinux@sha256:3e0d60696c5547a50a2973ec087409a3712c17e2c4cd28c241efa29f70912884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250518.0.352066` - linux; amd64

```console
$ docker pull archlinux@sha256:3a13e725e9531e9b08a7f331b052ff266dd60d1c9ec1571544242858bf5a7519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338178797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2146ba73ddcf422fa9452e57c4ea9418427554ec25183a2d919ed34cc29397`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a21012c4ba1bc77de8e0135b54df240569dbf6ba848c9a05c8822b96015d4de8`  
		Last Modified: Tue, 20 May 2025 02:15:19 GMT  
		Size: 338.2 MB (338168487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2bbbc3a5c161afb5a25216d65ddbbaef0cc7b5e23ca7db4b74842eac0e1b72`  
		Last Modified: Mon, 19 May 2025 23:03:12 GMT  
		Size: 10.3 KB (10310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250518.0.352066` - unknown; unknown

```console
$ docker pull archlinux@sha256:d7a37c0f32aa814e26f8e96d9d13e3e4f27db2499c6818d163556dfc1b4fda44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc28224d6ece19e3fc13da89edcd4a7b7445485ed32eb1ee4aa27f70c0556f6`

```dockerfile
```

-	Layers:
	-	`sha256:180cdd09d1b2721b993e70e5738471bcdf86e0e7439a6fe9f42c4fa94005de04`  
		Last Modified: Tue, 20 May 2025 01:48:25 GMT  
		Size: 12.3 MB (12298541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b2cf4b73a011536f69028e0a27896a6e4e8ff5b8c55b82935cd1150cbd8589`  
		Last Modified: Tue, 20 May 2025 01:48:25 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
