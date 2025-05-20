## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:3e0d60696c5547a50a2973ec087409a3712c17e2c4cd28c241efa29f70912884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3a13e725e9531e9b08a7f331b052ff266dd60d1c9ec1571544242858bf5a7519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338178797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2146ba73ddcf422fa9452e57c4ea9418427554ec25183a2d919ed34cc29397`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a21012c4ba1bc77de8e0135b54df240569dbf6ba848c9a05c8822b96015d4de8`  
		Last Modified: Mon, 19 May 2025 23:02:51 GMT  
		Size: 338.2 MB (338168487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2bbbc3a5c161afb5a25216d65ddbbaef0cc7b5e23ca7db4b74842eac0e1b72`  
		Last Modified: Mon, 19 May 2025 23:02:43 GMT  
		Size: 10.3 KB (10310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d7a37c0f32aa814e26f8e96d9d13e3e4f27db2499c6818d163556dfc1b4fda44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc28224d6ece19e3fc13da89edcd4a7b7445485ed32eb1ee4aa27f70c0556f6`

```dockerfile
```

-	Layers:
	-	`sha256:180cdd09d1b2721b993e70e5738471bcdf86e0e7439a6fe9f42c4fa94005de04`  
		Last Modified: Mon, 19 May 2025 23:02:44 GMT  
		Size: 12.3 MB (12298541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b2cf4b73a011536f69028e0a27896a6e4e8ff5b8c55b82935cd1150cbd8589`  
		Last Modified: Mon, 19 May 2025 23:02:43 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
