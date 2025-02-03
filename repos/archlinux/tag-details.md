<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250202.0.304438`](#archlinuxbase-202502020304438)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250202.0.304438`](#archlinuxbase-devel-202502020304438)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250202.0.304438`](#archlinuxmultilib-devel-202502020304438)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:bf256af6457f18c60316bdab5a86dfa6b212f4f4d0098098429e363b4d5db0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c13557438a1df09698ff8af836a22d36e0436ac02a1475c87bd8fc913bf4884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157487905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db11dbb531b7976426052ea28befbe1286c8a3da35adbe238c28caf9a51e5e9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:983e51fa3b68b5be32c985411449c562ed0a4e1f8631f8baad0878c18df1aa63`  
		Last Modified: Mon, 03 Feb 2025 19:27:22 GMT  
		Size: 157.5 MB (157479617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aaa455fa3c07708f646372e36175ac8826a50c00806f619ed2084912c97beb`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.3 KB (8288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:8bf846c4a8058e4869ef41af8f1dca2f6cd294204ea342d3e70346a30d3ef236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932f834ec3174f77586f20a7aec0118382fb02f49272fc49732adc5390858022`

```dockerfile
```

-	Layers:
	-	`sha256:aa1305d78119fe6f5c1b7e5d7a50bcfa578611712c5528a9a2fe8fc091c86270`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.1 MB (8088477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143c44261d7ea6dc4b78f3a28f36cc6bafc901eedd72653bec7d8caba4baa69`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250202.0.304438`

```console
$ docker pull archlinux@sha256:bf256af6457f18c60316bdab5a86dfa6b212f4f4d0098098429e363b4d5db0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250202.0.304438` - linux; amd64

```console
$ docker pull archlinux@sha256:c13557438a1df09698ff8af836a22d36e0436ac02a1475c87bd8fc913bf4884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157487905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db11dbb531b7976426052ea28befbe1286c8a3da35adbe238c28caf9a51e5e9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:983e51fa3b68b5be32c985411449c562ed0a4e1f8631f8baad0878c18df1aa63`  
		Last Modified: Mon, 03 Feb 2025 19:27:22 GMT  
		Size: 157.5 MB (157479617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aaa455fa3c07708f646372e36175ac8826a50c00806f619ed2084912c97beb`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.3 KB (8288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250202.0.304438` - unknown; unknown

```console
$ docker pull archlinux@sha256:8bf846c4a8058e4869ef41af8f1dca2f6cd294204ea342d3e70346a30d3ef236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932f834ec3174f77586f20a7aec0118382fb02f49272fc49732adc5390858022`

```dockerfile
```

-	Layers:
	-	`sha256:aa1305d78119fe6f5c1b7e5d7a50bcfa578611712c5528a9a2fe8fc091c86270`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.1 MB (8088477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143c44261d7ea6dc4b78f3a28f36cc6bafc901eedd72653bec7d8caba4baa69`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:60aaac6e5cb608323480bc3b49e9110183f3dba6baa0c5e57dc315f4365bdf42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:81e52e1f2371eb0aa8cabc06ceb0a5dd83a8922874a898dfa0680d65bfe2964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278602887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbea432e68fcb65b7085457fb60714e702b07d8d4a871be547b57c7ff75b811a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6132708ec3c2a0f14172f35bddb52ee1e6cc2a7780f822e4a251821b9be891fa`  
		Last Modified: Mon, 03 Feb 2025 19:28:00 GMT  
		Size: 278.6 MB (278593852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe56e40e02767b104fcfe35211e7cdc487c5a341081fda052a551126e48076a`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d976b5d33209fcad192e77e11601d050c099a6350d4074e4df423de7fd29ac68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f75131ec9424866f2afaa1c8cafd1ba7de562bcfaa287828dac08ecc655a922`

```dockerfile
```

-	Layers:
	-	`sha256:69ee1ac4478e893f3b2befd53892a58e151f7525b15cdc7657415cc4b2295449`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 11.9 MB (11895956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbacc84a84cc36008654c1644acc495f1f29b7171a78b35c11d5c30ea74137c`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250202.0.304438`

```console
$ docker pull archlinux@sha256:60aaac6e5cb608323480bc3b49e9110183f3dba6baa0c5e57dc315f4365bdf42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250202.0.304438` - linux; amd64

```console
$ docker pull archlinux@sha256:81e52e1f2371eb0aa8cabc06ceb0a5dd83a8922874a898dfa0680d65bfe2964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278602887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbea432e68fcb65b7085457fb60714e702b07d8d4a871be547b57c7ff75b811a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6132708ec3c2a0f14172f35bddb52ee1e6cc2a7780f822e4a251821b9be891fa`  
		Last Modified: Mon, 03 Feb 2025 19:28:00 GMT  
		Size: 278.6 MB (278593852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe56e40e02767b104fcfe35211e7cdc487c5a341081fda052a551126e48076a`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250202.0.304438` - unknown; unknown

```console
$ docker pull archlinux@sha256:d976b5d33209fcad192e77e11601d050c099a6350d4074e4df423de7fd29ac68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f75131ec9424866f2afaa1c8cafd1ba7de562bcfaa287828dac08ecc655a922`

```dockerfile
```

-	Layers:
	-	`sha256:69ee1ac4478e893f3b2befd53892a58e151f7525b15cdc7657415cc4b2295449`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 11.9 MB (11895956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbacc84a84cc36008654c1644acc495f1f29b7171a78b35c11d5c30ea74137c`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:bf256af6457f18c60316bdab5a86dfa6b212f4f4d0098098429e363b4d5db0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c13557438a1df09698ff8af836a22d36e0436ac02a1475c87bd8fc913bf4884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157487905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db11dbb531b7976426052ea28befbe1286c8a3da35adbe238c28caf9a51e5e9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:983e51fa3b68b5be32c985411449c562ed0a4e1f8631f8baad0878c18df1aa63`  
		Last Modified: Mon, 03 Feb 2025 19:27:22 GMT  
		Size: 157.5 MB (157479617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aaa455fa3c07708f646372e36175ac8826a50c00806f619ed2084912c97beb`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.3 KB (8288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:8bf846c4a8058e4869ef41af8f1dca2f6cd294204ea342d3e70346a30d3ef236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932f834ec3174f77586f20a7aec0118382fb02f49272fc49732adc5390858022`

```dockerfile
```

-	Layers:
	-	`sha256:aa1305d78119fe6f5c1b7e5d7a50bcfa578611712c5528a9a2fe8fc091c86270`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.1 MB (8088477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143c44261d7ea6dc4b78f3a28f36cc6bafc901eedd72653bec7d8caba4baa69`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:8354c1ea78242392e67387fb6b364d51eab0bdca51b989b516d1bbec70e91456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0d4df35c383a2e1e7c6b81c88327de5e487885a80d2eec5675519a31c2a5315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328460806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93c13b6197dd582433a8dc0023ad9977e18f3b5aeba8b235884838fa16bac88`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c1ff021d4b1d4d615e0bd2958452c80482e2d2e8f32790f3e1e3f6eb4161661e`  
		Last Modified: Mon, 03 Feb 2025 19:28:19 GMT  
		Size: 328.5 MB (328450566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775a06893295bab49f2edcf4f82a68924e3b8509f1238426974a29c9319f531b`  
		Last Modified: Mon, 03 Feb 2025 19:28:12 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:53879bb8197a47875c0ded6fdf648727bb3f5e08b1588b1d65d63bad7d1e2b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0129b605ab0bf1afa850a351f3fcecd67ccbb5dc4f982392fd858b06a770728`

```dockerfile
```

-	Layers:
	-	`sha256:b35a88c88b195ff883ef22ac9ceb94f3dcf917b3aa768999a4f00f7cc6ede0f3`  
		Last Modified: Mon, 03 Feb 2025 19:28:12 GMT  
		Size: 12.2 MB (12164476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec18124e57781805e7e82e2466ba295b7d913d4f1b4b5511fe9ef4701102e6ff`  
		Last Modified: Mon, 03 Feb 2025 19:28:11 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250202.0.304438`

```console
$ docker pull archlinux@sha256:8354c1ea78242392e67387fb6b364d51eab0bdca51b989b516d1bbec70e91456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250202.0.304438` - linux; amd64

```console
$ docker pull archlinux@sha256:0d4df35c383a2e1e7c6b81c88327de5e487885a80d2eec5675519a31c2a5315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328460806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93c13b6197dd582433a8dc0023ad9977e18f3b5aeba8b235884838fa16bac88`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c1ff021d4b1d4d615e0bd2958452c80482e2d2e8f32790f3e1e3f6eb4161661e`  
		Last Modified: Mon, 03 Feb 2025 19:28:19 GMT  
		Size: 328.5 MB (328450566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775a06893295bab49f2edcf4f82a68924e3b8509f1238426974a29c9319f531b`  
		Last Modified: Mon, 03 Feb 2025 19:28:12 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250202.0.304438` - unknown; unknown

```console
$ docker pull archlinux@sha256:53879bb8197a47875c0ded6fdf648727bb3f5e08b1588b1d65d63bad7d1e2b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0129b605ab0bf1afa850a351f3fcecd67ccbb5dc4f982392fd858b06a770728`

```dockerfile
```

-	Layers:
	-	`sha256:b35a88c88b195ff883ef22ac9ceb94f3dcf917b3aa768999a4f00f7cc6ede0f3`  
		Last Modified: Mon, 03 Feb 2025 19:28:12 GMT  
		Size: 12.2 MB (12164476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec18124e57781805e7e82e2466ba295b7d913d4f1b4b5511fe9ef4701102e6ff`  
		Last Modified: Mon, 03 Feb 2025 19:28:11 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
