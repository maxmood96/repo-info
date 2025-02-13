<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250209.0.306557`](#archlinuxbase-202502090306557)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250209.0.306557`](#archlinuxbase-devel-202502090306557)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250209.0.306557`](#archlinuxmultilib-devel-202502090306557)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:500a80b2efee7d810e0b5f231bb203174c204de929fe70ad18a952f5fb2504ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:e45ad60acc53d4b59ef4ef287721cf7a03e09525eeb407d15acef975b847ab30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157673375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d7641ec32ea96a101fba460d75040d06fc91768e479650165a49b7c2d836ee`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c4ce51beea9c3c5783dd11628e243d1c6679951a48f0168e07d67ad3ff6c26c7`  
		Last Modified: Mon, 10 Feb 2025 20:48:58 GMT  
		Size: 157.7 MB (157665076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e8c6f7906d1f823cf8cd1133a338637ec242c7055e3fe5c45a52240a887c5`  
		Last Modified: Mon, 10 Feb 2025 20:49:42 GMT  
		Size: 8.3 KB (8299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:921e3c3ca334102239da4131faff12e312849f04b3f35d1f84b586f204a62d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e96cb4fb96fa344686dd4bcd7fc972a9ff310a266e0003f6d25cb6ea2df0da`

```dockerfile
```

-	Layers:
	-	`sha256:37d9e99e17a41ef4d7334843f98f8ddbf008673b6f484652b402477b4fb2a0e2`  
		Last Modified: Thu, 13 Feb 2025 17:23:04 GMT  
		Size: 8.1 MB (8089059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a1e50b70d8cf398e003d7835141cb769554d1686e03d8631495b52606175b8`  
		Last Modified: Tue, 11 Feb 2025 05:49:13 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250209.0.306557`

```console
$ docker pull archlinux@sha256:500a80b2efee7d810e0b5f231bb203174c204de929fe70ad18a952f5fb2504ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250209.0.306557` - linux; amd64

```console
$ docker pull archlinux@sha256:e45ad60acc53d4b59ef4ef287721cf7a03e09525eeb407d15acef975b847ab30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157673375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d7641ec32ea96a101fba460d75040d06fc91768e479650165a49b7c2d836ee`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c4ce51beea9c3c5783dd11628e243d1c6679951a48f0168e07d67ad3ff6c26c7`  
		Last Modified: Mon, 10 Feb 2025 20:48:58 GMT  
		Size: 157.7 MB (157665076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e8c6f7906d1f823cf8cd1133a338637ec242c7055e3fe5c45a52240a887c5`  
		Last Modified: Mon, 10 Feb 2025 20:49:42 GMT  
		Size: 8.3 KB (8299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250209.0.306557` - unknown; unknown

```console
$ docker pull archlinux@sha256:921e3c3ca334102239da4131faff12e312849f04b3f35d1f84b586f204a62d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e96cb4fb96fa344686dd4bcd7fc972a9ff310a266e0003f6d25cb6ea2df0da`

```dockerfile
```

-	Layers:
	-	`sha256:37d9e99e17a41ef4d7334843f98f8ddbf008673b6f484652b402477b4fb2a0e2`  
		Last Modified: Thu, 13 Feb 2025 17:23:04 GMT  
		Size: 8.1 MB (8089059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a1e50b70d8cf398e003d7835141cb769554d1686e03d8631495b52606175b8`  
		Last Modified: Tue, 11 Feb 2025 05:49:13 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:d35892b93859c4170d753fe7efdd98b4f38c9d4539435e9bab71d1ccc9ab0483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f5e17fd8666fe0d4432ea83289ece234312368a8c5cc2c2f7a23d7c7e1abf147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278801050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3df05114946e71bcb5db0623d86d7e7a9a1273d084c1dc1b76ab624d60324`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:597f8ce19d766bcdf33ec6a6ec4f60bc434037a9a9efc05adab134ffa7dd739a`  
		Last Modified: Mon, 10 Feb 2025 20:50:42 GMT  
		Size: 278.8 MB (278792008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b222395fbe2616d512cc313813a661864b31323d3f0ec9883e4943b3f7c2d37c`  
		Last Modified: Mon, 10 Feb 2025 20:50:07 GMT  
		Size: 9.0 KB (9042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8eaeda8723c8a1156cc2dee3dec8820a770bb14047abb2d16601a5a392e6ff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae86713e6adf9e81b8380fcadb96457ded4d366f83832e85a24b15ad3443ca2`

```dockerfile
```

-	Layers:
	-	`sha256:e313ac902394ecdd87f7ed42a8194660134c93c8095d1742100c091e1607fa13`  
		Last Modified: Tue, 11 Feb 2025 07:41:55 GMT  
		Size: 11.9 MB (11896538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cdd40f761b97830706c748190103ecd552bfb753aeaf7bc5c3e5873a6d4cb9`  
		Last Modified: Tue, 11 Feb 2025 09:01:16 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250209.0.306557`

```console
$ docker pull archlinux@sha256:d35892b93859c4170d753fe7efdd98b4f38c9d4539435e9bab71d1ccc9ab0483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250209.0.306557` - linux; amd64

```console
$ docker pull archlinux@sha256:f5e17fd8666fe0d4432ea83289ece234312368a8c5cc2c2f7a23d7c7e1abf147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278801050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3df05114946e71bcb5db0623d86d7e7a9a1273d084c1dc1b76ab624d60324`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:597f8ce19d766bcdf33ec6a6ec4f60bc434037a9a9efc05adab134ffa7dd739a`  
		Last Modified: Mon, 10 Feb 2025 20:50:42 GMT  
		Size: 278.8 MB (278792008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b222395fbe2616d512cc313813a661864b31323d3f0ec9883e4943b3f7c2d37c`  
		Last Modified: Mon, 10 Feb 2025 20:50:07 GMT  
		Size: 9.0 KB (9042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250209.0.306557` - unknown; unknown

```console
$ docker pull archlinux@sha256:8eaeda8723c8a1156cc2dee3dec8820a770bb14047abb2d16601a5a392e6ff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae86713e6adf9e81b8380fcadb96457ded4d366f83832e85a24b15ad3443ca2`

```dockerfile
```

-	Layers:
	-	`sha256:e313ac902394ecdd87f7ed42a8194660134c93c8095d1742100c091e1607fa13`  
		Last Modified: Tue, 11 Feb 2025 07:41:55 GMT  
		Size: 11.9 MB (11896538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cdd40f761b97830706c748190103ecd552bfb753aeaf7bc5c3e5873a6d4cb9`  
		Last Modified: Tue, 11 Feb 2025 09:01:16 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:500a80b2efee7d810e0b5f231bb203174c204de929fe70ad18a952f5fb2504ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e45ad60acc53d4b59ef4ef287721cf7a03e09525eeb407d15acef975b847ab30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157673375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d7641ec32ea96a101fba460d75040d06fc91768e479650165a49b7c2d836ee`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c4ce51beea9c3c5783dd11628e243d1c6679951a48f0168e07d67ad3ff6c26c7`  
		Last Modified: Mon, 10 Feb 2025 20:48:58 GMT  
		Size: 157.7 MB (157665076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e8c6f7906d1f823cf8cd1133a338637ec242c7055e3fe5c45a52240a887c5`  
		Last Modified: Mon, 10 Feb 2025 20:49:42 GMT  
		Size: 8.3 KB (8299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:921e3c3ca334102239da4131faff12e312849f04b3f35d1f84b586f204a62d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e96cb4fb96fa344686dd4bcd7fc972a9ff310a266e0003f6d25cb6ea2df0da`

```dockerfile
```

-	Layers:
	-	`sha256:37d9e99e17a41ef4d7334843f98f8ddbf008673b6f484652b402477b4fb2a0e2`  
		Last Modified: Thu, 13 Feb 2025 17:23:04 GMT  
		Size: 8.1 MB (8089059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a1e50b70d8cf398e003d7835141cb769554d1686e03d8631495b52606175b8`  
		Last Modified: Tue, 11 Feb 2025 05:49:13 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:99ef0cdee7a0a6fc5b75e0161a0df351cf2346c470ffdf441b31184c3e34aeac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:796848981fcaecd6c813511ef4ddedb760551a5e96b6733ca61a8096778b05c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328815904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a708a49e93e712a9348ee8c9f4eff429a0d9c653ba4e62e3b7bfc2c0862c11`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:61c8fceafc7f0cdee9f810aaad8a75bd636d2b072b8452854e73c7c6f001b2c0`  
		Last Modified: Mon, 10 Feb 2025 21:05:30 GMT  
		Size: 328.8 MB (328805658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1c112cbef5f8327a79e16e83f249659b9bc4892c80fac781df8687965444f8`  
		Last Modified: Mon, 10 Feb 2025 21:05:19 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:97630311ffdd0fb5af4fcbf1829ffe91130322f79f395c811a0eaedf57524a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6e9545b31c45aa124916e93c02f42ed4e9e8ece4af2e8273323e2f480e983a`

```dockerfile
```

-	Layers:
	-	`sha256:eead521916ca67a28a7a761d802c8c64c0db9d5e235fc77b77d0127f4010d077`  
		Last Modified: Tue, 11 Feb 2025 09:01:16 GMT  
		Size: 12.2 MB (12165053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fc9e7c2cc63c105ee8aa59dd68eb15d7bd136027cfac645a94c000eeb737e7`  
		Last Modified: Mon, 10 Feb 2025 19:29:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250209.0.306557`

```console
$ docker pull archlinux@sha256:99ef0cdee7a0a6fc5b75e0161a0df351cf2346c470ffdf441b31184c3e34aeac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250209.0.306557` - linux; amd64

```console
$ docker pull archlinux@sha256:796848981fcaecd6c813511ef4ddedb760551a5e96b6733ca61a8096778b05c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328815904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a708a49e93e712a9348ee8c9f4eff429a0d9c653ba4e62e3b7bfc2c0862c11`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:61c8fceafc7f0cdee9f810aaad8a75bd636d2b072b8452854e73c7c6f001b2c0`  
		Last Modified: Mon, 10 Feb 2025 21:05:30 GMT  
		Size: 328.8 MB (328805658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1c112cbef5f8327a79e16e83f249659b9bc4892c80fac781df8687965444f8`  
		Last Modified: Mon, 10 Feb 2025 21:05:19 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250209.0.306557` - unknown; unknown

```console
$ docker pull archlinux@sha256:97630311ffdd0fb5af4fcbf1829ffe91130322f79f395c811a0eaedf57524a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6e9545b31c45aa124916e93c02f42ed4e9e8ece4af2e8273323e2f480e983a`

```dockerfile
```

-	Layers:
	-	`sha256:eead521916ca67a28a7a761d802c8c64c0db9d5e235fc77b77d0127f4010d077`  
		Last Modified: Tue, 11 Feb 2025 09:01:16 GMT  
		Size: 12.2 MB (12165053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fc9e7c2cc63c105ee8aa59dd68eb15d7bd136027cfac645a94c000eeb737e7`  
		Last Modified: Mon, 10 Feb 2025 19:29:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
