## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:be024e3a05d303481657494b132e01c42e77a3107efb50721987ecd99607c39a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5568187995f280bc9b2921d93c6ad5bdc21f952954503f856545d70fd9be5b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278598527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e496c7d8a96d7b4722aa0915df9587b1c18c8f5b0c82b436deb74342618a38`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250126.0.301347
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-01-26T00:07:29+00:00
# Sun, 26 Jan 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250126.0.301347' /etc/os-release # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 26 Jan 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:66c3f9f4aca38a7dc9f922fd26e5b25a2fced66440d16b5e53dd7977f060ea8c`  
		Last Modified: Tue, 28 Jan 2025 01:29:11 GMT  
		Size: 278.6 MB (278589485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab05d2bad4390199982294dfcf060c3c4c342920d89dde4bf2c90cef5fa8ea6`  
		Last Modified: Tue, 28 Jan 2025 01:29:03 GMT  
		Size: 9.0 KB (9042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:831e1537f2ed05e7713702bd7cff82e82297211253cdaac9376d22f27f084200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6941f61c4c50cd650a3663c2abd9300ecc1af38cec724bcb4c54031a78fc9ed9`

```dockerfile
```

-	Layers:
	-	`sha256:abdc23c032398cada3a2dbf731b06c6ebf4602be6bd045cffa94ef66999f2bfc`  
		Last Modified: Tue, 28 Jan 2025 01:29:03 GMT  
		Size: 11.9 MB (11895966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7166ce82987a43701efe745e408d3ffba582f6c222f8f61afccb91e5a55308d0`  
		Last Modified: Tue, 28 Jan 2025 01:29:03 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
