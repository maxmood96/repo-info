## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:caeef94ae95a271932b12257e369f2972dbbe2f586c93a0c2b0b0845761cd13c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:951df25434f499b8347640c2783ae0947b23b437f5b51798bac11bc69d868185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279482279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd021c7fbac2f46df87e291d78f0acb63d220f9c187ecb79b59c52db87c3cc19`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.version=20250216.0.309127
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.created=2025-02-16T00:07:33+00:00
# Sun, 16 Feb 2025 00:07:33 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Feb 2025 00:07:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250216.0.309127' /etc/os-release # buildkit
# Sun, 16 Feb 2025 00:07:33 GMT
ENV LANG=C.UTF-8
# Sun, 16 Feb 2025 00:07:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:766bfb0508c63b1a37d31b5663ed698d69413b056fac69b8c517a8a1a2039709`  
		Last Modified: Tue, 18 Feb 2025 23:49:54 GMT  
		Size: 279.5 MB (279473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d0b238d6ed00934480fbc0c4cb7fa53092c5d360d83cde63772ab1fd82262`  
		Last Modified: Tue, 18 Feb 2025 20:33:00 GMT  
		Size: 9.1 KB (9063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8e9a510bbd22cf8bb36a4038f5a9a214f3629416618b037b5fb55f203b2092d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11968995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d81e6f30510ab63b8b3ae3f70a4991fc563eda381bcec0b74b9a55281e17ac`

```dockerfile
```

-	Layers:
	-	`sha256:56ce7785aa3730f3221de44cc2081dbff647b6830426393adc854546148a4464`  
		Last Modified: Tue, 18 Feb 2025 23:48:20 GMT  
		Size: 12.0 MB (11957241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f80386277b0a620c70773c1121ce215cebb17718a85de4e4f2a620c3ac1ac3af`  
		Last Modified: Tue, 18 Feb 2025 23:48:20 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
