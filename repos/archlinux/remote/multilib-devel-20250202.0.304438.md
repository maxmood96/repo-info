## `archlinux:multilib-devel-20250202.0.304438`

```console
$ docker pull archlinux@sha256:8354c1ea78242392e67387fb6b364d51eab0bdca51b989b516d1bbec70e91456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250202.0.304438` - linux; amd64

```console
$ docker pull archlinux@sha256:0d4df35c383a2e1e7c6b81c88327de5e487885a80d2eec5675519a31c2a5315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328460806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93c13b6197dd582433a8dc0023ad9977e18f3b5aeba8b235884838fa16bac88`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c1ff021d4b1d4d615e0bd2958452c80482e2d2e8f32790f3e1e3f6eb4161661e`  
		Last Modified: Mon, 03 Feb 2025 19:28:19 GMT  
		Size: 328.5 MB (328450566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775a06893295bab49f2edcf4f82a68924e3b8509f1238426974a29c9319f531b`  
		Last Modified: Mon, 03 Feb 2025 19:28:12 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250202.0.304438` - unknown; unknown

```console
$ docker pull archlinux@sha256:53879bb8197a47875c0ded6fdf648727bb3f5e08b1588b1d65d63bad7d1e2b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0129b605ab0bf1afa850a351f3fcecd67ccbb5dc4f982392fd858b06a770728`

```dockerfile
```

-	Layers:
	-	`sha256:b35a88c88b195ff883ef22ac9ceb94f3dcf917b3aa768999a4f00f7cc6ede0f3`  
		Last Modified: Mon, 03 Feb 2025 19:28:12 GMT  
		Size: 12.2 MB (12164476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec18124e57781805e7e82e2466ba295b7d913d4f1b4b5511fe9ef4701102e6ff`  
		Last Modified: Mon, 03 Feb 2025 19:28:11 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
