## `archlinux:multilib-devel-20260329.0.507017`

```console
$ docker pull archlinux@sha256:d229b760db22a5348a778b6dc42749c160a9426990e413fd06484190c62f9a80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260329.0.507017` - linux; amd64

```console
$ docker pull archlinux@sha256:d9ed19bf543b46660be4cff8a23d54630fb5364ced64d1280c09eb9b05c5e9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268537672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8519ab0f23f7b3d466900bf4ffe097133f554841c91109dc57b66da0ddd395a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.version=20260329.0.507017
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.created=2026-03-29T00:10:46+00:00
# Mon, 30 Mar 2026 17:34:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 30 Mar 2026 17:34:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260329.0.507017' /etc/os-release # buildkit
# Mon, 30 Mar 2026 17:34:36 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:34:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a62fe7f33cbacca24085d9fba3b0371e6b6882ffb175eb3502dfa667f0865470`  
		Last Modified: Mon, 30 Mar 2026 17:35:28 GMT  
		Size: 268.5 MB (268527366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e6257934d9bebcd34e3ec6d04ea47b265b0d56e4172c1a49860b032064dc39`  
		Last Modified: Mon, 30 Mar 2026 17:35:22 GMT  
		Size: 10.3 KB (10306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260329.0.507017` - unknown; unknown

```console
$ docker pull archlinux@sha256:fdfb90122b0fc5c31dfd5871611d56a7f7dc3df54604a6f84a010ec5c56e4685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12213885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14fed52ee64392889cb4754c99c201948df326c85e307ace9460c661fbd2166`

```dockerfile
```

-	Layers:
	-	`sha256:041dcfa146c290350c97f715917c794b2671bc7eb52e02b14b5fd14b66a26e68`  
		Last Modified: Mon, 30 Mar 2026 17:35:23 GMT  
		Size: 12.2 MB (12202117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2489eaf24b91abbfffb910e9b3930bd47efb2990e48286979fcc5b62d721ae`  
		Last Modified: Mon, 30 Mar 2026 17:35:22 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
