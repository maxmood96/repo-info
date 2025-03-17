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
$ docker pull archlinux@sha256:42a33e798a4962982756560a6bd4b630e5394bca4d82ba199df0fc45ad3af7bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0bcb48829c8419196a0e426710c0cce34b5a3d980884d879809aae3120d169c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159211558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a49736c0aab9f79496a44c9b436ddb9b9b4714e16daf298c4497dee340fb7f9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ffc1d56182e7518eb7a75cb1a01ef2681d8002a8055b34dd5b4f4ae66a123b82`  
		Last Modified: Mon, 17 Mar 2025 17:50:10 GMT  
		Size: 159.2 MB (159203223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38beca783d0980c57587c0c5c1fdb07460ef01ef4d360869a605f3951d88369c`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:e448b27734677034f8a29b189c9aa7d34e3ead9dd78349cd4dd9a86df76cb775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a090ade9cbbbf15d3b2a62ccb6a76b35ada2018ac07fce46485d70d8fa3af3`

```dockerfile
```

-	Layers:
	-	`sha256:42b8262092613dfed596b7845c3afc30aaa6c350b5c3ee02759aa1fdfbdd8747`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.2 MB (8155521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027d2e3ce2b938c982d8c106b2bd67f50aa09713581dc5f51a2851c5fae53a80`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250316.0.322463`

```console
$ docker pull archlinux@sha256:42a33e798a4962982756560a6bd4b630e5394bca4d82ba199df0fc45ad3af7bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250316.0.322463` - linux; amd64

```console
$ docker pull archlinux@sha256:0bcb48829c8419196a0e426710c0cce34b5a3d980884d879809aae3120d169c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159211558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a49736c0aab9f79496a44c9b436ddb9b9b4714e16daf298c4497dee340fb7f9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ffc1d56182e7518eb7a75cb1a01ef2681d8002a8055b34dd5b4f4ae66a123b82`  
		Last Modified: Mon, 17 Mar 2025 17:50:10 GMT  
		Size: 159.2 MB (159203223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38beca783d0980c57587c0c5c1fdb07460ef01ef4d360869a605f3951d88369c`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250316.0.322463` - unknown; unknown

```console
$ docker pull archlinux@sha256:e448b27734677034f8a29b189c9aa7d34e3ead9dd78349cd4dd9a86df76cb775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a090ade9cbbbf15d3b2a62ccb6a76b35ada2018ac07fce46485d70d8fa3af3`

```dockerfile
```

-	Layers:
	-	`sha256:42b8262092613dfed596b7845c3afc30aaa6c350b5c3ee02759aa1fdfbdd8747`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.2 MB (8155521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027d2e3ce2b938c982d8c106b2bd67f50aa09713581dc5f51a2851c5fae53a80`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:8e9a67199c0e19b948e1fb2689e776badb2c809e60e245ec99f0c9fead3cdb89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b2b8809c3dd1a2615c0118e6fe14960e0f9e023bd93b2c4f27169d7fece6b134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280688675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a18fa20214e02eace3b3f6e7fab707d5e08a5975ee115c23eb441d0236d3db5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6ea895d481edad2d574c0da7ae67ab023c372f3339d132fbe9df2ed192e9af8c`  
		Last Modified: Mon, 17 Mar 2025 17:50:50 GMT  
		Size: 280.7 MB (280679605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e194902f33b02486da39c81de7fbff4e31abf37d09058562602565ec19de9e0b`  
		Last Modified: Mon, 17 Mar 2025 17:50:43 GMT  
		Size: 9.1 KB (9070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:28684ba8b71805f55134c30a43c7fd83dcbf78d57f68329d1138907e435d0ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11987671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652c325c88ad42fe1d579457298a9eaae37a062cb41a9135d8d4a9d2ce6622d8`

```dockerfile
```

-	Layers:
	-	`sha256:5b563dde661c80c1ba775a97b79912c37f36b0a916310b0313bcac0d51f5f793`  
		Last Modified: Mon, 17 Mar 2025 17:50:44 GMT  
		Size: 12.0 MB (11975917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1611911bbfe2fcd98c219696c4bf43e693d63ebf63476918626714f6535c797`  
		Last Modified: Mon, 17 Mar 2025 17:50:43 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250316.0.322463`

```console
$ docker pull archlinux@sha256:8e9a67199c0e19b948e1fb2689e776badb2c809e60e245ec99f0c9fead3cdb89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250316.0.322463` - linux; amd64

```console
$ docker pull archlinux@sha256:b2b8809c3dd1a2615c0118e6fe14960e0f9e023bd93b2c4f27169d7fece6b134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280688675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a18fa20214e02eace3b3f6e7fab707d5e08a5975ee115c23eb441d0236d3db5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6ea895d481edad2d574c0da7ae67ab023c372f3339d132fbe9df2ed192e9af8c`  
		Last Modified: Mon, 17 Mar 2025 17:50:50 GMT  
		Size: 280.7 MB (280679605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e194902f33b02486da39c81de7fbff4e31abf37d09058562602565ec19de9e0b`  
		Last Modified: Mon, 17 Mar 2025 17:50:43 GMT  
		Size: 9.1 KB (9070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250316.0.322463` - unknown; unknown

```console
$ docker pull archlinux@sha256:28684ba8b71805f55134c30a43c7fd83dcbf78d57f68329d1138907e435d0ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11987671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652c325c88ad42fe1d579457298a9eaae37a062cb41a9135d8d4a9d2ce6622d8`

```dockerfile
```

-	Layers:
	-	`sha256:5b563dde661c80c1ba775a97b79912c37f36b0a916310b0313bcac0d51f5f793`  
		Last Modified: Mon, 17 Mar 2025 17:50:44 GMT  
		Size: 12.0 MB (11975917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1611911bbfe2fcd98c219696c4bf43e693d63ebf63476918626714f6535c797`  
		Last Modified: Mon, 17 Mar 2025 17:50:43 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:42a33e798a4962982756560a6bd4b630e5394bca4d82ba199df0fc45ad3af7bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0bcb48829c8419196a0e426710c0cce34b5a3d980884d879809aae3120d169c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159211558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a49736c0aab9f79496a44c9b436ddb9b9b4714e16daf298c4497dee340fb7f9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ffc1d56182e7518eb7a75cb1a01ef2681d8002a8055b34dd5b4f4ae66a123b82`  
		Last Modified: Mon, 17 Mar 2025 17:50:10 GMT  
		Size: 159.2 MB (159203223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38beca783d0980c57587c0c5c1fdb07460ef01ef4d360869a605f3951d88369c`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:e448b27734677034f8a29b189c9aa7d34e3ead9dd78349cd4dd9a86df76cb775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a090ade9cbbbf15d3b2a62ccb6a76b35ada2018ac07fce46485d70d8fa3af3`

```dockerfile
```

-	Layers:
	-	`sha256:42b8262092613dfed596b7845c3afc30aaa6c350b5c3ee02759aa1fdfbdd8747`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 8.2 MB (8155521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027d2e3ce2b938c982d8c106b2bd67f50aa09713581dc5f51a2851c5fae53a80`  
		Last Modified: Mon, 17 Mar 2025 17:50:08 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:06e35cfb67ecad7144e7eed47f0da72c1a13e8a79fc4046c4b36c8a7bd3f6870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:9f3207a2265872f633478d58172d5795ad09d993b68360b472084b88067d0d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330699684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b450e5273289f2bd202e2485e6f90ddfe79b44bcc8c80bf27f1273ec961abf13`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a1901b4f066c719dceb6c165206acab439c74d74d988ec790c5f7a451744703c`  
		Last Modified: Mon, 17 Mar 2025 17:50:46 GMT  
		Size: 330.7 MB (330689448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb9c4d85f3a66cad602fc0d5fd2f688b737b7a8aa491129d8a1cbe4c1ef88e`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2ad9fafdb7e0bf20f3b4f60901b7bb54746ed84c6ccb0a69178569e75ed75aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12256242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408ad6539d1eee021b1a5bd7832c4b0ec8609f68c12323e38b01514adde08eeb`

```dockerfile
```

-	Layers:
	-	`sha256:bcf04837141ed06b7ff89c56dd4b2d8f642010514665d8dcd7b8ace4ee5fabc5`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 12.2 MB (12244432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e783cba17439c127bdea0ac2ef1de2870f3333afd29f4c66ff3e6c05588a4e8f`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250316.0.322463`

```console
$ docker pull archlinux@sha256:06e35cfb67ecad7144e7eed47f0da72c1a13e8a79fc4046c4b36c8a7bd3f6870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250316.0.322463` - linux; amd64

```console
$ docker pull archlinux@sha256:9f3207a2265872f633478d58172d5795ad09d993b68360b472084b88067d0d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330699684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b450e5273289f2bd202e2485e6f90ddfe79b44bcc8c80bf27f1273ec961abf13`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a1901b4f066c719dceb6c165206acab439c74d74d988ec790c5f7a451744703c`  
		Last Modified: Mon, 17 Mar 2025 17:50:46 GMT  
		Size: 330.7 MB (330689448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb9c4d85f3a66cad602fc0d5fd2f688b737b7a8aa491129d8a1cbe4c1ef88e`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250316.0.322463` - unknown; unknown

```console
$ docker pull archlinux@sha256:2ad9fafdb7e0bf20f3b4f60901b7bb54746ed84c6ccb0a69178569e75ed75aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12256242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408ad6539d1eee021b1a5bd7832c4b0ec8609f68c12323e38b01514adde08eeb`

```dockerfile
```

-	Layers:
	-	`sha256:bcf04837141ed06b7ff89c56dd4b2d8f642010514665d8dcd7b8ace4ee5fabc5`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 12.2 MB (12244432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e783cba17439c127bdea0ac2ef1de2870f3333afd29f4c66ff3e6c05588a4e8f`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
