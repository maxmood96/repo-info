<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240908.0.261281`](#archlinuxbase-202409080261281)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240908.0.261281`](#archlinuxbase-devel-202409080261281)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240908.0.261281`](#archlinuxmultilib-devel-202409080261281)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:dd8a773cb2aba170c094eecefa0da4256a008aff1c04a8ac9fc31f09cf025b81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:d37c2099060d7fa67d030e6cbe99b7c2c7f83633061259dd129770b36b26060f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151183302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0f676c66b87046098aab121b83ee673e8a59e7dd50ee2c41aa78b68054c1d6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a7eeb2be9236376dfb256be5af295b286214fd6f9583c91a99e5de0a412b7dd`  
		Last Modified: Mon, 26 Aug 2024 21:59:19 GMT  
		Size: 151.2 MB (151175032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23212d7e0f449ec376716945b27db2edcd57185f27775f7e89077106953412ee`  
		Last Modified: Fri, 06 Sep 2024 23:15:36 GMT  
		Size: 8.3 KB (8270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:f3f6a38692e6e30c3f986125d18a77fc180df261a24e1d8733ee4fdec4457fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca11434f2170ec4b7003c7a2c24ff209aa2437a9a187d2f9e584bb71f4b6b366`

```dockerfile
```

-	Layers:
	-	`sha256:3187d9bc1560d66b1a5ed06531edcb25caeb9d8141050d86c52b74ae49cc0b54`  
		Last Modified: Fri, 06 Sep 2024 23:15:36 GMT  
		Size: 8.1 MB (8103979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825c3ce96872d1bd42836159301ba69d468b1da7ca9490e5553edab65b66b3a3`  
		Last Modified: Fri, 06 Sep 2024 23:15:36 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240908.0.261281`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:2545b996b2de70ecc0293b8a607a31a2891396c182abb04af16e7d50ce9aee86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7488d90124dc3da3a43d2e941e599b974231967e2eab3eb697073a2e3448c97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271737203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc794c1bb8ce2a774f5b9bf9b041a1989ec39db83f65f5d84f676cfe9addb482`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:298dc0d2952244fad2540d1cd7765c9b3beb1fae3ae90fe74a9d3339125caf9b`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 271.7 MB (271728156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f3cf16aeba7031d385266919b9a059ee62a2ccfcd28b31da49d224b4781b2c`  
		Last Modified: Fri, 06 Sep 2024 23:15:55 GMT  
		Size: 9.0 KB (9047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5869b63583420d83894585cd1eae07f9dc1a206039e25abe5a837bcf8b03be37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7123064c45280af89ccac6015287201622cde7cd89078b1471e975829fd4c03b`

```dockerfile
```

-	Layers:
	-	`sha256:aff2027bf5ca9aaecf2ac91cdf300953623057ec5061c504772d192b9108af02`  
		Last Modified: Fri, 06 Sep 2024 23:15:56 GMT  
		Size: 11.8 MB (11818188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b9ed633a0af93cdc69f8b0e03a37ea3553b200878151251e08abfa1d82800c`  
		Last Modified: Fri, 06 Sep 2024 23:15:55 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240908.0.261281`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:dd8a773cb2aba170c094eecefa0da4256a008aff1c04a8ac9fc31f09cf025b81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:d37c2099060d7fa67d030e6cbe99b7c2c7f83633061259dd129770b36b26060f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151183302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0f676c66b87046098aab121b83ee673e8a59e7dd50ee2c41aa78b68054c1d6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a7eeb2be9236376dfb256be5af295b286214fd6f9583c91a99e5de0a412b7dd`  
		Last Modified: Mon, 26 Aug 2024 21:59:19 GMT  
		Size: 151.2 MB (151175032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23212d7e0f449ec376716945b27db2edcd57185f27775f7e89077106953412ee`  
		Last Modified: Fri, 06 Sep 2024 23:15:36 GMT  
		Size: 8.3 KB (8270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:f3f6a38692e6e30c3f986125d18a77fc180df261a24e1d8733ee4fdec4457fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca11434f2170ec4b7003c7a2c24ff209aa2437a9a187d2f9e584bb71f4b6b366`

```dockerfile
```

-	Layers:
	-	`sha256:3187d9bc1560d66b1a5ed06531edcb25caeb9d8141050d86c52b74ae49cc0b54`  
		Last Modified: Fri, 06 Sep 2024 23:15:36 GMT  
		Size: 8.1 MB (8103979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825c3ce96872d1bd42836159301ba69d468b1da7ca9490e5553edab65b66b3a3`  
		Last Modified: Fri, 06 Sep 2024 23:15:36 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:10912b44e838dd335ff9bcb38995c4807bbe8aa293623190afb3afd2716760de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:eff11b75a9bc18500f7d71b4cce218dde3483a05a02139eb4b3efb31da889fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321627596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ae1e385fa3ca79af934bfcfd4bdd1273b8ec5152ea3953424dcd302074d874`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b39c3f3d5831908f56eae8d8bceedb49c7424402515d9cf9b1feb3ba6c022781`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 321.6 MB (321617407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0ba7ee9a3b8b9b42fdce4d1f2c978a00e0c0a19a83a4e96752beb6e8a39cc7`  
		Last Modified: Fri, 06 Sep 2024 23:16:19 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0b811b6d24805858211a5c565f2d8f752a1fc3ece91eb130c201f60f3061855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49213f8b851b3c29d88b3e8b302b4a1f776557358da20274d1242f17425e7fae`

```dockerfile
```

-	Layers:
	-	`sha256:4b24a7253625f628d2c7b94757fde4664420b577841f858c78d1a010852537ad`  
		Last Modified: Fri, 06 Sep 2024 23:16:19 GMT  
		Size: 12.1 MB (12085490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e51c63051759cef7e90e1c7694d3db27d97a990e39666f462e16456ab891d13`  
		Last Modified: Fri, 06 Sep 2024 23:16:19 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240908.0.261281`

**does not exist** (yet?)
