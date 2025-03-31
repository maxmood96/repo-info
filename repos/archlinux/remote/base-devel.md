## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:11438acf52972a505eda9c9b588c1ee04f27186277aec15ef7f283ef6222c311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4d1b7a09932104456e96c77bb56c58616622f2503708d5a4d73e42a5850f1655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280831909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24c16ed9b3ebf03730a7f060c7cc0216fd1875ce3dec10621831f7f27a4393a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cb85c779ffeab5ed3bbaebb5b6d366ab27015ebf1161cba4c455902e74762905`  
		Last Modified: Mon, 31 Mar 2025 16:34:50 GMT  
		Size: 280.8 MB (280822858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361baea604e9e076887982734dd8196267555b7698a6d432c416b1a67cda5f20`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 9.1 KB (9051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4d4fbcbbdb2b6cacf0ac781b444d01d1d291c10422e704bd2e249c307e3bf727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11993871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed5f53b5f5e8ecd52564ff8581f1e6f8fe9ff50a2f9446fd15cf710b69da997`

```dockerfile
```

-	Layers:
	-	`sha256:8269457670b8542712582dde59edd256e5ee494e1a7d40dee68da80cb29bb00c`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 12.0 MB (11982117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4cd0ea4e5d469967ac6a07ba682820003b266837de94206a0f27024e9087a4`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
