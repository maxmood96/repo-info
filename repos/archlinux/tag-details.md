<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250413.0.335299`](#archlinuxbase-202504130335299)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250413.0.335299`](#archlinuxbase-devel-202504130335299)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250413.0.335299`](#archlinuxmultilib-devel-202504130335299)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:95e914e8b16eb07c8660c4352c1530a52dcf829038f1f65233543fee28a78d6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:2bc4e27fb84da173ba06756de32def4daa6450d36817e2cb8f39ff498d42186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160022478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f933370266099185a60baadf9d7af78d42b832d85988cc38ce640567795ada`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250406.0.331908
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-04-06T00:07:28+00:00
# Sun, 06 Apr 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250406.0.331908' /etc/os-release # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 06 Apr 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5d0dd26df6b775844a45d3d2b4ab2164f22c5a0888f1445e2c34f23e6135fad8`  
		Last Modified: Mon, 07 Apr 2025 18:03:41 GMT  
		Size: 160.0 MB (160014123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407b29e0f093892f642e2c89f45844893b21cf4c0154a5c693eac0fdb96aa969`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 8.4 KB (8355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9017f22a54b74878f9b33d53d9cc571fe6bb5c9337f33939d4e7868ac805cbbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee256ca5e285ed7cf2e424a47011a1152f7068560949aae0c164042915750f8e`

```dockerfile
```

-	Layers:
	-	`sha256:2454f49832f802d70ca4a6ffba68d9c8606613d2260b7f57782720f7f9004a76`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 8.2 MB (8162146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d86d4aa84108478c1065e2746660d1f38fa76c5196875ee8591ce5d099ad5336`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250413.0.335299`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:3d31f40bcc1906a600cfd60ca402704f6c8255ff7ea6d7924e007c531fc0a967
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7e0a3a332be4c9cacfb32ab4048efd0f0886851862965aa034247be9ae456279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281546207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84fea2e6f3fb8948b31851ce4272f436d3b934f76a5616b680bcfcb3748870a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250406.0.331908
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-04-06T00:07:28+00:00
# Sun, 06 Apr 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250406.0.331908' /etc/os-release # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 06 Apr 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:34b1058b6f6cc11aa7a452f023b91e3f5a3b87ece19c6f6ccfbf890893b3657f`  
		Last Modified: Mon, 07 Apr 2025 18:03:53 GMT  
		Size: 281.5 MB (281537033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b2ffd56f55b5b4806373f362e9b24bb7ed6de316e33f9ddf0c6431d659bb9`  
		Last Modified: Mon, 07 Apr 2025 18:03:48 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3ed84327f4596f0a78d18256f930f21e60c395495c41e02549c519646ee9e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11994332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27cb2805a16c90414b17683929835c9d0517523ca4c9cb230b16ecf008b2b2d`

```dockerfile
```

-	Layers:
	-	`sha256:3bda438186c9981ccd73624fcad54d60dff7b440fa512f9e645671b2c11b9d8e`  
		Last Modified: Mon, 07 Apr 2025 18:03:48 GMT  
		Size: 12.0 MB (11982578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7c1e887b4dbdac0a0583cf264d9da2b81341d4fb9de1338808e052477dfeca`  
		Last Modified: Mon, 07 Apr 2025 18:03:48 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250413.0.335299`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:95e914e8b16eb07c8660c4352c1530a52dcf829038f1f65233543fee28a78d6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2bc4e27fb84da173ba06756de32def4daa6450d36817e2cb8f39ff498d42186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160022478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f933370266099185a60baadf9d7af78d42b832d85988cc38ce640567795ada`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250406.0.331908
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-04-06T00:07:28+00:00
# Sun, 06 Apr 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250406.0.331908' /etc/os-release # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 06 Apr 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5d0dd26df6b775844a45d3d2b4ab2164f22c5a0888f1445e2c34f23e6135fad8`  
		Last Modified: Mon, 07 Apr 2025 18:03:41 GMT  
		Size: 160.0 MB (160014123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407b29e0f093892f642e2c89f45844893b21cf4c0154a5c693eac0fdb96aa969`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 8.4 KB (8355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:9017f22a54b74878f9b33d53d9cc571fe6bb5c9337f33939d4e7868ac805cbbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee256ca5e285ed7cf2e424a47011a1152f7068560949aae0c164042915750f8e`

```dockerfile
```

-	Layers:
	-	`sha256:2454f49832f802d70ca4a6ffba68d9c8606613d2260b7f57782720f7f9004a76`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 8.2 MB (8162146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d86d4aa84108478c1065e2746660d1f38fa76c5196875ee8591ce5d099ad5336`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:b625f5d64812272a2969596a861d0fc2f9c88a391b9f7de7ca29a33cdbf4ec57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4f2d98923a12665dd8520030d87bc54a15bd177437a78d20f673aba40ab3fd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331542097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54118882a98d870564b8c805d01b3a4dba5a0a1d98fb671cfb926a1c771ae34`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250406.0.331908
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-04-06T00:07:28+00:00
# Sun, 06 Apr 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250406.0.331908' /etc/os-release # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 06 Apr 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2b1771da912aba432c25dc8e466887ca1f92e7e753002ba2052e82815b5fca8f`  
		Last Modified: Mon, 07 Apr 2025 18:09:03 GMT  
		Size: 331.5 MB (331531784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056af4e3a52ede0d2a6b35a9a32d5396a3e311ab645a4b5938247a7729841ac9`  
		Last Modified: Mon, 07 Apr 2025 18:08:53 GMT  
		Size: 10.3 KB (10313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd907aa0b6a448746dcd77343f6765718774c79232906c1518efc840d3a692e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12262924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb700d418fafc1057559825d021cdf42bcae165187de01dda63716e2a919a6c`

```dockerfile
```

-	Layers:
	-	`sha256:e995abc01400339b580f5eebaeb8f6e7cc5bf5d0afb64ef92b03a95cd15ea500`  
		Last Modified: Mon, 07 Apr 2025 18:08:53 GMT  
		Size: 12.3 MB (12251113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fb6373dfaee771421b1ae9f86e3bff2b882fa4f41ea15ffbda2359b6838aa9`  
		Last Modified: Mon, 07 Apr 2025 18:08:53 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250413.0.335299`

**does not exist** (yet?)
