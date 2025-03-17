<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250316.0.322463`](#archlinuxbase-202503160322463)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250316.0.322463`](#archlinuxbase-devel-202503160322463)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250316.0.322463`](#archlinuxmultilib-devel-202503160322463)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:ae7491066c2f96861d7b442aef512974138c2004b8bf5b2aacda6b8fd9e112fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:068aa6bfc1e735cdf9be3dbf66327011f99126656f479168f479d68b28181106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159152424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d4665b7362f3c2d04392ddec5964b72d305e3640a5e99430f3a4be00c2d6f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250302.0.316047
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-03-02T00:07:35+00:00
# Sun, 02 Mar 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250302.0.316047' /etc/os-release # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 02 Mar 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:51e5f99a23d6af0dc9c3bb45943e9950d7aa3a815eaedd81e944b1f0999c88e1`  
		Last Modified: Mon, 03 Mar 2025 19:12:43 GMT  
		Size: 159.1 MB (159144057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb7f519a524771019f49e25f7c55ea730a29becb5d3e6e1d72af226714dc5d9`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:a3990677d69dabc03809ed735990bcaf7d6af24e1f51193a9102ee09da08f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cf10d6ccdeb296a6be5048270c7cc3902e7a0af18c72669b90b697cf8890af`

```dockerfile
```

-	Layers:
	-	`sha256:a8f854c114c75d52c5dce84540c6aab80a1d12432f599145aeca4c709a7eedd9`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 8.2 MB (8155499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4ae77eb4717a10f5b21a1ef6933ea61dd0a091558d99a23a67258833568dc7`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250316.0.322463`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:61b9b05cf6a7a42aa1a32f0b00c92dcfc0b6acf3af2db1b86ab29f6605b21401
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:188ef5ce95b5a784984d9758c0cda67c284798500336ed4eed2bb15efe469389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280617641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad077ca48e15980d045d8adec7190650b679f318eaad53eec87704605c4a2b6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250302.0.316047
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-03-02T00:07:35+00:00
# Sun, 02 Mar 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250302.0.316047' /etc/os-release # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 02 Mar 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:21f5dcdde9037bc145a8f09b4dbc4c0ecf8cd531d80b207c214406f49fbd1be6`  
		Last Modified: Mon, 03 Mar 2025 19:13:19 GMT  
		Size: 280.6 MB (280608555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc006fc98655a856225002ded016e566c954840bbf607934b6f1947803dc1a15`  
		Last Modified: Mon, 03 Mar 2025 19:13:15 GMT  
		Size: 9.1 KB (9086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5d373902da7ba241e66d8ac6d3fc438584200531e842029ab3ee9808413a4ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11987649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e394d34ade0f93edb1efcb623348d73c688850a5cc6775ea96e0d4315a6874df`

```dockerfile
```

-	Layers:
	-	`sha256:54906d633b93a81f3961468d3d4be89ee28f899b3aca44c479c3a438176aaec5`  
		Last Modified: Mon, 03 Mar 2025 19:13:15 GMT  
		Size: 12.0 MB (11975895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8745b03003325ea5e1ea0e2aa309a67f25a7fadb09ee2f2623ef1187b89019b8`  
		Last Modified: Mon, 03 Mar 2025 19:13:15 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250316.0.322463`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ae7491066c2f96861d7b442aef512974138c2004b8bf5b2aacda6b8fd9e112fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:068aa6bfc1e735cdf9be3dbf66327011f99126656f479168f479d68b28181106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159152424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d4665b7362f3c2d04392ddec5964b72d305e3640a5e99430f3a4be00c2d6f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250302.0.316047
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-03-02T00:07:35+00:00
# Sun, 02 Mar 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250302.0.316047' /etc/os-release # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 02 Mar 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:51e5f99a23d6af0dc9c3bb45943e9950d7aa3a815eaedd81e944b1f0999c88e1`  
		Last Modified: Mon, 03 Mar 2025 19:12:43 GMT  
		Size: 159.1 MB (159144057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb7f519a524771019f49e25f7c55ea730a29becb5d3e6e1d72af226714dc5d9`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:a3990677d69dabc03809ed735990bcaf7d6af24e1f51193a9102ee09da08f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cf10d6ccdeb296a6be5048270c7cc3902e7a0af18c72669b90b697cf8890af`

```dockerfile
```

-	Layers:
	-	`sha256:a8f854c114c75d52c5dce84540c6aab80a1d12432f599145aeca4c709a7eedd9`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 8.2 MB (8155499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4ae77eb4717a10f5b21a1ef6933ea61dd0a091558d99a23a67258833568dc7`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:74c759e625389806b3553d7c5a0d95d26618428883ebeab775a68b6f40ad35ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b47bcac2a43bf0857b4397fad9be6cc18be1a8f35f11a27b39506d9932decd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330623643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58e84aa3cf0a9087fff5fdd8656f92fd208b9de89c0c62334aa7f85c0b5f637`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250302.0.316047
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-03-02T00:07:35+00:00
# Sun, 02 Mar 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250302.0.316047' /etc/os-release # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 02 Mar 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8523c5c460860703ca90183e37ae7db9d135d3191690aca4536d4a832ada5be1`  
		Last Modified: Mon, 03 Mar 2025 19:13:17 GMT  
		Size: 330.6 MB (330613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0241c1f953725c2e9dd779092b62b12f27247841a3dbe3d331f2c14126ebb331`  
		Last Modified: Mon, 03 Mar 2025 19:13:12 GMT  
		Size: 10.3 KB (10255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4355bbb255fa34a842705eb9748b6739f11fbb74d2d0c949621b0106f9a92660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12256221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f444cdf961017b6bb633f1ec1a7653068999ec44f747258ec89233180d77b6ce`

```dockerfile
```

-	Layers:
	-	`sha256:f93007251547515c009447d22715c8552dd88c48bb53bbf23c95d974cabb744d`  
		Last Modified: Mon, 03 Mar 2025 19:13:12 GMT  
		Size: 12.2 MB (12244410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59e51e77aa926b1683d6d5746611689fef2415f1bb3d1cd8c3fe268a776e257`  
		Last Modified: Mon, 03 Mar 2025 19:13:12 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250316.0.322463`

**does not exist** (yet?)
