## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:01bd0ee1c23c3dec1dcb0fce558150a222ee2ef0a3776404de33d0714bcefbb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3cf6781e229fc3f9e0b8740857d95b84e5580309285afc351c3a1b441a958c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247090944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125a2089ec4ace006ce7c1d29e9adf6c4e60b733bbc5f2693be553599c5af18`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:48:19 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:48:19 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:48:24 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:48:24 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:48:24 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5c1f30f5a8968675635fdbe2ce53d92208401558240cf52fcdaf22993ac0aaca`  
		Last Modified: Mon, 13 Apr 2026 17:49:09 GMT  
		Size: 247.1 MB (247081762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e94337e7f0c30454b4def77c429066ed4fad19ffca83181b7a4858d476d7ec`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:cb476b5d33482050fc27c94471173ba6e3d41f6b5ef0e172b69388c66e398807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11976487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85cb3cfb350c2454a21fe35cc3be4457372cad982fef9532da64b52ed9c6e07`

```dockerfile
```

-	Layers:
	-	`sha256:6e62e15360dc69f393c8ebe706c1934b098ae02631dfc76d7049a70b0a037081`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 12.0 MB (11964776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67fd359350dea2789a482ec3a1e4ac7066824f66716cfe0cee0bed232ed06d7`  
		Last Modified: Mon, 13 Apr 2026 17:49:03 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
