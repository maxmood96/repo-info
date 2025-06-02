<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250601.0.358000`](#archlinuxbase-202506010358000)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250601.0.358000`](#archlinuxbase-devel-202506010358000)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250601.0.358000`](#archlinuxmultilib-devel-202506010358000)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:5519bb4afc78843352ea5afb3ea022c76c93b22f6c762c87cdc2b6885860965b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:882de919fa2a7313b327800f64251f11dd803da0ee4ef55a759ee40c06f4ce41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162389075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22c3b9e7ce1d4d1e228fecf74b6090f173c9bcad19bff9e41a47eb7868e8a2c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.version=20250525.0.354646
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.created=2025-05-25T00:07:54+00:00
# Sun, 25 May 2025 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 May 2025 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250525.0.354646' /etc/os-release # buildkit
# Sun, 25 May 2025 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 25 May 2025 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0d274ac583c892ca0d5ee71cadf19a4cafca53dec75afed39bb6bf218cee20f8`  
		Last Modified: Tue, 27 May 2025 18:51:21 GMT  
		Size: 162.4 MB (162380696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c749a56ae37e94ae94a5d071d60bdf0e537d1a02423cd7df1132e9c02a1dbd4`  
		Last Modified: Tue, 27 May 2025 18:51:18 GMT  
		Size: 8.4 KB (8379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:6923b44e9de715de26a743a9f2d5f72ea12a8179c197dede93b5f1ebb76cb804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8180777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e57c3d57733c75520339a3b2d87760afc4d04da87c7bba0a7680c06dc69693`

```dockerfile
```

-	Layers:
	-	`sha256:b993f8f92a17f7a9f9719f6ae415651fd7bee7c9dc66af8bec7d01e1637858da`  
		Last Modified: Tue, 27 May 2025 18:51:19 GMT  
		Size: 8.2 MB (8168805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53133b9118535718588c2705dd0a0e530730019fc77cd55bdc5bd084e303859`  
		Last Modified: Tue, 27 May 2025 18:51:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250601.0.358000`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:cc583ad12f43f59a25c9833b638b5656ab5941fefb92404f95e8c15ca162b62b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:80db78991e3b8cbc06978080b9aecacf44b45ae8dcf9df665d6b5822ad615a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287058217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8936d8d04f80e46c73351fd816703abd057ef4a6cdb3d397015356f42f79791c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.version=20250525.0.354646
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.created=2025-05-25T00:07:54+00:00
# Sun, 25 May 2025 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 May 2025 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250525.0.354646' /etc/os-release # buildkit
# Sun, 25 May 2025 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 25 May 2025 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c184cf66b9fc050ddf0631ef482f6eed24164bd8b38afc0e99cd7eec8f405ebc`  
		Last Modified: Tue, 27 May 2025 18:51:44 GMT  
		Size: 287.0 MB (287049022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a85f83999853f4bf40957a392bfe9255c9d7f7965de183da977cf3dff8a9ad`  
		Last Modified: Tue, 27 May 2025 18:51:40 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:977d8218552496dfe26fa64f871cac5418f5b1e5ba7eb785426320d68c492913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12041372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4042b5cb0aac9e8ba643a1fc1a0b8cce4c538743f3d0a3c31015909fe68d1f93`

```dockerfile
```

-	Layers:
	-	`sha256:f7bc271bfb97491614ad4a39b17aac91c8e9057d7c662ba1e539ded9cd134cb4`  
		Last Modified: Tue, 27 May 2025 18:51:40 GMT  
		Size: 12.0 MB (12029618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3ad2a9fa377d8a76c100a382e45575753f7ccc2faa032018cbeab06304b27e`  
		Last Modified: Tue, 27 May 2025 18:51:40 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250601.0.358000`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:5519bb4afc78843352ea5afb3ea022c76c93b22f6c762c87cdc2b6885860965b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:882de919fa2a7313b327800f64251f11dd803da0ee4ef55a759ee40c06f4ce41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162389075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22c3b9e7ce1d4d1e228fecf74b6090f173c9bcad19bff9e41a47eb7868e8a2c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.version=20250525.0.354646
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.created=2025-05-25T00:07:54+00:00
# Sun, 25 May 2025 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 May 2025 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250525.0.354646' /etc/os-release # buildkit
# Sun, 25 May 2025 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 25 May 2025 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0d274ac583c892ca0d5ee71cadf19a4cafca53dec75afed39bb6bf218cee20f8`  
		Last Modified: Tue, 27 May 2025 18:51:21 GMT  
		Size: 162.4 MB (162380696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c749a56ae37e94ae94a5d071d60bdf0e537d1a02423cd7df1132e9c02a1dbd4`  
		Last Modified: Tue, 27 May 2025 18:51:18 GMT  
		Size: 8.4 KB (8379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:6923b44e9de715de26a743a9f2d5f72ea12a8179c197dede93b5f1ebb76cb804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8180777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e57c3d57733c75520339a3b2d87760afc4d04da87c7bba0a7680c06dc69693`

```dockerfile
```

-	Layers:
	-	`sha256:b993f8f92a17f7a9f9719f6ae415651fd7bee7c9dc66af8bec7d01e1637858da`  
		Last Modified: Tue, 27 May 2025 18:51:19 GMT  
		Size: 8.2 MB (8168805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53133b9118535718588c2705dd0a0e530730019fc77cd55bdc5bd084e303859`  
		Last Modified: Tue, 27 May 2025 18:51:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:68302e0528cde22744d1a740ef41bf39b53499760afe63b70bcc5476e104b305
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c610420447bbbc5123790a6d276b3f5a375334bca7b7bf2ab3fdaa6bea459fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338202536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2873f8627434d281f5aaedd55a7d4db9f6018a9bd58f5d34136ab52a215228`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.version=20250525.0.354646
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.created=2025-05-25T00:07:54+00:00
# Sun, 25 May 2025 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 May 2025 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250525.0.354646' /etc/os-release # buildkit
# Sun, 25 May 2025 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 25 May 2025 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:078d9a48ab98980e9814165084b9aa06cc353b71dc529f18e74b34151ebfb280`  
		Last Modified: Tue, 27 May 2025 18:52:12 GMT  
		Size: 338.2 MB (338192260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5ab2201e23756fed572b08087aba5ebefbe2f9f0dfa8454b5fb7e35cf95f1d`  
		Last Modified: Tue, 27 May 2025 18:52:03 GMT  
		Size: 10.3 KB (10276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:807766c09a13af3b22e93cdee9eba25197ec30a094d353529eb45f2ad9465874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9737f64c584866a464e033db3f7d93a71d45bfe9c5a139d84a1ffe486673d6`

```dockerfile
```

-	Layers:
	-	`sha256:1d95f4771e90617bc7424144d65e65ec7df971fc4da8eeca002302da837ac1df`  
		Last Modified: Tue, 27 May 2025 18:52:04 GMT  
		Size: 12.3 MB (12298507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:879b785c42df989918859ef0986c7aa55a06cdb731041c4d14c40c1bf65bde6d`  
		Last Modified: Tue, 27 May 2025 18:52:03 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250601.0.358000`

**does not exist** (yet?)
