## `archlinux:latest`

```console
$ docker pull archlinux@sha256:bf256af6457f18c60316bdab5a86dfa6b212f4f4d0098098429e363b4d5db0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c13557438a1df09698ff8af836a22d36e0436ac02a1475c87bd8fc913bf4884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157487905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db11dbb531b7976426052ea28befbe1286c8a3da35adbe238c28caf9a51e5e9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:983e51fa3b68b5be32c985411449c562ed0a4e1f8631f8baad0878c18df1aa63`  
		Last Modified: Mon, 03 Feb 2025 19:27:22 GMT  
		Size: 157.5 MB (157479617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4aaa455fa3c07708f646372e36175ac8826a50c00806f619ed2084912c97beb`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.3 KB (8288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:8bf846c4a8058e4869ef41af8f1dca2f6cd294204ea342d3e70346a30d3ef236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932f834ec3174f77586f20a7aec0118382fb02f49272fc49732adc5390858022`

```dockerfile
```

-	Layers:
	-	`sha256:aa1305d78119fe6f5c1b7e5d7a50bcfa578611712c5528a9a2fe8fc091c86270`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 8.1 MB (8088477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143c44261d7ea6dc4b78f3a28f36cc6bafc901eedd72653bec7d8caba4baa69`  
		Last Modified: Mon, 03 Feb 2025 19:27:20 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json
