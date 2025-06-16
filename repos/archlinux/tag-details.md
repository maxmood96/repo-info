<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250615.0.365905`](#archlinuxbase-202506150365905)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250615.0.365905`](#archlinuxbase-devel-202506150365905)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250615.0.365905`](#archlinuxmultilib-devel-202506150365905)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:d2094076ea97044f0a0d7e8ea7ce025cc4fb9409b3bd5c4749c21728c204d490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c2eeedb62514510cd3f84ebc23bd4324a106a4be383ec149212fdd65833b1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163064044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c19710e5c8d31343b187ed378711fc6aa989ffc9541b0687779376be2aef86e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.version=20250608.0.361578
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.created=2025-06-08T00:07:57+00:00
# Sun, 08 Jun 2025 00:07:57 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250608.0.361578' /etc/os-release # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
ENV LANG=C.UTF-8
# Sun, 08 Jun 2025 00:07:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6eb9a8a8f4c4496c84236c01bbfb11cbb608f66759fd0d841ed932687fa8da39`  
		Last Modified: Mon, 09 Jun 2025 22:48:27 GMT  
		Size: 163.1 MB (163055701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc962479e73fd2293dcef41742b92fb5d741911195f105d0bdbb0043d84c42d7`  
		Last Modified: Mon, 09 Jun 2025 19:09:36 GMT  
		Size: 8.3 KB (8343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:c20f9cff8b04a03d4905bfb2c82b05c557a24fea7e3ae56f6b265c083c364bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8157558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99caff0cb3fb8e6383ce12529dab1550037ac034d87faafe3af92d140ae936a1`

```dockerfile
```

-	Layers:
	-	`sha256:555123536b26a9aa64d87246d81145b737725609abc9eee3537611425b1209af`  
		Last Modified: Mon, 09 Jun 2025 22:48:17 GMT  
		Size: 8.1 MB (8145586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be52222307b16d2e84a3e7266fee9db2cc0eaaba844cdc3ce9800be2b43d5116`  
		Last Modified: Mon, 09 Jun 2025 22:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250615.0.365905`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:5b87f50b25ce0ea047a13cdcd0043b22f61f6b341e3264b49d8ec98eb4308d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d78e0b8556659db64a766f6e9aa982ca986cc9b8743300881246bee817eebf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287762151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc51fd8af02ccbe9cd40162f8ce07ec7ebcffd9477cfb3e21bd059a87e99556`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.version=20250608.0.361578
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.created=2025-06-08T00:07:57+00:00
# Sun, 08 Jun 2025 00:07:57 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250608.0.361578' /etc/os-release # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
ENV LANG=C.UTF-8
# Sun, 08 Jun 2025 00:07:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edaf86bcae51e42a88f99a1abbffc4007b15f9c39b3a85d74af977ca02a7db1f`  
		Last Modified: Mon, 09 Jun 2025 22:48:35 GMT  
		Size: 287.8 MB (287752988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4f01c4f25e43fce7667d7058c041b5836282f45efb05cafc8a23f74453ff03`  
		Last Modified: Mon, 09 Jun 2025 19:10:29 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:097185de7b7e16ca563118b2a1bf0b70667d127d993489dd034b00d53b8306e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12018152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3aaaaa0c653f320196018de497c7cb88d94c270af5032163b4ee6222a4089d`

```dockerfile
```

-	Layers:
	-	`sha256:a7fdab34f709e2fc5baeaae173e94d12e23fa490a9f4e8d9f198a35214b29ac5`  
		Last Modified: Mon, 09 Jun 2025 22:48:23 GMT  
		Size: 12.0 MB (12006399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e983e8d72cf1cb479b9a164d1cea8b70187ea71d2503d768cea6d3000faa2f`  
		Last Modified: Mon, 09 Jun 2025 22:48:24 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250615.0.365905`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:d2094076ea97044f0a0d7e8ea7ce025cc4fb9409b3bd5c4749c21728c204d490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c2eeedb62514510cd3f84ebc23bd4324a106a4be383ec149212fdd65833b1e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163064044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c19710e5c8d31343b187ed378711fc6aa989ffc9541b0687779376be2aef86e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.version=20250608.0.361578
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.created=2025-06-08T00:07:57+00:00
# Sun, 08 Jun 2025 00:07:57 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250608.0.361578' /etc/os-release # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
ENV LANG=C.UTF-8
# Sun, 08 Jun 2025 00:07:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6eb9a8a8f4c4496c84236c01bbfb11cbb608f66759fd0d841ed932687fa8da39`  
		Last Modified: Mon, 09 Jun 2025 22:48:27 GMT  
		Size: 163.1 MB (163055701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc962479e73fd2293dcef41742b92fb5d741911195f105d0bdbb0043d84c42d7`  
		Last Modified: Mon, 09 Jun 2025 19:09:36 GMT  
		Size: 8.3 KB (8343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:c20f9cff8b04a03d4905bfb2c82b05c557a24fea7e3ae56f6b265c083c364bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8157558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99caff0cb3fb8e6383ce12529dab1550037ac034d87faafe3af92d140ae936a1`

```dockerfile
```

-	Layers:
	-	`sha256:555123536b26a9aa64d87246d81145b737725609abc9eee3537611425b1209af`  
		Last Modified: Mon, 09 Jun 2025 22:48:17 GMT  
		Size: 8.1 MB (8145586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be52222307b16d2e84a3e7266fee9db2cc0eaaba844cdc3ce9800be2b43d5116`  
		Last Modified: Mon, 09 Jun 2025 22:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:37333001fa294ed7a7d24251bc2e9d4d1994179f41ab4824296917fb85655641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:da861e322fb59830d475c836f19ddce01ed49b57d62da3412e2a20656d7fc666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338915575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d2e3c9ae7759a8e95c98da2d5344e656f5e879971d06bad78a13b397316dd2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.version=20250608.0.361578
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.created=2025-06-08T00:07:57+00:00
# Sun, 08 Jun 2025 00:07:57 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250608.0.361578' /etc/os-release # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
ENV LANG=C.UTF-8
# Sun, 08 Jun 2025 00:07:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ea7e7f76419f161d7e505b4739c95118b6711ff02193c3191043e82dfd0d77e0`  
		Last Modified: Mon, 09 Jun 2025 20:22:02 GMT  
		Size: 338.9 MB (338905315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e566327128d535b57df6147958cb3dcbcd2dec2bb700ee641e2e51480bc443`  
		Last Modified: Mon, 09 Jun 2025 19:10:31 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:280f5d01ba094e5fb935ebd3f18b9b3ab68eb690e85d57d8c552a01e73ec36cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12287098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d7e266299c5d2e4628d8102c1064f632b5d7340d0624101b1929b9a84b70db`

```dockerfile
```

-	Layers:
	-	`sha256:3e53a7edde5327ab20078444499959f668c15587710b781d8183c90ee1533694`  
		Last Modified: Mon, 09 Jun 2025 22:48:27 GMT  
		Size: 12.3 MB (12275288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2308e8a46ecddf3a4044d82523454512cf8b9395f23ee4604d637fa51d3ab9`  
		Last Modified: Mon, 09 Jun 2025 22:48:27 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250615.0.365905`

**does not exist** (yet?)
