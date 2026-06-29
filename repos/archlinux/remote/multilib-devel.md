## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9bc32184564e58859eb926bb2e1bed6f0f015630d03efe3e2c5ac0f18ef068b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8701413ec07e507e1ada210786064a69d40bacf83446f0703054c4e883451701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327304532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c81fc202fa87a9fdde656d8614a075838c20a4155e38104147c89a2b920f3b2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.version=20260628.0.549485
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 29 Jun 2026 19:09:15 GMT
LABEL org.opencontainers.image.created=2026-06-28T00:09:46+00:00
# Mon, 29 Jun 2026 19:09:15 GMT
COPY /rootfs/ / # buildkit
# Mon, 29 Jun 2026 19:09:23 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260628.0.549485' /etc/os-release # buildkit
# Mon, 29 Jun 2026 19:09:23 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jun 2026 19:09:23 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1a1e4c1b130ce3d9c5fa0b371b195ba2d4f472e3198d2f0c91b8f5baf610e1dc`  
		Last Modified: Mon, 29 Jun 2026 19:10:23 GMT  
		Size: 327.3 MB (327291896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0316db9df4d6ef93a9f0bccfe375745144f4bc23913e475d1c826f058e9179d2`  
		Last Modified: Mon, 29 Jun 2026 19:10:17 GMT  
		Size: 12.6 KB (12636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0cf4386f3c403a8d29e0167e1f9722b95e1ef6901254f10266d2d91610a5f3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14684091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c163c8f212b070958b87cf3d913ab6a7fe178415bd105eb6d1869ffbe9d41e`

```dockerfile
```

-	Layers:
	-	`sha256:229910163543f007522df8de01b1d252db6f6093f53c8d790f42ef07a8112c76`  
		Last Modified: Mon, 29 Jun 2026 19:10:18 GMT  
		Size: 14.7 MB (14672323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab190e33c8fa87d2ad7c2d8e4a53db49d5e44882140fe51e150f377a5ce1b2a0`  
		Last Modified: Mon, 29 Jun 2026 19:10:17 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
