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
