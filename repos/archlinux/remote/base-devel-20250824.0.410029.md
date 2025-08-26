## `archlinux:base-devel-20250824.0.410029`

```console
$ docker pull archlinux@sha256:8ccc930c28ab4f483ff9bc1b53957150fbe94afe48928ebb0b14a8af41c75023
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250824.0.410029` - linux; amd64

```console
$ docker pull archlinux@sha256:656656b38529210a575736bfb5eabbd835ae321c4d5b14a07a489acef3deb844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289139093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71915b2f439c1152983c3eed417c5e410b3dab02d03dca20c3628e5ecc9c5c46`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:834bd6aa009ff890ad3d3c9d51ebf96eb0dd6cd845ae62d44a5d0ad64487911d`  
		Last Modified: Mon, 25 Aug 2025 22:49:24 GMT  
		Size: 289.1 MB (289129940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8bf13b8dc24ccd7f003e7e64dfe1f1b88f271ce3222752d03edcdcaef5c3e7`  
		Last Modified: Mon, 25 Aug 2025 19:53:52 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250824.0.410029` - unknown; unknown

```console
$ docker pull archlinux@sha256:5381edb1ae3c1245c7fcedb94add28020d99655ec1fd046a3eb0dc57c7e136d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b76856c616da7626772ef03651e53448068ea64f40e2b49d8caf67965482fcd`

```dockerfile
```

-	Layers:
	-	`sha256:93fba30b5d942b96456fe65b3c1ff4f73275d19078c2da9c89570712e14658b2`  
		Last Modified: Mon, 25 Aug 2025 22:48:21 GMT  
		Size: 12.1 MB (12063807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59f9f676d962f92bc2559ad360890573f8d5f58acef82033acb4d95c8c4b098`  
		Last Modified: Mon, 25 Aug 2025 22:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
