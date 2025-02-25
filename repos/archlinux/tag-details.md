<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250223.0.312761`](#archlinuxbase-202502230312761)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250223.0.312761`](#archlinuxbase-devel-202502230312761)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250223.0.312761`](#archlinuxmultilib-devel-202502230312761)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:0dd90d4fc8e6d991810f57222fa3a2d926b34e4aa3adb1117857c4685def16cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a2ec6393d71cc4b5ec3b8749d6fb8ab46f3d7804542c778e58945425064a23a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158773606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0995e2d39d4e0e18432ae70b57f09667f40c6a73693dc9d294799696ab588e14`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:70c9c0bc740b2885ab94a3ed5f1f0f0d5c4e414d39b84d1a896a60ff68f74780`  
		Last Modified: Mon, 24 Feb 2025 20:29:08 GMT  
		Size: 158.8 MB (158765282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295b16ff000d323d54017b773a25cf28118f4ff9d132c428336b58a9babe9d`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0fabb023c7544271b4bc385ab045839cdd95c469b6c8524c94c61df3875f1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8159967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651998445313026f641596942a94b3c3c28fe08a0f26b25cca5de3c7d39e0a07`

```dockerfile
```

-	Layers:
	-	`sha256:3f7f9721672652bba099e96c2ad82f525143eef1f3346b9592ebb454eea5cf05`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.1 MB (8147996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a40a8731b74907e6ec9938e258510eab4b3cf6fad27261516338d66a7d833b2`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250223.0.312761`

```console
$ docker pull archlinux@sha256:0dd90d4fc8e6d991810f57222fa3a2d926b34e4aa3adb1117857c4685def16cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250223.0.312761` - linux; amd64

```console
$ docker pull archlinux@sha256:a2ec6393d71cc4b5ec3b8749d6fb8ab46f3d7804542c778e58945425064a23a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158773606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0995e2d39d4e0e18432ae70b57f09667f40c6a73693dc9d294799696ab588e14`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:70c9c0bc740b2885ab94a3ed5f1f0f0d5c4e414d39b84d1a896a60ff68f74780`  
		Last Modified: Mon, 24 Feb 2025 20:29:08 GMT  
		Size: 158.8 MB (158765282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295b16ff000d323d54017b773a25cf28118f4ff9d132c428336b58a9babe9d`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250223.0.312761` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0fabb023c7544271b4bc385ab045839cdd95c469b6c8524c94c61df3875f1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8159967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651998445313026f641596942a94b3c3c28fe08a0f26b25cca5de3c7d39e0a07`

```dockerfile
```

-	Layers:
	-	`sha256:3f7f9721672652bba099e96c2ad82f525143eef1f3346b9592ebb454eea5cf05`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.1 MB (8147996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a40a8731b74907e6ec9938e258510eab4b3cf6fad27261516338d66a7d833b2`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:cd39606466737d54e804fd5bad28c0fd195aba0042cd3c38c60aca14e281b895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:85a806225854c084f6122ff453517e22f5d998094bef13b0ad74f4f983250865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280244252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b648ccfa3dd5007f0201036d2d5803938cac01d6b7ca66c4cbbbc45a5b04cc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:52c18e014de0f10e1675122d732c121993497f96975726b19208798ac5ec9328`  
		Last Modified: Mon, 24 Feb 2025 20:29:41 GMT  
		Size: 280.2 MB (280235177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb5e786de9d4a3fd6ce9778e8a34ae5c72b3e36c34d7a4f9b63a6228fd8b61`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:71f1cea6167ec0211286fd788ff0c81677d8bbb823ecedbda9e6fcdc10665cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11980146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c0650c190dd2e5181a313618f945c98df1f28b3eb86d80df6ead6591681d39`

```dockerfile
```

-	Layers:
	-	`sha256:0882295c03fe1a298bbf8fb2d58765305b0a41aa33ff2486ac4244ccc19fee25`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 12.0 MB (11968392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1160a80a4f8dfc675a9ec6bc950a108524b349c7f53bd872ff584223bd6ffc01`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250223.0.312761`

```console
$ docker pull archlinux@sha256:cd39606466737d54e804fd5bad28c0fd195aba0042cd3c38c60aca14e281b895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250223.0.312761` - linux; amd64

```console
$ docker pull archlinux@sha256:85a806225854c084f6122ff453517e22f5d998094bef13b0ad74f4f983250865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280244252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b648ccfa3dd5007f0201036d2d5803938cac01d6b7ca66c4cbbbc45a5b04cc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:52c18e014de0f10e1675122d732c121993497f96975726b19208798ac5ec9328`  
		Last Modified: Mon, 24 Feb 2025 20:29:41 GMT  
		Size: 280.2 MB (280235177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb5e786de9d4a3fd6ce9778e8a34ae5c72b3e36c34d7a4f9b63a6228fd8b61`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250223.0.312761` - unknown; unknown

```console
$ docker pull archlinux@sha256:71f1cea6167ec0211286fd788ff0c81677d8bbb823ecedbda9e6fcdc10665cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11980146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c0650c190dd2e5181a313618f945c98df1f28b3eb86d80df6ead6591681d39`

```dockerfile
```

-	Layers:
	-	`sha256:0882295c03fe1a298bbf8fb2d58765305b0a41aa33ff2486ac4244ccc19fee25`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 12.0 MB (11968392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1160a80a4f8dfc675a9ec6bc950a108524b349c7f53bd872ff584223bd6ffc01`  
		Last Modified: Mon, 24 Feb 2025 20:29:37 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:0dd90d4fc8e6d991810f57222fa3a2d926b34e4aa3adb1117857c4685def16cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:a2ec6393d71cc4b5ec3b8749d6fb8ab46f3d7804542c778e58945425064a23a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158773606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0995e2d39d4e0e18432ae70b57f09667f40c6a73693dc9d294799696ab588e14`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:70c9c0bc740b2885ab94a3ed5f1f0f0d5c4e414d39b84d1a896a60ff68f74780`  
		Last Modified: Mon, 24 Feb 2025 20:29:08 GMT  
		Size: 158.8 MB (158765282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d295b16ff000d323d54017b773a25cf28118f4ff9d132c428336b58a9babe9d`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0fabb023c7544271b4bc385ab045839cdd95c469b6c8524c94c61df3875f1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8159967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651998445313026f641596942a94b3c3c28fe08a0f26b25cca5de3c7d39e0a07`

```dockerfile
```

-	Layers:
	-	`sha256:3f7f9721672652bba099e96c2ad82f525143eef1f3346b9592ebb454eea5cf05`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 8.1 MB (8147996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a40a8731b74907e6ec9938e258510eab4b3cf6fad27261516338d66a7d833b2`  
		Last Modified: Mon, 24 Feb 2025 20:29:06 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:d5e028f1638d310cc7a9fb11e1b0ea405d6b1c9c62c3757f7981ab08c4e91cc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6eb24c1061ccb1c6e41a737cf524aac5f47076531a3db7d98cb89c767009bb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330257679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769e3859181049fccd96195146a835445896cd4616647494d8779a888e0638e1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:30697cacdae779eb2353295674328b41e46159d06e3b92f3984b2d6e608e1b27`  
		Last Modified: Mon, 24 Feb 2025 20:29:50 GMT  
		Size: 330.2 MB (330247473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5d62fb6565a7832cac1862cefbc4b3649084e20aab1ec2125ae083d5e03b0`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:252c57a7807566d185df378c2e28a75ff506dec712d916698a4524451ce14676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12248718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217ab4d0e2bba7c6ef486029aa76cac1221cc5d46696915b0cde7efc659a4ce`

```dockerfile
```

-	Layers:
	-	`sha256:729ca1f9fbf7be78a15a301d453ac2f26e5095edefa498ea172effc0c29c92c6`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 12.2 MB (12236907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20bd475c5d21685ba45825c8cd2367a748391d8fb703bf93f66cc8a1df8fcbae`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250223.0.312761`

```console
$ docker pull archlinux@sha256:d5e028f1638d310cc7a9fb11e1b0ea405d6b1c9c62c3757f7981ab08c4e91cc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250223.0.312761` - linux; amd64

```console
$ docker pull archlinux@sha256:6eb24c1061ccb1c6e41a737cf524aac5f47076531a3db7d98cb89c767009bb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330257679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769e3859181049fccd96195146a835445896cd4616647494d8779a888e0638e1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.version=20250223.0.312761
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Feb 2025 00:07:38 GMT
LABEL org.opencontainers.image.created=2025-02-23T00:07:38+00:00
# Sun, 23 Feb 2025 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250223.0.312761' /etc/os-release # buildkit
# Sun, 23 Feb 2025 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 23 Feb 2025 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:30697cacdae779eb2353295674328b41e46159d06e3b92f3984b2d6e608e1b27`  
		Last Modified: Mon, 24 Feb 2025 20:29:50 GMT  
		Size: 330.2 MB (330247473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5d62fb6565a7832cac1862cefbc4b3649084e20aab1ec2125ae083d5e03b0`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250223.0.312761` - unknown; unknown

```console
$ docker pull archlinux@sha256:252c57a7807566d185df378c2e28a75ff506dec712d916698a4524451ce14676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12248718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0217ab4d0e2bba7c6ef486029aa76cac1221cc5d46696915b0cde7efc659a4ce`

```dockerfile
```

-	Layers:
	-	`sha256:729ca1f9fbf7be78a15a301d453ac2f26e5095edefa498ea172effc0c29c92c6`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 12.2 MB (12236907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20bd475c5d21685ba45825c8cd2367a748391d8fb703bf93f66cc8a1df8fcbae`  
		Last Modified: Mon, 24 Feb 2025 20:29:46 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
