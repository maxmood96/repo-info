## `archlinux:multilib-devel-20251221.0.472429`

```console
$ docker pull archlinux@sha256:bc257626b0dde4f463c1631ac8cf32990821f41ed1707ade1a5275c425e058e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251221.0.472429` - linux; amd64

```console
$ docker pull archlinux@sha256:2bf1eff21f22d04c419708e8c6e8fcbe9634e1802e839a80bf60020c540bd138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343559220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b01dbf52d45f4a8f2b53c6e83c820a4b03e614cdec51a1f773f6461924ff51a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:47:07 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:47:07 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:47:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:47:15 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:47:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b3468db2eccc780b7997ac3dd1dd6a1e534bccb26331620aa0e0774b8032bed0`  
		Last Modified: Tue, 23 Dec 2025 20:52:57 GMT  
		Size: 343.5 MB (343548899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95ee9581597d9db3df23bc3583ed8b361f3714d44bbe5b8be5f6e2e3ee1b1fa`  
		Last Modified: Tue, 23 Dec 2025 20:52:48 GMT  
		Size: 10.3 KB (10321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251221.0.472429` - unknown; unknown

```console
$ docker pull archlinux@sha256:437274e7fbc426dc350cd3f58365ac6d8c4d3692fd5cc1c633b36599f5d7888d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6793eafa2aafc1ac6fa224df3c13bf04ffb57bd0b537c16ab239a64fbacdffa`

```dockerfile
```

-	Layers:
	-	`sha256:c983f3955a785774649f8afe2305b45c35f25e7ab86766d64d4be759c80909d9`  
		Last Modified: Tue, 23 Dec 2025 20:48:30 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6905de94dcf9e4700c796bc7065d35b5d1f67259fbfb38c83655b1144e320be4`  
		Last Modified: Tue, 23 Dec 2025 20:48:31 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
