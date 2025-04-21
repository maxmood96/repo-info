<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250420.0.338771`](#archlinuxbase-202504200338771)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250420.0.338771`](#archlinuxbase-devel-202504200338771)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250420.0.338771`](#archlinuxmultilib-devel-202504200338771)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:3f2eefb6cbbdcb3a9677442d569c1f332706eb535da31275128508ca365af1b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a8323f89dfc10b4281ad3ce790de6541056fa03a348db0167b8759b64998f98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14be0997a90bec78c3c526042f8dc9474d073f718c0b3260afb7120a62c0adb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.version=20250413.0.335299
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.created=2025-04-13T00:07:50+00:00
# Sun, 13 Apr 2025 00:07:50 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250413.0.335299' /etc/os-release # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
ENV LANG=C.UTF-8
# Sun, 13 Apr 2025 00:07:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e480c905023911546029c27182f928580da4546c7dc85f842a974c9effe646ad`  
		Last Modified: Mon, 14 Apr 2025 18:00:53 GMT  
		Size: 160.2 MB (160218350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794c4182559636633d7d4f27839d8ea0d05f74dfdd184a988915008fcea6a10a`  
		Last Modified: Mon, 14 Apr 2025 18:00:50 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:2b7cefe5890586d1759be10fb001c913996872910b9bc30ee56af02da8bc1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b908d8d16d8c95b8a35eb435106613e5dfc865c6ca64a35470f3db5c3a06ec81`

```dockerfile
```

-	Layers:
	-	`sha256:383710fdac844c3ca7f15dc13ba8937b82d95427c153a1b1e6cc38fe3f6f9466`  
		Last Modified: Mon, 14 Apr 2025 18:00:51 GMT  
		Size: 8.2 MB (8164632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbed1ed9b4f213cd46a8ec3b943d348fd36a119420cf5cd035072449d4660bf`  
		Last Modified: Mon, 14 Apr 2025 18:00:50 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250420.0.338771`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:6c2b425acd8752cf50a78c33b360811cacbe71c4b596838f4aa8752469955269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6eb91015bcc283a912a302a7b22665d98461816a75c220b4944d840581c3adbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281765810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053cdbf777e997f66204ce3cc14db807b624970e99bc5e746c3213ef8c9c967a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.version=20250413.0.335299
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.created=2025-04-13T00:07:50+00:00
# Sun, 13 Apr 2025 00:07:50 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250413.0.335299' /etc/os-release # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
ENV LANG=C.UTF-8
# Sun, 13 Apr 2025 00:07:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c282d2893b767f376f8dcaccecd0f322acb7c7a95a74873bea131260cacf7493`  
		Last Modified: Mon, 14 Apr 2025 18:01:26 GMT  
		Size: 281.8 MB (281756646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6f3bdec2aaa51e14106d14b92ea2fc8750ec87497a1e8fa60fbbc9a9d78cef`  
		Last Modified: Mon, 14 Apr 2025 18:01:21 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:76202b7b85b92c5aef23bb4b68f4897b8aae95c70ce0841ecc0809e1e18b4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11996818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c397ebe69b37e683423f766bf710a1b309f1801de60ad61e658ffba47bac0dbe`

```dockerfile
```

-	Layers:
	-	`sha256:e4c55bc06c1cf576ec10b1d3484db55fda70fb102ebaeda37aaec6880cc97998`  
		Last Modified: Mon, 14 Apr 2025 18:01:22 GMT  
		Size: 12.0 MB (11985064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7fcc3706f198d4ff6ac55086d1eecbe551e7d17f20e4e841cda7b48950ad270`  
		Last Modified: Mon, 14 Apr 2025 18:01:21 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250420.0.338771`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:3f2eefb6cbbdcb3a9677442d569c1f332706eb535da31275128508ca365af1b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a8323f89dfc10b4281ad3ce790de6541056fa03a348db0167b8759b64998f98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14be0997a90bec78c3c526042f8dc9474d073f718c0b3260afb7120a62c0adb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.version=20250413.0.335299
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.created=2025-04-13T00:07:50+00:00
# Sun, 13 Apr 2025 00:07:50 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250413.0.335299' /etc/os-release # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
ENV LANG=C.UTF-8
# Sun, 13 Apr 2025 00:07:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e480c905023911546029c27182f928580da4546c7dc85f842a974c9effe646ad`  
		Last Modified: Mon, 14 Apr 2025 18:00:53 GMT  
		Size: 160.2 MB (160218350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794c4182559636633d7d4f27839d8ea0d05f74dfdd184a988915008fcea6a10a`  
		Last Modified: Mon, 14 Apr 2025 18:00:50 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:2b7cefe5890586d1759be10fb001c913996872910b9bc30ee56af02da8bc1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b908d8d16d8c95b8a35eb435106613e5dfc865c6ca64a35470f3db5c3a06ec81`

```dockerfile
```

-	Layers:
	-	`sha256:383710fdac844c3ca7f15dc13ba8937b82d95427c153a1b1e6cc38fe3f6f9466`  
		Last Modified: Mon, 14 Apr 2025 18:00:51 GMT  
		Size: 8.2 MB (8164632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbed1ed9b4f213cd46a8ec3b943d348fd36a119420cf5cd035072449d4660bf`  
		Last Modified: Mon, 14 Apr 2025 18:00:50 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:521ba353716efe7a8938ef4cebd8eec63b3112d0d42f927ef7a095de71361aab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5877e4f34b73dde77086bdb7b8c2cdc2ac909cac0ccc7234b3e1e42537f4d736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331766952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c7309fde5a9ee0b0b41a84bd8546da9b425608be3a69f9f9a73a135f1b7e4c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.version=20250413.0.335299
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.created=2025-04-13T00:07:50+00:00
# Sun, 13 Apr 2025 00:07:50 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250413.0.335299' /etc/os-release # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
ENV LANG=C.UTF-8
# Sun, 13 Apr 2025 00:07:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7c59532cd91bd88ed8d5a515903378df2df6ec04b43146fbf79d48c0b357d9b1`  
		Last Modified: Mon, 14 Apr 2025 18:01:34 GMT  
		Size: 331.8 MB (331756653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6691d2c981d2211a8e6a6d4a18c2793d3e28738e708a72d402f0963b3316d4`  
		Last Modified: Mon, 14 Apr 2025 18:01:28 GMT  
		Size: 10.3 KB (10299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3e5012423e5b160b9ec5833767d6c9ece50e09cc6207f141591ca63efe78fdb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12265410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a10eb9944685c52afdcc0e99b0a2279b283203bb3a481a66e1c787ab1e3b1e`

```dockerfile
```

-	Layers:
	-	`sha256:420d8c5d9735ac9dd061250c023cebcf3ee6d76290b91fe03bc92dbba04a9d03`  
		Last Modified: Mon, 14 Apr 2025 18:01:28 GMT  
		Size: 12.3 MB (12253599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b6808055b6a2ee364b1bc9cc1690b76de484fdba7c95dab14b1a67dbaf9db8`  
		Last Modified: Mon, 14 Apr 2025 18:01:28 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250420.0.338771`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
