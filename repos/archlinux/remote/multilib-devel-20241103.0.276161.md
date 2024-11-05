## `archlinux:multilib-devel-20241103.0.276161`

```console
$ docker pull archlinux@sha256:b9eb0459c6e380b3c92e155654e06d7c3107a9691ac7d091275861d1994fae51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241103.0.276161` - linux; amd64

```console
$ docker pull archlinux@sha256:a0f12e0add3c48afc4be7a4ccb87a19252bdb721fe2efc8f44ba606671ae8783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322266339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559d9693277569132d87b31d9a5b2314bf13f2e14fbbd530dac227b9a0838af7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ee64a7811103c061f3a30fb81cfeffb7ffd494c90867c065f6ad59738ad625b1`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 322.3 MB (322256125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72519b37c903eecf6bd5206c532180689bd474c9224cb998d54b4be00d4d7bf1`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 10.2 KB (10214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241103.0.276161` - unknown; unknown

```console
$ docker pull archlinux@sha256:96b7999c362e61e95a67ad9700de818d9e2b994c64566a39791153596b945921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12238170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7558523368ec36f23e46ccf711607b066c90a75b86ff5746e08e65c1c564c24`

```dockerfile
```

-	Layers:
	-	`sha256:a9320fcab8f22f17c5c4bb31bac425c7e82962e65efb135e6b8aa1890f3a2ff8`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 12.2 MB (12226576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc6b53b3d837c4b83fa6994ebc59bcb678bf26eebfc7e080e4d0c530d9ffb79`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json
