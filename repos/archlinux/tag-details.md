<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250817.0.405639`](#archlinuxbase-202508170405639)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250817.0.405639`](#archlinuxbase-devel-202508170405639)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250817.0.405639`](#archlinuxmultilib-devel-202508170405639)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:104d24b4464e89a16566d3e68ce0e2707aa15258c690ee9bef755930e8bc1c2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c8c254d98a4d8a768a3df6664727d7fc47c62b7fe680db014182c7d5745cd63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168824318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e8ea7cbe1d296ba02abd87dec90b798901bc5324b4562bce7438ac7d44cdc2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250810.0.398652
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-08-10T00:07:35+00:00
# Sun, 10 Aug 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250810.0.398652' /etc/os-release # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 10 Aug 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:99c7ced3048ae449d7bbe868fdaae1794ddf29670e0a8e66476355dce22d3e82`  
		Last Modified: Mon, 11 Aug 2025 19:48:29 GMT  
		Size: 168.8 MB (168815972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f76e6e58198908de29c433b05f6a58a12cf634457cf1353c9f7f150646842`  
		Last Modified: Mon, 11 Aug 2025 16:41:46 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:40122200033cb0780c5a2d37e455c41bfa7e966c438a24262be35ec377878c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e70a861316fb14ab79d0433bea4832f12d70583ddb6b1cf05a96b63efef04d`

```dockerfile
```

-	Layers:
	-	`sha256:11e6c7542a04c87bb06d2a610e86d83337140b55ab0c91292b1bc92a51e5c54d`  
		Last Modified: Mon, 11 Aug 2025 19:48:19 GMT  
		Size: 8.2 MB (8162399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd693ca89249bed05ff6361ea9f9065ca971e556d84cbd5c62692652700f323`  
		Last Modified: Mon, 11 Aug 2025 19:48:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250817.0.405639`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:92a0740113bd2af7f38bf7c9992efd5ee61e745e9934326eb50ecdf24495b055
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7bf5d00a7e8473652564baba1da92ca3ad2db6ad9855b0a3255aabe68411c778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307034893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952307d2bab25b4808157fe3ed835868bea8b5954145ffa666e39f61eb40e8ac`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250810.0.398652
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-08-10T00:07:35+00:00
# Sun, 10 Aug 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250810.0.398652' /etc/os-release # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 10 Aug 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:515896c7cc7d6fef4d3fbf34e346c6c9051e0be95d5d732aa229d9f351acf9fb`  
		Last Modified: Mon, 11 Aug 2025 19:50:19 GMT  
		Size: 307.0 MB (307025742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1db20b211cf7a03cc50031438ce24251d1ce629d977877be6c7141737dc4b92`  
		Last Modified: Mon, 11 Aug 2025 16:41:44 GMT  
		Size: 9.2 KB (9151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5ee14bacfba5eaa81d8eabb78565830b81ab0d654ed403b9fe9934b50bd71b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b55c988109051f320608ad79249a3c615f470894eb60c3d37e36041586ca43`

```dockerfile
```

-	Layers:
	-	`sha256:0ebd39a228b0ed224fae0d9cd176039aaf0fb24f45d018747c60b0d231e5ec11`  
		Last Modified: Mon, 11 Aug 2025 19:48:21 GMT  
		Size: 12.1 MB (12063807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0339765509ae6229a50dbe98118fa7cfe5e72b53130521b9a8d8ef462a73313a`  
		Last Modified: Mon, 11 Aug 2025 19:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250817.0.405639`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:104d24b4464e89a16566d3e68ce0e2707aa15258c690ee9bef755930e8bc1c2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c8c254d98a4d8a768a3df6664727d7fc47c62b7fe680db014182c7d5745cd63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168824318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e8ea7cbe1d296ba02abd87dec90b798901bc5324b4562bce7438ac7d44cdc2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250810.0.398652
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-08-10T00:07:35+00:00
# Sun, 10 Aug 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250810.0.398652' /etc/os-release # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 10 Aug 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:99c7ced3048ae449d7bbe868fdaae1794ddf29670e0a8e66476355dce22d3e82`  
		Last Modified: Mon, 11 Aug 2025 19:48:29 GMT  
		Size: 168.8 MB (168815972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f76e6e58198908de29c433b05f6a58a12cf634457cf1353c9f7f150646842`  
		Last Modified: Mon, 11 Aug 2025 16:41:46 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:40122200033cb0780c5a2d37e455c41bfa7e966c438a24262be35ec377878c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e70a861316fb14ab79d0433bea4832f12d70583ddb6b1cf05a96b63efef04d`

```dockerfile
```

-	Layers:
	-	`sha256:11e6c7542a04c87bb06d2a610e86d83337140b55ab0c91292b1bc92a51e5c54d`  
		Last Modified: Mon, 11 Aug 2025 19:48:19 GMT  
		Size: 8.2 MB (8162399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd693ca89249bed05ff6361ea9f9065ca971e556d84cbd5c62692652700f323`  
		Last Modified: Mon, 11 Aug 2025 19:48:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:ceeeca91f88305fcc3d59761f080368aacb113c1ea5f708920995e9ed3a159f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:9c3d9e65a6d665d2b4c760f4df0bb75b6deb1187b455bb161dcebc8220bc9f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.3 MB (358324402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc68686ebb40e48897d5b92bb3333e06bd1213ba1fd76602a2533f0209a73ab9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250810.0.398652
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-08-10T00:07:35+00:00
# Sun, 10 Aug 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250810.0.398652' /etc/os-release # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 10 Aug 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:71ca4fc96d00bd13faa0c13bb0699fd58f80215ed66560f5b200c969c5ebbd46`  
		Last Modified: Mon, 11 Aug 2025 20:17:20 GMT  
		Size: 358.3 MB (358314134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b176c205797d706d232f226326cdb8661940a88bfcb3ba704464585b00653bc5`  
		Last Modified: Mon, 11 Aug 2025 17:07:07 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:258b6fab39a9b9124f18790a2a065d37a7102ea05798f1493a8f5004040a32c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72d5e4161c5a7d8a86146940e9962d98d03eb35ab9105db383edee231032070`

```dockerfile
```

-	Layers:
	-	`sha256:4fed8fac575a94c0b42f20f24a3cf7f934f24cba15df71a0075c56b071f37207`  
		Last Modified: Mon, 11 Aug 2025 19:48:25 GMT  
		Size: 12.3 MB (12332701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80490166b61838f075b438b351c109682a4e470475787eb01d605c3eaac90a93`  
		Last Modified: Mon, 11 Aug 2025 19:48:26 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250817.0.405639`

**does not exist** (yet?)
