<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250907.0.417472`](#archlinuxbase-202509070417472)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250907.0.417472`](#archlinuxbase-devel-202509070417472)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250907.0.417472`](#archlinuxmultilib-devel-202509070417472)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:fc6a7997e569e600cac7b69ccc322515b72fddbdb388e978faa3c0f12bd13dae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0710015542f7006b2b3438fe8a169a39b00d3d53ea11d0cab83a2f1b22c3da28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164286474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bc50773cdec3219ae5b97176ed9e9859df22cfef90b30046e2fb0201678f5b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:865fe9d98847c3e4f27e91efa00448b37a5c098def3a8311214a15ba321af560`  
		Last Modified: Mon, 08 Sep 2025 19:31:33 GMT  
		Size: 164.3 MB (164278139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61a1d3796c9d0cd3df769300606bc8b78dda703ccd5d86f2e8c00a81dc2fa70`  
		Last Modified: Mon, 08 Sep 2025 17:16:13 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:773713e0eaaea5313e16dbde71b93a8c524a375e9513afa84d70628ac5be5422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed7031a8b72702fd4481bcef589b31caf2125bb7d272975e9e331de85c6a21b`

```dockerfile
```

-	Layers:
	-	`sha256:7484c5e353623068c7ae2641424dc2b973cf6c357688e0deef8aaf8821186f6d`  
		Last Modified: Mon, 08 Sep 2025 19:48:18 GMT  
		Size: 8.2 MB (8181515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922f19aec4d51a158204c97f7f38b6d2969af31c375cdba0b3b9f0d4700ab441`  
		Last Modified: Mon, 08 Sep 2025 19:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250907.0.417472`

```console
$ docker pull archlinux@sha256:fc6a7997e569e600cac7b69ccc322515b72fddbdb388e978faa3c0f12bd13dae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250907.0.417472` - linux; amd64

```console
$ docker pull archlinux@sha256:0710015542f7006b2b3438fe8a169a39b00d3d53ea11d0cab83a2f1b22c3da28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164286474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bc50773cdec3219ae5b97176ed9e9859df22cfef90b30046e2fb0201678f5b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:865fe9d98847c3e4f27e91efa00448b37a5c098def3a8311214a15ba321af560`  
		Last Modified: Mon, 08 Sep 2025 19:31:33 GMT  
		Size: 164.3 MB (164278139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61a1d3796c9d0cd3df769300606bc8b78dda703ccd5d86f2e8c00a81dc2fa70`  
		Last Modified: Mon, 08 Sep 2025 17:16:13 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250907.0.417472` - unknown; unknown

```console
$ docker pull archlinux@sha256:773713e0eaaea5313e16dbde71b93a8c524a375e9513afa84d70628ac5be5422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed7031a8b72702fd4481bcef589b31caf2125bb7d272975e9e331de85c6a21b`

```dockerfile
```

-	Layers:
	-	`sha256:7484c5e353623068c7ae2641424dc2b973cf6c357688e0deef8aaf8821186f6d`  
		Last Modified: Mon, 08 Sep 2025 19:48:18 GMT  
		Size: 8.2 MB (8181515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922f19aec4d51a158204c97f7f38b6d2969af31c375cdba0b3b9f0d4700ab441`  
		Last Modified: Mon, 08 Sep 2025 19:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:52caef7ac18d69010f97ebb0b0d23cbb02e0b9bfc5715f044508b3552beaa419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7dd35e9ca75b183042a9f22b8106b19d9511a5b610039072546ba6c5c3a81af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289366809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87221098b9c69429253a9100b1c3f3aa2e8967c9e2968512dccc9861c26ff697`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ac0c9d6e9598df47eb858042b1f9b6e70be0ac5bb78c53e2dd86c0e3a7ad926c`  
		Last Modified: Mon, 08 Sep 2025 19:49:56 GMT  
		Size: 289.4 MB (289357647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa474f8ed776670f9356c8bafbabcc3de7a582a1184f2b08dd6a8f695cefffe`  
		Last Modified: Mon, 08 Sep 2025 17:16:28 GMT  
		Size: 9.2 KB (9162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:23fd162a0710e105899d86115d9408eac294799a94247f2886a3dbf30591a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12094679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4627380783c74775050cd4c7173492d7d4c0fc2a4f2469804185595e497348`

```dockerfile
```

-	Layers:
	-	`sha256:62ad2a8ad3aa16dd6a6c452b96982b184bbe1b16e888c18ea0d6e33644945fe4`  
		Last Modified: Mon, 08 Sep 2025 19:48:29 GMT  
		Size: 12.1 MB (12082925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63f333a0f76bc63fbc19f6663bd01ea8fac4c8bad0669e40ccd8463b35399f7`  
		Last Modified: Mon, 08 Sep 2025 19:48:30 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250907.0.417472`

```console
$ docker pull archlinux@sha256:52caef7ac18d69010f97ebb0b0d23cbb02e0b9bfc5715f044508b3552beaa419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250907.0.417472` - linux; amd64

```console
$ docker pull archlinux@sha256:7dd35e9ca75b183042a9f22b8106b19d9511a5b610039072546ba6c5c3a81af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289366809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87221098b9c69429253a9100b1c3f3aa2e8967c9e2968512dccc9861c26ff697`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ac0c9d6e9598df47eb858042b1f9b6e70be0ac5bb78c53e2dd86c0e3a7ad926c`  
		Last Modified: Mon, 08 Sep 2025 19:49:56 GMT  
		Size: 289.4 MB (289357647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa474f8ed776670f9356c8bafbabcc3de7a582a1184f2b08dd6a8f695cefffe`  
		Last Modified: Mon, 08 Sep 2025 17:16:28 GMT  
		Size: 9.2 KB (9162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250907.0.417472` - unknown; unknown

```console
$ docker pull archlinux@sha256:23fd162a0710e105899d86115d9408eac294799a94247f2886a3dbf30591a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12094679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4627380783c74775050cd4c7173492d7d4c0fc2a4f2469804185595e497348`

```dockerfile
```

-	Layers:
	-	`sha256:62ad2a8ad3aa16dd6a6c452b96982b184bbe1b16e888c18ea0d6e33644945fe4`  
		Last Modified: Mon, 08 Sep 2025 19:48:29 GMT  
		Size: 12.1 MB (12082925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63f333a0f76bc63fbc19f6663bd01ea8fac4c8bad0669e40ccd8463b35399f7`  
		Last Modified: Mon, 08 Sep 2025 19:48:30 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:fc6a7997e569e600cac7b69ccc322515b72fddbdb388e978faa3c0f12bd13dae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0710015542f7006b2b3438fe8a169a39b00d3d53ea11d0cab83a2f1b22c3da28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164286474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bc50773cdec3219ae5b97176ed9e9859df22cfef90b30046e2fb0201678f5b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:865fe9d98847c3e4f27e91efa00448b37a5c098def3a8311214a15ba321af560`  
		Last Modified: Mon, 08 Sep 2025 19:31:33 GMT  
		Size: 164.3 MB (164278139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61a1d3796c9d0cd3df769300606bc8b78dda703ccd5d86f2e8c00a81dc2fa70`  
		Last Modified: Mon, 08 Sep 2025 17:16:13 GMT  
		Size: 8.3 KB (8335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:773713e0eaaea5313e16dbde71b93a8c524a375e9513afa84d70628ac5be5422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed7031a8b72702fd4481bcef589b31caf2125bb7d272975e9e331de85c6a21b`

```dockerfile
```

-	Layers:
	-	`sha256:7484c5e353623068c7ae2641424dc2b973cf6c357688e0deef8aaf8821186f6d`  
		Last Modified: Mon, 08 Sep 2025 19:48:18 GMT  
		Size: 8.2 MB (8181515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922f19aec4d51a158204c97f7f38b6d2969af31c375cdba0b3b9f0d4700ab441`  
		Last Modified: Mon, 08 Sep 2025 19:48:19 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:0cd3f227a24ba5110d93ddd83a45f8634edaea544dc497474a22953346c80357
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c8dc88a3af806c0a7a108a22623f78e0da02430451d6fa4835091e8c622a1eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340679545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63c8652702a57d1f5c496f1b41a6e33a0f11a572dc038f44133336b88e3d630`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7abf3d7da9943cb2159eaebfb57c876d373acb19f559c2f4b7f37e05ca632aa`  
		Last Modified: Mon, 08 Sep 2025 20:15:47 GMT  
		Size: 340.7 MB (340669290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a478f69a8846193264085a9c6342534acee5a921a258862cc5a42af8cb2a1a`  
		Last Modified: Mon, 08 Sep 2025 17:23:20 GMT  
		Size: 10.3 KB (10255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a180945ad55c76d33fcbf7c45dc698e91d076c09f0b75045d01fbbcaa229d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12363630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cff58e2624aad65f050ab06dbc13b218ab028b7662202d8e5cdb8dfbfa3d85d`

```dockerfile
```

-	Layers:
	-	`sha256:a6594782c8cd07a748c297b67c55038b9373ebbcee1b4e2d09958dec0a2cb081`  
		Last Modified: Mon, 08 Sep 2025 19:48:33 GMT  
		Size: 12.4 MB (12351819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6007a7a1382493e7433eefb0cc17838d0027b52bf6b47a519ae37b626d4095fe`  
		Last Modified: Mon, 08 Sep 2025 19:48:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250907.0.417472`

```console
$ docker pull archlinux@sha256:0cd3f227a24ba5110d93ddd83a45f8634edaea544dc497474a22953346c80357
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250907.0.417472` - linux; amd64

```console
$ docker pull archlinux@sha256:c8dc88a3af806c0a7a108a22623f78e0da02430451d6fa4835091e8c622a1eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340679545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63c8652702a57d1f5c496f1b41a6e33a0f11a572dc038f44133336b88e3d630`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7abf3d7da9943cb2159eaebfb57c876d373acb19f559c2f4b7f37e05ca632aa`  
		Last Modified: Mon, 08 Sep 2025 20:15:47 GMT  
		Size: 340.7 MB (340669290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a478f69a8846193264085a9c6342534acee5a921a258862cc5a42af8cb2a1a`  
		Last Modified: Mon, 08 Sep 2025 17:23:20 GMT  
		Size: 10.3 KB (10255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250907.0.417472` - unknown; unknown

```console
$ docker pull archlinux@sha256:a180945ad55c76d33fcbf7c45dc698e91d076c09f0b75045d01fbbcaa229d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12363630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cff58e2624aad65f050ab06dbc13b218ab028b7662202d8e5cdb8dfbfa3d85d`

```dockerfile
```

-	Layers:
	-	`sha256:a6594782c8cd07a748c297b67c55038b9373ebbcee1b4e2d09958dec0a2cb081`  
		Last Modified: Mon, 08 Sep 2025 19:48:33 GMT  
		Size: 12.4 MB (12351819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6007a7a1382493e7433eefb0cc17838d0027b52bf6b47a519ae37b626d4095fe`  
		Last Modified: Mon, 08 Sep 2025 19:48:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
