## `archlinux:base-devel-20240825.0.257728`

```console
$ docker pull archlinux@sha256:2545b996b2de70ecc0293b8a607a31a2891396c182abb04af16e7d50ce9aee86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240825.0.257728` - linux; amd64

```console
$ docker pull archlinux@sha256:7488d90124dc3da3a43d2e941e599b974231967e2eab3eb697073a2e3448c97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271737203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc794c1bb8ce2a774f5b9bf9b041a1989ec39db83f65f5d84f676cfe9addb482`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:298dc0d2952244fad2540d1cd7765c9b3beb1fae3ae90fe74a9d3339125caf9b`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 271.7 MB (271728156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f3cf16aeba7031d385266919b9a059ee62a2ccfcd28b31da49d224b4781b2c`  
		Last Modified: Fri, 06 Sep 2024 23:15:55 GMT  
		Size: 9.0 KB (9047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240825.0.257728` - unknown; unknown

```console
$ docker pull archlinux@sha256:5869b63583420d83894585cd1eae07f9dc1a206039e25abe5a837bcf8b03be37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7123064c45280af89ccac6015287201622cde7cd89078b1471e975829fd4c03b`

```dockerfile
```

-	Layers:
	-	`sha256:aff2027bf5ca9aaecf2ac91cdf300953623057ec5061c504772d192b9108af02`  
		Last Modified: Fri, 06 Sep 2024 23:15:56 GMT  
		Size: 11.8 MB (11818188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b9ed633a0af93cdc69f8b0e03a37ea3553b200878151251e08abfa1d82800c`  
		Last Modified: Fri, 06 Sep 2024 23:15:55 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
