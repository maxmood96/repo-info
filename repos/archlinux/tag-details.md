<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240101.0.204074`](#archlinuxbase-202401010204074)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240101.0.204074`](#archlinuxbase-devel-202401010204074)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240101.0.204074`](#archlinuxmultilib-devel-202401010204074)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:e0cdf8208d276f77eaba78e1ef0e94f7a70c15090cfc09299be5521ceb4a0705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:2fe50139e8eff5be59fffa698e09003df948e655a3fd4e841b15e858e4982ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350179b164059944a654dfab989fddbb68a8e857dacc97777e3b625aa418155b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc4fe693d3a172aaa30338898d9358941319d1114416838bbdc38e762ece972`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 8.2 KB (8152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:4bfed7edac7290affed5bd244ee801be39a21a77d6720c8fba25f2244edfc1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7813966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6adf6ab28a1db76d18f8e5817bd69b096ff53792075f2c4e6bdcac25fcbba85`

```dockerfile
```

-	Layers:
	-	`sha256:af2795535157dbf5923f794df4a6b3287816159811c94c924a62e2fb96ade8f1`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 7.8 MB (7802294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842e8ca534a4db9ef4c4f93594e2291833dde88df585ed57339c67f8e805bd7d`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 11.7 KB (11672 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240101.0.204074`

```console
$ docker pull archlinux@sha256:e0cdf8208d276f77eaba78e1ef0e94f7a70c15090cfc09299be5521ceb4a0705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:2fe50139e8eff5be59fffa698e09003df948e655a3fd4e841b15e858e4982ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350179b164059944a654dfab989fddbb68a8e857dacc97777e3b625aa418155b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc4fe693d3a172aaa30338898d9358941319d1114416838bbdc38e762ece972`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 8.2 KB (8152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20240101.0.204074` - unknown; unknown

```console
$ docker pull archlinux@sha256:4bfed7edac7290affed5bd244ee801be39a21a77d6720c8fba25f2244edfc1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7813966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6adf6ab28a1db76d18f8e5817bd69b096ff53792075f2c4e6bdcac25fcbba85`

```dockerfile
```

-	Layers:
	-	`sha256:af2795535157dbf5923f794df4a6b3287816159811c94c924a62e2fb96ade8f1`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 7.8 MB (7802294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842e8ca534a4db9ef4c4f93594e2291833dde88df585ed57339c67f8e805bd7d`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 11.7 KB (11672 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:a20d103ba70c910b40a274748a0bbb43d96f4e37ef45ce367c080aee370dfde8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f5d80e223b925204224653f63ddc2bdb2ece26691cad67c3a7e526a0f1147f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4009240989a60ea769d91858d428615edb2ee2ac54fa2e1fe85883b83548bc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad59c724b2d7e7041a88eae078be10f472732091bab7b3ff59e2bbd5056e65f6`  
		Last Modified: Wed, 29 May 2024 19:57:22 GMT  
		Size: 266.2 MB (266230027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e81a3aeb405ec80b4084aef14b8997cea2a066263c3b5bf3218dde94801e58`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 8.9 KB (8939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d61ec44f785a760a1381e1283aaa568c4704a72073bef9e65499dc9286369b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11443681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3997782d4cceaf17cb4eedd076574ed31d5c32d445e56e496d3c466fcba40f8`

```dockerfile
```

-	Layers:
	-	`sha256:c104f7a606c0dd987c990b87afe2b92e5803be27f08b84047589192c1213ba91`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 11.4 MB (11432227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce3c5f8e22cac3c19169bb8b5c9e7bfa626a32629acf911dbc0a8f73f51feef`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 11.5 KB (11454 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:a20d103ba70c910b40a274748a0bbb43d96f4e37ef45ce367c080aee370dfde8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:f5d80e223b925204224653f63ddc2bdb2ece26691cad67c3a7e526a0f1147f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4009240989a60ea769d91858d428615edb2ee2ac54fa2e1fe85883b83548bc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad59c724b2d7e7041a88eae078be10f472732091bab7b3ff59e2bbd5056e65f6`  
		Last Modified: Wed, 29 May 2024 19:57:22 GMT  
		Size: 266.2 MB (266230027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e81a3aeb405ec80b4084aef14b8997cea2a066263c3b5bf3218dde94801e58`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 8.9 KB (8939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240101.0.204074` - unknown; unknown

```console
$ docker pull archlinux@sha256:d61ec44f785a760a1381e1283aaa568c4704a72073bef9e65499dc9286369b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11443681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3997782d4cceaf17cb4eedd076574ed31d5c32d445e56e496d3c466fcba40f8`

```dockerfile
```

-	Layers:
	-	`sha256:c104f7a606c0dd987c990b87afe2b92e5803be27f08b84047589192c1213ba91`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 11.4 MB (11432227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce3c5f8e22cac3c19169bb8b5c9e7bfa626a32629acf911dbc0a8f73f51feef`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 11.5 KB (11454 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:e0cdf8208d276f77eaba78e1ef0e94f7a70c15090cfc09299be5521ceb4a0705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2fe50139e8eff5be59fffa698e09003df948e655a3fd4e841b15e858e4982ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350179b164059944a654dfab989fddbb68a8e857dacc97777e3b625aa418155b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc4fe693d3a172aaa30338898d9358941319d1114416838bbdc38e762ece972`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 8.2 KB (8152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:4bfed7edac7290affed5bd244ee801be39a21a77d6720c8fba25f2244edfc1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7813966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6adf6ab28a1db76d18f8e5817bd69b096ff53792075f2c4e6bdcac25fcbba85`

```dockerfile
```

-	Layers:
	-	`sha256:af2795535157dbf5923f794df4a6b3287816159811c94c924a62e2fb96ade8f1`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 7.8 MB (7802294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842e8ca534a4db9ef4c4f93594e2291833dde88df585ed57339c67f8e805bd7d`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 11.7 KB (11672 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:ad0fb9c2da48cbb7c38ec278819fa6c0ccf321e910750059ffd3311478aa4a68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e178965db0bcd548d8708b185b75bbf7baa9610c87707395e09a4b3936db24fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316042474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c36062429000daee9967c3a6c523fbf4b7025aeb4408f69746b60e5c9d29d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35515117493e52c38adb77412e5d70e1c716a60977e0d1bad3b1ed7e46700be3`  
		Last Modified: Wed, 29 May 2024 19:57:38 GMT  
		Size: 316.0 MB (316032410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad89dbd88444ae98e574e40539b211581ed6c64271ddf0e53c7b32fa645b974`  
		Last Modified: Wed, 29 May 2024 19:57:34 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:6203d19901e030ab0daec80b608b3db9e3fe8051d6f16aa6401075a7a51871b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11702905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a656c662bc10d622ea50e9941ccb5df83f39084ad8014f45a12734f6053ebf85`

```dockerfile
```

-	Layers:
	-	`sha256:2196da55d05a9d7a7fb16e898751b96da5e8ba62b27b617af1c53f23a3404d9b`  
		Last Modified: Wed, 29 May 2024 19:57:34 GMT  
		Size: 11.7 MB (11691394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2c8dc4fc5ca08b34ef8009248a3fb39dbea4ab5c111952b3d8622e6eb3d702`  
		Last Modified: Wed, 29 May 2024 19:57:33 GMT  
		Size: 11.5 KB (11511 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:ad0fb9c2da48cbb7c38ec278819fa6c0ccf321e910750059ffd3311478aa4a68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:e178965db0bcd548d8708b185b75bbf7baa9610c87707395e09a4b3936db24fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316042474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c36062429000daee9967c3a6c523fbf4b7025aeb4408f69746b60e5c9d29d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35515117493e52c38adb77412e5d70e1c716a60977e0d1bad3b1ed7e46700be3`  
		Last Modified: Wed, 29 May 2024 19:57:38 GMT  
		Size: 316.0 MB (316032410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad89dbd88444ae98e574e40539b211581ed6c64271ddf0e53c7b32fa645b974`  
		Last Modified: Wed, 29 May 2024 19:57:34 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240101.0.204074` - unknown; unknown

```console
$ docker pull archlinux@sha256:6203d19901e030ab0daec80b608b3db9e3fe8051d6f16aa6401075a7a51871b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11702905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a656c662bc10d622ea50e9941ccb5df83f39084ad8014f45a12734f6053ebf85`

```dockerfile
```

-	Layers:
	-	`sha256:2196da55d05a9d7a7fb16e898751b96da5e8ba62b27b617af1c53f23a3404d9b`  
		Last Modified: Wed, 29 May 2024 19:57:34 GMT  
		Size: 11.7 MB (11691394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2c8dc4fc5ca08b34ef8009248a3fb39dbea4ab5c111952b3d8622e6eb3d702`  
		Last Modified: Wed, 29 May 2024 19:57:33 GMT  
		Size: 11.5 KB (11511 bytes)  
		MIME: application/vnd.in-toto+json
