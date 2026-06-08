## `archlinux:base`

```console
$ docker pull archlinux@sha256:a1f78e6a19f19d0f6cd9bf35ec59de31fe0bdeff6a94e968be0276ca255f14cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:fb47d15e0fd28369c700edcfa46dd44e234d8ab6fee9627ee5f1ead5f1fc6c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131171103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18054cdf72229c2a48277565a6d80f3e2a7b91209010f8b0b50e43b97bd133f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.version=20260607.0.541780
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 08 Jun 2026 18:50:15 GMT
LABEL org.opencontainers.image.created=2026-06-07T00:09:31+00:00
# Mon, 08 Jun 2026 18:50:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jun 2026 18:50:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260607.0.541780' /etc/os-release # buildkit
# Mon, 08 Jun 2026 18:50:18 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jun 2026 18:50:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f84cafa04e5c2c4a470761f8140e0f2a20f298d0c1385f4e465a3ceded3ede79`  
		Last Modified: Mon, 08 Jun 2026 18:50:44 GMT  
		Size: 131.2 MB (131162431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba61d83f91dee65cd4786c6eee321d3b838b887ed4b36c5c50cbcda73d13605`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 8.7 KB (8672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:49bcbaa8d06bca06f4ba14af2d182758028dfce62c41410a23c1c6d25fed3791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1723c5e4cfe344f0486568cdadd2b48667a0b8fa5fb374ffcfee3a28892e26`

```dockerfile
```

-	Layers:
	-	`sha256:ba018fc32aa7762cf7829b138d39eebbc36af9547c240c4046fadbcb9cd275ff`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 8.2 MB (8182429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d2ee4f5ebb9c953b3045d16444d4873dfc971af37231b328cdf801391a47b`  
		Last Modified: Mon, 08 Jun 2026 18:50:41 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json
