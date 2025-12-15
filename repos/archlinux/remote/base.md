## `archlinux:base`

```console
$ docker pull archlinux@sha256:cbda7ef1fe6738d94dcae2bac2c6bc28978b2a41c24773f5cf73f58fa9986078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:42a51c3da6340ad79480f7db1fcc58fd77d4f38016f1155f4361954416ebcf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174525091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a51b69982e7d358e00530615c2f5b52948ff9242f2dc5cac06f4669e20c971`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:31:50 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:31:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:31:53 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:31:53 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f01404d5588892b3d97f4e80816575127ee71f0db9920a3765dc85e0df6538e3`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 174.5 MB (174516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c119f11fe6f01b611131f168c8e326d034460637feb832b8bc9bb8f73ec79b81`  
		Last Modified: Mon, 15 Dec 2025 18:32:42 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:576d378ca9e9738a8642a05ce7c94c83ecb0d12403637478e72105ea1a2803a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806ff195fe88dfd2d95b3c6bf2e4c4ff1014feea828fe72d6ae397c3511269c`

```dockerfile
```

-	Layers:
	-	`sha256:188106a5390cec650c09c7625e5fe3c6b614be676edb3fc733f0a91bcea34041`  
		Last Modified: Mon, 15 Dec 2025 20:48:16 GMT  
		Size: 8.4 MB (8368818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48ea3967ab3185e964cb5d8d68b3ae50c41bf41f0b4054b7456e3e0e4364ce8`  
		Last Modified: Mon, 15 Dec 2025 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
