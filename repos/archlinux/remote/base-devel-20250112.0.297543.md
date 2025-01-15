## `archlinux:base-devel-20250112.0.297543`

```console
$ docker pull archlinux@sha256:5bffbf54bf180c86fbe2ade792cd2d3e957df50fa45da63cb8995564aa90ff9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250112.0.297543` - linux; amd64

```console
$ docker pull archlinux@sha256:bfdcc60a7bff6bd7f45b02b9fa64d7962c050d5e223b1df1052b05389bbaf7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274245183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a83b1826554594b9cbc44667fb9065d7e895ccb4d5c871c4d17fe44f53137`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250112.0.297543
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-01-12T00:07:47+00:00
# Sun, 12 Jan 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250112.0.297543' /etc/os-release # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 12 Jan 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:19a599bcbe68b61c0f6ac716193c401951e23f55a309045c997dba16a3374820`  
		Last Modified: Mon, 13 Jan 2025 19:29:14 GMT  
		Size: 274.2 MB (274236106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e2925da3e00761896ebcd51442a961926b6578f306e242b3ec6e43d776b39b`  
		Last Modified: Tue, 14 Jan 2025 20:38:36 GMT  
		Size: 9.1 KB (9077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250112.0.297543` - unknown; unknown

```console
$ docker pull archlinux@sha256:1faa61dc7071bc3420230183ac805815f7a8ebae57d33c356f09fb68e9b1e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e49912cfbaad5f8ad029aca7edd8708a25abf9cc08411c1d26e7d27092f340`

```dockerfile
```

-	Layers:
	-	`sha256:c8405add251a7d5a7598e1a190f49786176e17c2ec8e8de3aca813f82c75c6bf`  
		Last Modified: Mon, 13 Jan 2025 19:29:10 GMT  
		Size: 11.9 MB (11895722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a2e25c40caf508460a713b94556306d42d5b7a4e927fbf64d985fb7c3cb10a`  
		Last Modified: Mon, 13 Jan 2025 19:29:10 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
