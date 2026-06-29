<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260628.0.549485`](#archlinuxbase-202606280549485)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260628.0.549485`](#archlinuxbase-devel-202606280549485)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260628.0.549485`](#archlinuxmultilib-devel-202606280549485)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:d9abf957599bddf27955a0dd82b4457dcfaace50525bb773f6c7518f8015e7e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:cc54f12fae7c81bd0d1a38f1694b4c28ffc708b358dd5876ab77dde49d37925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131368828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435ed19930af3ee3bbecbface47941c8fd2a6e3985516ceeb61d2b3b3e78ab09`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.version=20260621.0.546891
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.created=2026-06-21T00:09:09+00:00
# Mon, 22 Jun 2026 19:45:05 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 19:45:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260621.0.546891' /etc/os-release # buildkit
# Mon, 22 Jun 2026 19:45:07 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:45:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ab5bfa2e5807a3c5c29f3e1ca9c37088a006dd7a0b85eaf01292209d76ecc57b`  
		Last Modified: Mon, 22 Jun 2026 19:45:32 GMT  
		Size: 131.4 MB (131360138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b870649fd58e8b1d400a4293bb484d7f462a736493ce0ac56fd2faa68f38ca8`  
		Last Modified: Mon, 22 Jun 2026 19:45:29 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:5023748da22f12ddc65821a144a7105c4d8cfd3a3926f021c82f3a27430b9ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8188301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65147f82d924d8f4af76fbbcc29ba1bcdc2e038bcf1464488fd31d86cf37864`

```dockerfile
```

-	Layers:
	-	`sha256:001bafb1448cc60f0138f0068135b43fffb51a1bcdf6e408e28729ba3d3443ce`  
		Last Modified: Mon, 22 Jun 2026 19:45:29 GMT  
		Size: 8.2 MB (8176372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57e136ab266c57d7367c6134d5c3b6902eaf48ca82ea294cc14edd30bd1f092`  
		Last Modified: Mon, 22 Jun 2026 19:45:28 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260628.0.549485`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:cf028aee853281ba9b3cba41b49f7ad4836275256226938ab619e0f05b1e6105
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:9e9da3122b537ad94f22c8c6f89c1e3f253f3a1e22944364a061c75a041705da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303476484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a526da64be671b23ef83f536caa4cef2a32735775c66f2236da1faa549c44ed`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.version=20260621.0.546891
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.created=2026-06-21T00:09:09+00:00
# Mon, 22 Jun 2026 19:45:03 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 19:45:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260621.0.546891' /etc/os-release # buildkit
# Mon, 22 Jun 2026 19:45:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:45:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:62643db854ce653b16203b398b46ee50dab761672d23297d03123adb232575e2`  
		Last Modified: Mon, 22 Jun 2026 19:46:02 GMT  
		Size: 303.5 MB (303465083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af39dfe94e24e71fad2521b922aff4ed726e224913d162d050cbcf17dbc532f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:be48dd7af8c2581120437086d384ec198c4904e81dc99368d10d4b074495688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14391790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182f008c3d3c04bd2a451a101f2d03e12bf162658c49f995254cb653be318010`

```dockerfile
```

-	Layers:
	-	`sha256:7657b4e8bce2843760e0550f8b92cd02f33275daa81be6edfde2a0b2e7ebe3ec`  
		Last Modified: Mon, 22 Jun 2026 19:45:56 GMT  
		Size: 14.4 MB (14380078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e360c05349f29d112ac8780a6d69629726f81182c0927a0e5dec9cc0835a0f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260628.0.549485`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:d9abf957599bddf27955a0dd82b4457dcfaace50525bb773f6c7518f8015e7e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:cc54f12fae7c81bd0d1a38f1694b4c28ffc708b358dd5876ab77dde49d37925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131368828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435ed19930af3ee3bbecbface47941c8fd2a6e3985516ceeb61d2b3b3e78ab09`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.version=20260621.0.546891
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 22 Jun 2026 19:45:05 GMT
LABEL org.opencontainers.image.created=2026-06-21T00:09:09+00:00
# Mon, 22 Jun 2026 19:45:05 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 19:45:07 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260621.0.546891' /etc/os-release # buildkit
# Mon, 22 Jun 2026 19:45:07 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:45:07 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ab5bfa2e5807a3c5c29f3e1ca9c37088a006dd7a0b85eaf01292209d76ecc57b`  
		Last Modified: Mon, 22 Jun 2026 19:45:32 GMT  
		Size: 131.4 MB (131360138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b870649fd58e8b1d400a4293bb484d7f462a736493ce0ac56fd2faa68f38ca8`  
		Last Modified: Mon, 22 Jun 2026 19:45:29 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:5023748da22f12ddc65821a144a7105c4d8cfd3a3926f021c82f3a27430b9ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8188301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65147f82d924d8f4af76fbbcc29ba1bcdc2e038bcf1464488fd31d86cf37864`

```dockerfile
```

-	Layers:
	-	`sha256:001bafb1448cc60f0138f0068135b43fffb51a1bcdf6e408e28729ba3d3443ce`  
		Last Modified: Mon, 22 Jun 2026 19:45:29 GMT  
		Size: 8.2 MB (8176372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57e136ab266c57d7367c6134d5c3b6902eaf48ca82ea294cc14edd30bd1f092`  
		Last Modified: Mon, 22 Jun 2026 19:45:28 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:b3d3414c33e700ea0268cfd98f7b93ad15eae04820c18e15f4206951c33c17ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5018ebf50dc41326b5becee912df1861158257ebd8b085ed6e64d7a9080c1cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325876711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909e126b2bc9284d6e50fbde442f865cd15c9fd76527a6c666d14dc26829696`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.version=20260621.0.546891
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.created=2026-06-21T00:09:09+00:00
# Mon, 22 Jun 2026 19:45:39 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 19:45:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260621.0.546891' /etc/os-release # buildkit
# Mon, 22 Jun 2026 19:45:47 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:45:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:26a2f4e971794b5cd538bb8bfc45e2c869ff01f072afebb464bf1501e121888d`  
		Last Modified: Mon, 22 Jun 2026 19:46:47 GMT  
		Size: 325.9 MB (325864186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465090eae9f4efa8090ac4f85c7fdc8d05a57c4fd0817cc085ddadac7c829ff2`  
		Last Modified: Mon, 22 Jun 2026 19:46:41 GMT  
		Size: 12.5 KB (12525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4f9b35e2ef52d379cfb5628136579061b32e7d0f086929c01c75738cfb0b93b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14662862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056cb1773884c4aeb4c2e1fa3733484a39b2d218db54d8ac3a981d1456618435`

```dockerfile
```

-	Layers:
	-	`sha256:f2f07abf78a99d12b4b363543abc33c63cd23d15325c6ad1a2da1679dfe41cb9`  
		Last Modified: Mon, 22 Jun 2026 19:46:42 GMT  
		Size: 14.7 MB (14651094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4f474d86efa9ddf01100075fba24f3e4be97255c17266ed4dbc75c179a30c9`  
		Last Modified: Mon, 22 Jun 2026 19:46:41 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260628.0.549485`

**does not exist** (yet?)
