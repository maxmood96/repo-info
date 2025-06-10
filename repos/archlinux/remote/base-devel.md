## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:5b87f50b25ce0ea047a13cdcd0043b22f61f6b341e3264b49d8ec98eb4308d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d78e0b8556659db64a766f6e9aa982ca986cc9b8743300881246bee817eebf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287762151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc51fd8af02ccbe9cd40162f8ce07ec7ebcffd9477cfb3e21bd059a87e99556`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.version=20250608.0.361578
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 08 Jun 2025 00:07:57 GMT
LABEL org.opencontainers.image.created=2025-06-08T00:07:57+00:00
# Sun, 08 Jun 2025 00:07:57 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250608.0.361578' /etc/os-release # buildkit
# Sun, 08 Jun 2025 00:07:57 GMT
ENV LANG=C.UTF-8
# Sun, 08 Jun 2025 00:07:57 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edaf86bcae51e42a88f99a1abbffc4007b15f9c39b3a85d74af977ca02a7db1f`  
		Last Modified: Mon, 09 Jun 2025 22:48:35 GMT  
		Size: 287.8 MB (287752988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4f01c4f25e43fce7667d7058c041b5836282f45efb05cafc8a23f74453ff03`  
		Last Modified: Mon, 09 Jun 2025 19:10:29 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:097185de7b7e16ca563118b2a1bf0b70667d127d993489dd034b00d53b8306e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12018152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3aaaaa0c653f320196018de497c7cb88d94c270af5032163b4ee6222a4089d`

```dockerfile
```

-	Layers:
	-	`sha256:a7fdab34f709e2fc5baeaae173e94d12e23fa490a9f4e8d9f198a35214b29ac5`  
		Last Modified: Mon, 09 Jun 2025 22:48:23 GMT  
		Size: 12.0 MB (12006399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e983e8d72cf1cb479b9a164d1cea8b70187ea71d2503d768cea6d3000faa2f`  
		Last Modified: Mon, 09 Jun 2025 22:48:24 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json
