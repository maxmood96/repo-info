## `archlinux:multilib-devel-20240908.0.261281`

```console
$ docker pull archlinux@sha256:34476c1e210f7c0de33d33569fa636da564751c79fb0d6cf59374e84aebed268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240908.0.261281` - linux; amd64

```console
$ docker pull archlinux@sha256:8c7f0e4ed679bbc66e3b5b78dc876a65a02ca319702d022164a4e22dcdc063da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322164261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad11b0d9aec60b3ff4eeeafdf71d06f31260b896a1d5c1ff11f913ba8e6b461`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.version=20240908.0.261281
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.created=2024-09-08T00:07:27+00:00
# Sun, 08 Sep 2024 00:07:27 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240908.0.261281' /etc/os-release # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 00:07:27 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53ae51d027274ad9e04c1b0f683a81d643a09ad9b3892ccade4d40f11ed81097`  
		Last Modified: Mon, 09 Sep 2024 19:05:05 GMT  
		Size: 322.2 MB (322154051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae698b60132ac648a39a026af430e8c78450761b5087a57cedfaebffeaa9673`  
		Last Modified: Mon, 09 Sep 2024 19:05:00 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240908.0.261281` - unknown; unknown

```console
$ docker pull archlinux@sha256:250f99d3f1bbc14786d024914ed1afe9f0ffe1ff5aa396f1b3389366817cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12181257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1574ef952546a8886fd2a699d768e2c7303577a4312fedd672a997153e2a38`

```dockerfile
```

-	Layers:
	-	`sha256:b8f31e5d5209e48f38c957405a5b2fe7abd312372d22fed2950fa41fec45938f`  
		Last Modified: Mon, 09 Sep 2024 19:05:00 GMT  
		Size: 12.2 MB (12169697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2bdb9a743029eb08939a6c7c64af51e8cc9b0f85425604208bc4185ab08594b`  
		Last Modified: Mon, 09 Sep 2024 19:05:00 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
