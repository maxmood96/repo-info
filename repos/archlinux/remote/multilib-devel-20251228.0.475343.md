## `archlinux:multilib-devel-20251228.0.475343`

```console
$ docker pull archlinux@sha256:604fccf6283d42ea730a9d529ca0fae86ac3e45e46cf174a2fd9b7106c74ba66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251228.0.475343` - linux; amd64

```console
$ docker pull archlinux@sha256:97b57d96e956c96abc53c08ce4fd79bbdac22c559c6c9d56057f00cce49bb9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343557638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777c0ca8979ac84d7c4e6a2840cb08c885090f0164971d71fd328c8a9fe807b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.version=20251228.0.475343
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Sun, 28 Dec 2025 06:06:28 GMT
LABEL org.opencontainers.image.created=2025-12-28T00:07:28+00:00
# Sun, 28 Dec 2025 06:06:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Dec 2025 06:06:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251228.0.475343' /etc/os-release # buildkit
# Sun, 28 Dec 2025 06:06:35 GMT
ENV LANG=C.UTF-8
# Sun, 28 Dec 2025 06:06:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6a0bb30a4ccec874efca15569e0fff6d09a9e1af5958081f4d046eaea43d7141`  
		Last Modified: Sun, 28 Dec 2025 06:07:58 GMT  
		Size: 343.5 MB (343547334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c8a8d2b418cba295d04ef814183f4188be9bbbed25d599f9078c2f206cc58`  
		Last Modified: Sun, 28 Dec 2025 06:07:36 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251228.0.475343` - unknown; unknown

```console
$ docker pull archlinux@sha256:a484d17b7fff752e73a82ef84f4abbede35b29fd0f5baa6fd764dafd8630fa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1590c89d0bbfcca9a3e920d247621b5dcc217175f73fc0d574b0f9a8ccdb4446`

```dockerfile
```

-	Layers:
	-	`sha256:1aa9efdcaf1769a73d19dba0780948aef1b4687b23076f870b4db120936dd066`  
		Last Modified: Sun, 28 Dec 2025 08:48:29 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b471fde77527b03de17b6541da89d06397a33c20a19f90da2d77fc995c58ff`  
		Last Modified: Sun, 28 Dec 2025 08:48:30 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
