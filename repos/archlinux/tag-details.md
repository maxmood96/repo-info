<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250608.0.361578`](#archlinuxbase-202506080361578)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250608.0.361578`](#archlinuxbase-devel-202506080361578)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250608.0.361578`](#archlinuxmultilib-devel-202506080361578)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:d3e52901b28d7a9bdd1fa47ec2a14e3ad5008c18cd1fb4d6961ce8ad90a7ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:68948306c655c44da90ed8be0a33dab973e85dd9b30aa4e64b0086dd04b8f459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162462964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694ad64eaa86aedf76a1d460a77c880dea64e1cbfe97a7455ae6ddcb9db2be0b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250601.0.358000
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-06-01T00:08:08+00:00
# Sun, 01 Jun 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250601.0.358000' /etc/os-release # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 01 Jun 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a168de9ee172b75bcbeb8854e1b7c4507a03e0e43dc1646e44747f140b6c43d8`  
		Last Modified: Tue, 03 Jun 2025 13:31:05 GMT  
		Size: 162.5 MB (162454599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d78b97bc7ccb3f6b298f4f8a698a542a301d20d448ded16ae82a729abbd2cde`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:c6c68f5ca517259ce14eea5c6a25daacdcfd1a220ad62e1d8df1d08dc79535aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8181302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea736c9edb49a2afade82f036fd810d0f2cfc5ca78a26a3811080599c58f6e7b`

```dockerfile
```

-	Layers:
	-	`sha256:5e111c2ae1864798eda0aebc09a41a024e886a7e2fbc1a51075f440a216238bc`  
		Last Modified: Tue, 03 Jun 2025 19:11:19 GMT  
		Size: 8.2 MB (8169330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d72f48a5a2b826078818b72d7cb63b57bc2de8785a5d70c5589486f04c678`  
		Last Modified: Tue, 03 Jun 2025 19:11:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250608.0.361578`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:3f7f6e4ddc04d4f6a8cb36b4af9e2290371f36dde1650c5177b50b7233706a35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6e2243eb90d12e09cbddf7d5297ac44195928282881562e6c9d339b44c029fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287135856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2d27cb2ad3b2f7d3491dd4607dd0472e8da9c34bf2fc74a5877bb7ef49bd20`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250601.0.358000
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-06-01T00:08:08+00:00
# Sun, 01 Jun 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250601.0.358000' /etc/os-release # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 01 Jun 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9eba33a123ffc0a67ad7c9fc71d74e5256149041186372c705e8ad4ca87f9ef2`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 287.1 MB (287126647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a033bf9719d0e801b428a756787b040ecc18dd0d1c1cfdda275e839bf1a2cd7`  
		Last Modified: Tue, 03 Jun 2025 13:32:29 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:58eb529e583d6583df0e8260bda56b2d8ad28c39f3463049fad7a566793cac67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12041897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b2fdf1a33d27824c978e00195d6382520bf710a70dc59c30e0f138bec9058d`

```dockerfile
```

-	Layers:
	-	`sha256:a653be72637f899fa9eedc6023ed722fe12ae3a14e14346ad22918102ece5738`  
		Last Modified: Wed, 04 Jun 2025 04:59:06 GMT  
		Size: 12.0 MB (12030143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1edbe1f07b5d13c5b76883241fc3c8eef54b37fb5c272566e8614ae3fca9850`  
		Last Modified: Wed, 04 Jun 2025 04:59:08 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250608.0.361578`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:d3e52901b28d7a9bdd1fa47ec2a14e3ad5008c18cd1fb4d6961ce8ad90a7ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:68948306c655c44da90ed8be0a33dab973e85dd9b30aa4e64b0086dd04b8f459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162462964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694ad64eaa86aedf76a1d460a77c880dea64e1cbfe97a7455ae6ddcb9db2be0b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250601.0.358000
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-06-01T00:08:08+00:00
# Sun, 01 Jun 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250601.0.358000' /etc/os-release # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 01 Jun 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a168de9ee172b75bcbeb8854e1b7c4507a03e0e43dc1646e44747f140b6c43d8`  
		Last Modified: Tue, 03 Jun 2025 13:31:05 GMT  
		Size: 162.5 MB (162454599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d78b97bc7ccb3f6b298f4f8a698a542a301d20d448ded16ae82a729abbd2cde`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:c6c68f5ca517259ce14eea5c6a25daacdcfd1a220ad62e1d8df1d08dc79535aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8181302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea736c9edb49a2afade82f036fd810d0f2cfc5ca78a26a3811080599c58f6e7b`

```dockerfile
```

-	Layers:
	-	`sha256:5e111c2ae1864798eda0aebc09a41a024e886a7e2fbc1a51075f440a216238bc`  
		Last Modified: Tue, 03 Jun 2025 19:11:19 GMT  
		Size: 8.2 MB (8169330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d72f48a5a2b826078818b72d7cb63b57bc2de8785a5d70c5589486f04c678`  
		Last Modified: Tue, 03 Jun 2025 19:11:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:3cc1f84a3d30af91a961939003511e14f055a79b51995268a56c61c5821287ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0c5dc362cc9f9f5038a1af45508f5c617ef9c501f9d0ff49529dbe11ab3c3a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338277512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0acf492e5b791dd24f739431f626d44643590aad0defa786e144748617a7914`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250601.0.358000
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-06-01T00:08:08+00:00
# Sun, 01 Jun 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250601.0.358000' /etc/os-release # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 01 Jun 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:12fc202400169e3d4e72f4fcd423ace9fbf29163322ea51c21ec76f9acf93b60`  
		Last Modified: Tue, 03 Jun 2025 13:58:50 GMT  
		Size: 338.3 MB (338267185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043f027ba9731cbcf066d48c033293a39d0250988ac4814e3098923b3ddddfa5`  
		Last Modified: Tue, 03 Jun 2025 13:58:43 GMT  
		Size: 10.3 KB (10327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:981313fe9db3103fc34231ccfc19f7e8c9662d4eaf220eaeb887a7ef9b8511c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacdd8c2029fb859fe9a3472e1f55c65a951c6d28c05a03eb48a2c0055797f71`

```dockerfile
```

-	Layers:
	-	`sha256:dbf46450f15bc13a9243f81ccfe97652be728992ef72454183344ce075364f5b`  
		Last Modified: Wed, 04 Jun 2025 04:58:33 GMT  
		Size: 12.3 MB (12299032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d0142f06753a116a2a8199a20c5179834d61f50a5c455408c59b4e388e240b`  
		Last Modified: Wed, 04 Jun 2025 04:58:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250608.0.361578`

**does not exist** (yet?)
