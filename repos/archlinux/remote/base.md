## `archlinux:base`

```console
$ docker pull archlinux@sha256:729afdc31856d0faf2c93c2291f3e81bccd5e75082f45e0f3513f65f83b88973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9d8002a9a805c88311039f050170eb14869df3b1edb525b72a03071f27769744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151134668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91721497913e579ac4e370dac68221b7800d88a9b3a7958f2ca27b17585f6b7a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240915.0.262934
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-15T00:07:28+00:00
# Sun, 15 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240915.0.262934' /etc/os-release # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 15 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:913facc7a97f31827a37ce293c99494796700c08c8eeeb0248dca1afae3f5c5c`  
		Last Modified: Mon, 16 Sep 2024 17:56:53 GMT  
		Size: 151.1 MB (151126440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9ac91550b6b2fb5cd51322f7c95fc35769726e272cdf1d09ea924b44e0bba`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 8.2 KB (8228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:f09cbd701b523029c6c1f03c2be671775da8d5c3a6a0cbb7d65d94397c4157fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8113930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daeddc386ac6f6acde612795ed4aca688b3d0eb4fc6c20748cd5fed3aa78eda`

```dockerfile
```

-	Layers:
	-	`sha256:a33233f144321ed1571b8be64f0563f4711ffafddc79af4aeb4c5688be78884c`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 8.1 MB (8102210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa1a7aedb81bb3177773eff83634a4d726ada1e96dec3379cfd00d07e14cd30`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 11.7 KB (11720 bytes)  
		MIME: application/vnd.in-toto+json
