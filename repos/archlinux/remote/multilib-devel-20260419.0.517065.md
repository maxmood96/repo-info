## `archlinux:multilib-devel-20260419.0.517065`

```console
$ docker pull archlinux@sha256:eb1f8b3bd95dcbdbe602bdc85f2166247b7f096b5a646a19aed205bec6771067
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260419.0.517065` - linux; amd64

```console
$ docker pull archlinux@sha256:1aaeb9dff4f60613df76bf30d8899e77d796fa71ab79fcbe76271d565746410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269533467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e355236ea60c3b4ffbbde824611b15a534d57ca69613e7ef05351e5bae5d1a01`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:47:12 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:47:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:47:18 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:47:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:47:18 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c678628832858cc081c20f7661be106a02b6b75e928d4cdc26418f0a7020ced3`  
		Last Modified: Mon, 20 Apr 2026 21:48:06 GMT  
		Size: 269.5 MB (269523086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168718046a8b227ef0c6c2c79f994f80fdcd4efb19bcaa602417e5eeb3610b02`  
		Last Modified: Mon, 20 Apr 2026 21:47:58 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260419.0.517065` - unknown; unknown

```console
$ docker pull archlinux@sha256:e4d2ff284589e4ab1fbbdd9a94de5399b7cd545992b148487995260a5a2ab370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12263806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacb4af6d2fabc230b60eb47dc75a9d119d7ac716b44d900578710af4bb66e41`

```dockerfile
```

-	Layers:
	-	`sha256:bb539de3ec61ed6a39ed5e15cc2c075d24d0006ff38b5762cd5faf0e758a4c62`  
		Last Modified: Mon, 20 Apr 2026 21:47:59 GMT  
		Size: 12.3 MB (12252038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc867a394bf03492bad170a5fc445180ab3e6abd12fbe3513599527d0aa1d06`  
		Last Modified: Mon, 20 Apr 2026 21:47:58 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
