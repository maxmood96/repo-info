## `archlinux:multilib-devel-20241110.0.278197`

```console
$ docker pull archlinux@sha256:25f4d79c05832a338c8a05921364a93d1736e49eb6dbce9fb5d7a77b33730dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241110.0.278197` - linux; amd64

```console
$ docker pull archlinux@sha256:7bdccad0d730d937cf13c0da67b52e9ab65113fcd7f7f6bcf92547934ff61da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c1ba506b1d4ded9900724a22b6c45c9a2b3fc1730b414ad8465bfe25a81d4f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3ab97c08b12194b39487459a35c6eae1338779f256278f9827959dea61a640bd`  
		Last Modified: Mon, 11 Nov 2024 18:58:58 GMT  
		Size: 322.3 MB (322278597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dffb47154ea1ce0649d809746d4f3756a12af61fe14ab6064dd05a811eaccf`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241110.0.278197` - unknown; unknown

```console
$ docker pull archlinux@sha256:8e5cf1acd9ba98bf4960b9ba1ae87525c03ec97c316703a4ad73e35aa7f2ee0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e3f9da20e701b50e519a2525d8e34c28a1b249fb2a95edd813f38552e216a4`

```dockerfile
```

-	Layers:
	-	`sha256:cd86b9436854dc6687c33dee316859237c3e1d9a846a2eca2a9616eaaba253e4`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 12.2 MB (12164481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415bf24fdb2d6674ad2ca5785ae568c336d36ec9e303b16a1cd660be5102e334`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json
