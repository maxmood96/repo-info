## `archlinux:base`

```console
$ docker pull archlinux@sha256:7ca06cad29fe509ea1b4a0fb40485ca410fe5fdbea39888c5f3169b4961b2b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9c1cd902a49c2fa899622c286cba954f82b95b00abc1d9e094103eed3600594a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163274141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac8e88fb26b28530e3448585327a70fe5d414f5af5f91c60a455dfd1042338`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.version=20250706.0.377547
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 06 Jul 2025 00:07:04 GMT
LABEL org.opencontainers.image.created=2025-07-06T00:07:03+00:00
# Sun, 06 Jul 2025 00:07:04 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250706.0.377547' /etc/os-release # buildkit
# Sun, 06 Jul 2025 00:07:04 GMT
ENV LANG=C.UTF-8
# Sun, 06 Jul 2025 00:07:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e4655ef3515a3583f60522ea0db589115ae05d3ea8243775d40be9fd671a514a`  
		Last Modified: Mon, 07 Jul 2025 22:48:31 GMT  
		Size: 163.3 MB (163265783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7df37c7b4083f7f8c7c1ed77b16aa0f7e02318ac65fa5a6ce1a136eed4439`  
		Last Modified: Mon, 07 Jul 2025 20:42:00 GMT  
		Size: 8.4 KB (8358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d69d7dd59bb59dde508dbe82ea394fbbf613088f55858ffaff6298f6e91f2082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b49d45c13961b8773e2e5bfe4aae70fc3770bd0bbe0272f243bc7f5e76fb5c`

```dockerfile
```

-	Layers:
	-	`sha256:75d8da399c93b2b984d9accb99f333d21162055db8115ba89f6917f944cfa353`  
		Last Modified: Mon, 07 Jul 2025 22:48:16 GMT  
		Size: 8.2 MB (8150035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e19c8ae070fa0a130cefd4738882cf0db6f79c15295390cf28a57688da1f28`  
		Last Modified: Mon, 07 Jul 2025 22:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
