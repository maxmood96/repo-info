## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b212ba57dea42f74f3197e5926ec6b9dece07bbc17147afb91db874549b5fd11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:499525353b9944a10f65f1266d08c93fd18bc1dc957d993a93a4a24e174f2c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271745957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdd7b7c6cf0339af07a9d0e072cc511d722117513ec2fb3d010bd46e024ad8b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.version=20240818.0.255804
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.created=2024-08-18T00:07:58+00:00
# Sun, 18 Aug 2024 00:07:58 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240818.0.255804' /etc/os-release # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 18 Aug 2024 00:07:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:24b1c3c45b6ca33f24c75d7f2e4306cd305f51c8872d4f9047898a8c60b6a0b3`  
		Last Modified: Mon, 19 Aug 2024 17:58:28 GMT  
		Size: 271.7 MB (271736915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed4f37407001e5dc344a5c6dd67a4dfec15d9692c6675b174b36fa8cbe85afa`  
		Last Modified: Mon, 19 Aug 2024 17:58:20 GMT  
		Size: 9.0 KB (9042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9608e74653b13d26c01aa68dd4cc93aa97d41b2e88aacd7c135cbb3d2c6fb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e711d12dec1851e0b37d58b1726bc94c8731ae533b7671ee4d96133dad7ba8`

```dockerfile
```

-	Layers:
	-	`sha256:b628a25d8c672a0297a0cc33637ba042d9379aedf6237272923f767085434ecb`  
		Last Modified: Mon, 19 Aug 2024 17:58:21 GMT  
		Size: 11.8 MB (11818150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4e66114aedecd35b14ceec19f0277ff10b61c3eccdcb51373ad3c3ec9f2332`  
		Last Modified: Mon, 19 Aug 2024 17:58:20 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
