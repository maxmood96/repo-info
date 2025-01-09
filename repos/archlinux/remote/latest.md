## `archlinux:latest`

```console
$ docker pull archlinux@sha256:292bb4ec7866af67f8d66fe2114eef840eebc74302db00b891dcb2d278bec80a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:da131d0947336cbabc971ee7e400d94f2a2f4c32e6bc759e2a0b0f09fe2245cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153107935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf34a96768a3e964a69639d9573d0e50984783a1bd1d005745e9b5efbe0993d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:734567a21ac630b02c05a26a3b8bdedcba14ff5644a33b2bb998c65564bf7647`  
		Last Modified: Tue, 07 Jan 2025 01:29:16 GMT  
		Size: 153.1 MB (153099589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720411fb211aad740ff49e678394c60d7fb50bb25e8facf43fcaa4b69c0841e`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:1d20104a9198b4c02c8e513610d2454cd5dff48415eb7307c0f0239955b1dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f480a73f486501c3b42fdddb3b95874342168690ba88abe7802bec934095c63b`

```dockerfile
```

-	Layers:
	-	`sha256:0cc3395c8528c58062d37eb37fa11ad9176baf5d9d6f812631d1ab95bb8e48a1`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 8.1 MB (8088854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d459c75d9f78faab6db5c1038683dc414844909ce309f42e39d9fd777d4298c`  
		Last Modified: Wed, 08 Jan 2025 17:58:13 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
