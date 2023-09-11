<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230910.0.177821`](#archlinuxbase-202309100177821)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230910.0.177821`](#archlinuxbase-devel-202309100177821)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:b29dab0d5f362cfe2ed4662c46f27855681d56fb548fd2f6d927fd573131178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:e21266b93a65192313d3857651abf2b5a194bad9438b3d8a565aeeb3b4400d5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146839994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1105a6ef005205836e53206cc7caf132c09b408b34e45cee059c2beda11a1188`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 24 Jul 2023 22:19:49 GMT
LABEL org.opencontainers.image.version=20230723.0.166908
# Mon, 24 Jul 2023 22:19:49 GMT
LABEL org.opencontainers.image.revision=301942f9e5995770cb5e4dedb4fe9166afa4806d
# Mon, 24 Jul 2023 22:19:49 GMT
LABEL org.opencontainers.image.created=2023-07-23T00:07:48+00:00
# Mon, 24 Jul 2023 22:19:55 GMT
COPY dir:e476a1d0c4718704b5b5b632f6fd36c05209de348495fc04ae8d8d978905fdc4 in / 
# Mon, 24 Jul 2023 22:19:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230723.0.166908' /etc/os-release
# Mon, 24 Jul 2023 22:19:57 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jul 2023 22:19:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:87df56ae4a93ddebdf3e602f51ec00a4846561f7d5e516e5ef1396c1778e6f1a`  
		Last Modified: Mon, 24 Jul 2023 22:21:41 GMT  
		Size: 146.8 MB (146831902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7171264b9dde16fa667a907717acc72fad7c38e3424ef7ab558f3ad20d8b783e`  
		Last Modified: Mon, 24 Jul 2023 22:21:21 GMT  
		Size: 8.1 KB (8092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20230910.0.177821`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:4a5ba44e5cb4bf49932da6d2ba9dbdb04ac6843fe40568c5479a218e6163b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0177814601cc10b58d4364bb790c8ce0c17db10d48a7c8da54a1f697253159e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263720287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51879f7f2befde96ccc332d360e00da3159a6eb351cd65e046307eb66fe1c74a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 24 Jul 2023 22:20:47 GMT
LABEL org.opencontainers.image.version=20230723.0.166908
# Mon, 24 Jul 2023 22:20:47 GMT
LABEL org.opencontainers.image.revision=301942f9e5995770cb5e4dedb4fe9166afa4806d
# Mon, 24 Jul 2023 22:20:47 GMT
LABEL org.opencontainers.image.created=2023-07-23T00:07:51+00:00
# Mon, 24 Jul 2023 22:20:58 GMT
COPY dir:0b871f5e73e52537b3829dfbffbd8ef04e46de7d619959305deb2d62e1d8e596 in / 
# Mon, 24 Jul 2023 22:21:01 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230723.0.166908' /etc/os-release
# Mon, 24 Jul 2023 22:21:01 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jul 2023 22:21:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7db0a613b381eb6bf1765e6d2670a1d1e353b8bcfb7effef0675494727728006`  
		Last Modified: Mon, 24 Jul 2023 22:22:27 GMT  
		Size: 263.7 MB (263711445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0549be721c1ee7c45a29e67e47ab6ec2608500d98dd3d436547da2e6f8ebc7a6`  
		Last Modified: Mon, 24 Jul 2023 22:21:52 GMT  
		Size: 8.8 KB (8842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230910.0.177821`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:b29dab0d5f362cfe2ed4662c46f27855681d56fb548fd2f6d927fd573131178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e21266b93a65192313d3857651abf2b5a194bad9438b3d8a565aeeb3b4400d5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146839994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1105a6ef005205836e53206cc7caf132c09b408b34e45cee059c2beda11a1188`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 24 Jul 2023 22:19:49 GMT
LABEL org.opencontainers.image.version=20230723.0.166908
# Mon, 24 Jul 2023 22:19:49 GMT
LABEL org.opencontainers.image.revision=301942f9e5995770cb5e4dedb4fe9166afa4806d
# Mon, 24 Jul 2023 22:19:49 GMT
LABEL org.opencontainers.image.created=2023-07-23T00:07:48+00:00
# Mon, 24 Jul 2023 22:19:55 GMT
COPY dir:e476a1d0c4718704b5b5b632f6fd36c05209de348495fc04ae8d8d978905fdc4 in / 
# Mon, 24 Jul 2023 22:19:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230723.0.166908' /etc/os-release
# Mon, 24 Jul 2023 22:19:57 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jul 2023 22:19:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:87df56ae4a93ddebdf3e602f51ec00a4846561f7d5e516e5ef1396c1778e6f1a`  
		Last Modified: Mon, 24 Jul 2023 22:21:41 GMT  
		Size: 146.8 MB (146831902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7171264b9dde16fa667a907717acc72fad7c38e3424ef7ab558f3ad20d8b783e`  
		Last Modified: Mon, 24 Jul 2023 22:21:21 GMT  
		Size: 8.1 KB (8092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
