<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260412.0.513370`](#archlinuxbase-202604120513370)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260412.0.513370`](#archlinuxbase-devel-202604120513370)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260412.0.513370`](#archlinuxmultilib-devel-202604120513370)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:4c24063e3e3fa753b0c1f5cd0486ed5bee0173da61b1e73a3fb872f10163f760
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:510bead7bcbe2a4c190c1f1db94763d1ea079cf4612688f3ccc9ddfb6147de49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129432783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff30320934df1071bb33892039bfb4aa21d2c72a78c9a040f12c67ac9460c72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:47:07 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:47:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edfbbe617b176994dfb9c35ff5c72f5a5021c1716196804101a97c25fafd913e`  
		Last Modified: Mon, 13 Apr 2026 17:47:35 GMT  
		Size: 129.4 MB (129424120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229820f59e0fdb118794c698a40a0fc82ecea473c8e14450b8f6a95bdc06d70a`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 8.7 KB (8663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d52b5f2ccd08d6dbe7aaac42100605f6f4ed97675b2ab0b9d1b9d26d2a9ff095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0754ba67cd9dafd07ae5ff3d26801deefdf897b1900b56ac07eff89f4bc5e6`

```dockerfile
```

-	Layers:
	-	`sha256:5e94eedf2d40d7cae0d21ee55c053fac6252cd2e6497a3215e1350e5651f3c05`  
		Last Modified: Mon, 13 Apr 2026 17:47:33 GMT  
		Size: 8.2 MB (8178027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64d625bcea621f79c961584687324144e1f82c1a195eb77c7d1f43e6b9d04b4`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260412.0.513370`

```console
$ docker pull archlinux@sha256:4c24063e3e3fa753b0c1f5cd0486ed5bee0173da61b1e73a3fb872f10163f760
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260412.0.513370` - linux; amd64

```console
$ docker pull archlinux@sha256:510bead7bcbe2a4c190c1f1db94763d1ea079cf4612688f3ccc9ddfb6147de49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129432783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff30320934df1071bb33892039bfb4aa21d2c72a78c9a040f12c67ac9460c72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:47:07 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:47:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edfbbe617b176994dfb9c35ff5c72f5a5021c1716196804101a97c25fafd913e`  
		Last Modified: Mon, 13 Apr 2026 17:47:35 GMT  
		Size: 129.4 MB (129424120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229820f59e0fdb118794c698a40a0fc82ecea473c8e14450b8f6a95bdc06d70a`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 8.7 KB (8663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260412.0.513370` - unknown; unknown

```console
$ docker pull archlinux@sha256:d52b5f2ccd08d6dbe7aaac42100605f6f4ed97675b2ab0b9d1b9d26d2a9ff095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0754ba67cd9dafd07ae5ff3d26801deefdf897b1900b56ac07eff89f4bc5e6`

```dockerfile
```

-	Layers:
	-	`sha256:5e94eedf2d40d7cae0d21ee55c053fac6252cd2e6497a3215e1350e5651f3c05`  
		Last Modified: Mon, 13 Apr 2026 17:47:33 GMT  
		Size: 8.2 MB (8178027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64d625bcea621f79c961584687324144e1f82c1a195eb77c7d1f43e6b9d04b4`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:01bd0ee1c23c3dec1dcb0fce558150a222ee2ef0a3776404de33d0714bcefbb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3cf6781e229fc3f9e0b8740857d95b84e5580309285afc351c3a1b441a958c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247090944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125a2089ec4ace006ce7c1d29e9adf6c4e60b733bbc5f2693be553599c5af18`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:48:19 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:48:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:48:24 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:48:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5c1f30f5a8968675635fdbe2ce53d92208401558240cf52fcdaf22993ac0aaca`  
		Last Modified: Mon, 13 Apr 2026 17:49:09 GMT  
		Size: 247.1 MB (247081762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e94337e7f0c30454b4def77c429066ed4fad19ffca83181b7a4858d476d7ec`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:cb476b5d33482050fc27c94471173ba6e3d41f6b5ef0e172b69388c66e398807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11976487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85cb3cfb350c2454a21fe35cc3be4457372cad982fef9532da64b52ed9c6e07`

```dockerfile
```

-	Layers:
	-	`sha256:6e62e15360dc69f393c8ebe706c1934b098ae02631dfc76d7049a70b0a037081`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 12.0 MB (11964776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67fd359350dea2789a482ec3a1e4ac7066824f66716cfe0cee0bed232ed06d7`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260412.0.513370`

```console
$ docker pull archlinux@sha256:01bd0ee1c23c3dec1dcb0fce558150a222ee2ef0a3776404de33d0714bcefbb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260412.0.513370` - linux; amd64

```console
$ docker pull archlinux@sha256:3cf6781e229fc3f9e0b8740857d95b84e5580309285afc351c3a1b441a958c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247090944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125a2089ec4ace006ce7c1d29e9adf6c4e60b733bbc5f2693be553599c5af18`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:48:19 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:48:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:48:24 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:48:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5c1f30f5a8968675635fdbe2ce53d92208401558240cf52fcdaf22993ac0aaca`  
		Last Modified: Mon, 13 Apr 2026 17:49:09 GMT  
		Size: 247.1 MB (247081762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e94337e7f0c30454b4def77c429066ed4fad19ffca83181b7a4858d476d7ec`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260412.0.513370` - unknown; unknown

```console
$ docker pull archlinux@sha256:cb476b5d33482050fc27c94471173ba6e3d41f6b5ef0e172b69388c66e398807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11976487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85cb3cfb350c2454a21fe35cc3be4457372cad982fef9532da64b52ed9c6e07`

```dockerfile
```

-	Layers:
	-	`sha256:6e62e15360dc69f393c8ebe706c1934b098ae02631dfc76d7049a70b0a037081`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 12.0 MB (11964776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67fd359350dea2789a482ec3a1e4ac7066824f66716cfe0cee0bed232ed06d7`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:4c24063e3e3fa753b0c1f5cd0486ed5bee0173da61b1e73a3fb872f10163f760
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:510bead7bcbe2a4c190c1f1db94763d1ea079cf4612688f3ccc9ddfb6147de49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129432783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff30320934df1071bb33892039bfb4aa21d2c72a78c9a040f12c67ac9460c72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:47:07 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:47:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edfbbe617b176994dfb9c35ff5c72f5a5021c1716196804101a97c25fafd913e`  
		Last Modified: Mon, 13 Apr 2026 17:47:35 GMT  
		Size: 129.4 MB (129424120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229820f59e0fdb118794c698a40a0fc82ecea473c8e14450b8f6a95bdc06d70a`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 8.7 KB (8663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d52b5f2ccd08d6dbe7aaac42100605f6f4ed97675b2ab0b9d1b9d26d2a9ff095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0754ba67cd9dafd07ae5ff3d26801deefdf897b1900b56ac07eff89f4bc5e6`

```dockerfile
```

-	Layers:
	-	`sha256:5e94eedf2d40d7cae0d21ee55c053fac6252cd2e6497a3215e1350e5651f3c05`  
		Last Modified: Mon, 13 Apr 2026 17:47:33 GMT  
		Size: 8.2 MB (8178027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64d625bcea621f79c961584687324144e1f82c1a195eb77c7d1f43e6b9d04b4`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:3fc2ead62b076c22a52de9356a2fdae5267a6b367d9738fc1603bddaf33e3168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:17244fb6581e539cc7582d0245ea93743efcad4c627ab78f0ed97f6f80427238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e999681263a5c23a0ea934cdf7a39ab4ddc6fd4693e2c53997a620b2e4e9a581`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:48:07 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:48:13 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:48:13 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:48:13 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58f17d36b1f875da33d63bcf8aca97555ff01fd66e8541aa5ba8046f40f02bde`  
		Last Modified: Mon, 13 Apr 2026 17:49:04 GMT  
		Size: 269.2 MB (269241935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b812d701975c8357fdd24cf8b88562d605ff90a39c598732dd8cf60faf2477aa`  
		Last Modified: Mon, 13 Apr 2026 17:48:58 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e4dea3319f9fb499ee404b78bcdda52e5353bec086842311f24f130c8b66323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4831d50e6b528c2eb42c5b602d70f3c272838e63e126237ba9db773aa1b9d052`

```dockerfile
```

-	Layers:
	-	`sha256:129b444e2b9c38ae6eae5ea7ae02a5626150812c5b5567277820b172bc6898f0`  
		Last Modified: Mon, 13 Apr 2026 17:48:58 GMT  
		Size: 12.2 MB (12234646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:466953aaadf55676730564b99e589d6133a87673fe345bfe02699e3e518b9854`  
		Last Modified: Mon, 13 Apr 2026 17:48:57 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260412.0.513370`

```console
$ docker pull archlinux@sha256:3fc2ead62b076c22a52de9356a2fdae5267a6b367d9738fc1603bddaf33e3168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260412.0.513370` - linux; amd64

```console
$ docker pull archlinux@sha256:17244fb6581e539cc7582d0245ea93743efcad4c627ab78f0ed97f6f80427238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e999681263a5c23a0ea934cdf7a39ab4ddc6fd4693e2c53997a620b2e4e9a581`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:48:07 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:48:13 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:48:13 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:48:13 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58f17d36b1f875da33d63bcf8aca97555ff01fd66e8541aa5ba8046f40f02bde`  
		Last Modified: Mon, 13 Apr 2026 17:49:04 GMT  
		Size: 269.2 MB (269241935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b812d701975c8357fdd24cf8b88562d605ff90a39c598732dd8cf60faf2477aa`  
		Last Modified: Mon, 13 Apr 2026 17:48:58 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260412.0.513370` - unknown; unknown

```console
$ docker pull archlinux@sha256:e4dea3319f9fb499ee404b78bcdda52e5353bec086842311f24f130c8b66323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4831d50e6b528c2eb42c5b602d70f3c272838e63e126237ba9db773aa1b9d052`

```dockerfile
```

-	Layers:
	-	`sha256:129b444e2b9c38ae6eae5ea7ae02a5626150812c5b5567277820b172bc6898f0`  
		Last Modified: Mon, 13 Apr 2026 17:48:58 GMT  
		Size: 12.2 MB (12234646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:466953aaadf55676730564b99e589d6133a87673fe345bfe02699e3e518b9854`  
		Last Modified: Mon, 13 Apr 2026 17:48:57 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
