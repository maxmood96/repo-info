## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:485d4b471606e7e7e118b89f23ee59014338219861eb51e8682d9bc8c6212ad0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:78dac93b3899c3ca8da196f031c4269a2e922ff403cbb7033a77aa6d3b288bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321609342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c681f92f5bc3b27021717b33b0562ce6fab5ecbb9b2b28ebb7c0d5eee916b291`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20240728.0.249973
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-07-28T00:07:38+00:00
# Sun, 28 Jul 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240728.0.249973' /etc/os-release # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 28 Jul 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cfa234794e98e25410bbe10a20f100f1b0209775183d77be3028abd8feccc700`  
		Last Modified: Mon, 29 Jul 2024 18:57:16 GMT  
		Size: 321.6 MB (321599158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea515c7c1e758017809fc54cf4798e8eb2badf8a1a2744b10454735af3e29cf`  
		Last Modified: Mon, 29 Jul 2024 18:57:12 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f07c7ccd51b4553bd77877b81e46948143d6938d46b3822bc9b5adbb25c94ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0e88799e5886f93a81bc4716f727997ae0e4a6c3f482c4961b36bcfc921a89`

```dockerfile
```

-	Layers:
	-	`sha256:e8d9f04c64c88fa3ec9af0d39a76336bbccff9ed1a8bc51c8d7640161dd44934`  
		Last Modified: Mon, 29 Jul 2024 18:57:12 GMT  
		Size: 12.1 MB (12063678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50954966d24dc6f68cc45c527370572310767b83ae172eef67cae85348f9b54`  
		Last Modified: Mon, 29 Jul 2024 18:57:12 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json
