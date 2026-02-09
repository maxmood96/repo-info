## `archlinux:multilib-devel-20260208.0.488728`

```console
$ docker pull archlinux@sha256:223963305dfbb4a1a5ac46a12e87966526df053abe87dc4662eb1d512feaa435
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260208.0.488728` - linux; amd64

```console
$ docker pull archlinux@sha256:c2f8ab73bfeb71ca21edfd2613e96aeb4166835e5cc4139c12fafd0823f57b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345524666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af8b22150e3f0d3732212ec0bdbe6e6cbd19468550ccf784b2f152e7e33958`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:37:32 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:37:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:37:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:37:40 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:37:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c87d276e83970850f8d41f0d5f9e2c96eb05df99ef0478d864e9e9b5a76ebd6c`  
		Last Modified: Mon, 09 Feb 2026 19:38:36 GMT  
		Size: 345.5 MB (345514244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571e13d7871681f45bbfef9522d1b4a8087420f777d1acb94f695bd1a01c2d2`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260208.0.488728` - unknown; unknown

```console
$ docker pull archlinux@sha256:aa971e7830192713f2819c672811cf73af8d9c0c76588ad3e86416c6e52ad302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12448457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c2e8a2bccce9cff0ecc1eeb863efd61d0c3b9e48c4a5889c458f23808c62cf`

```dockerfile
```

-	Layers:
	-	`sha256:fd0824790dbe8b02f896b98a6856502b7fa68f80694ffb58f28028124295f04e`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 12.4 MB (12436689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dfae207c8826eea78a0f6b07abfe3513d13120fd5239d616449287a7a417936`  
		Last Modified: Mon, 09 Feb 2026 19:38:29 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
