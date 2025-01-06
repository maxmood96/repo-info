<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241229.0.293060`](#archlinuxbase-202412290293060)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241229.0.293060`](#archlinuxbase-devel-202412290293060)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241229.0.293060`](#archlinuxmultilib-devel-202412290293060)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:efed7c2151d9875426ba77d4bec4c8126a4f422c834131dc4d179c20a1242a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:4bfad6b404e7e2ae4b8a36b048eb9d469e69445f5d2196e9ceec72468cca5d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152782285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c652e2bab60c298ad1aa7099354fd534a79c84e8179d36a45612d8f60887aec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9b7265eae795fc1044fb1a9ad407f315fd7f47f8171b3d6934ad0dd34e7c2882`  
		Last Modified: Thu, 02 Jan 2025 19:29:35 GMT  
		Size: 152.8 MB (152773979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c01223f5d96e3452caf453a754a8782a236f112179996e540b0c33e63b63f7`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:8bb0af37c95a3ba4a150df5169d2a3992fd4f8c57ed5381663bf07abfb54927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8089740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cb71c59b5771c19b16afdf036b39620fa029d0a1edb336b2378f504581bd76`

```dockerfile
```

-	Layers:
	-	`sha256:4759a3aef3624507e0c85dc69f41b813dfb35571ca16f268d3c4fa669b0d5ecf`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 8.1 MB (8077768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cab5c3f90a382ab3b36ac06fc112696065a6f351e529876f23fd7db25d1c31`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241229.0.293060`

```console
$ docker pull archlinux@sha256:efed7c2151d9875426ba77d4bec4c8126a4f422c834131dc4d179c20a1242a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241229.0.293060` - linux; amd64

```console
$ docker pull archlinux@sha256:4bfad6b404e7e2ae4b8a36b048eb9d469e69445f5d2196e9ceec72468cca5d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152782285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c652e2bab60c298ad1aa7099354fd534a79c84e8179d36a45612d8f60887aec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9b7265eae795fc1044fb1a9ad407f315fd7f47f8171b3d6934ad0dd34e7c2882`  
		Last Modified: Thu, 02 Jan 2025 19:29:35 GMT  
		Size: 152.8 MB (152773979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c01223f5d96e3452caf453a754a8782a236f112179996e540b0c33e63b63f7`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241229.0.293060` - unknown; unknown

```console
$ docker pull archlinux@sha256:8bb0af37c95a3ba4a150df5169d2a3992fd4f8c57ed5381663bf07abfb54927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8089740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cb71c59b5771c19b16afdf036b39620fa029d0a1edb336b2378f504581bd76`

```dockerfile
```

-	Layers:
	-	`sha256:4759a3aef3624507e0c85dc69f41b813dfb35571ca16f268d3c4fa669b0d5ecf`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 8.1 MB (8077768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cab5c3f90a382ab3b36ac06fc112696065a6f351e529876f23fd7db25d1c31`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:4347db83d2b7f759a5c538d29b00bc8b1e60038201d84bda578aa5a0a36f0497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e876b97415a60942fe8dc858bd63be541ea9e544e304fe64db774a50b5ab0888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273922644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75ddc14b412c54f0546ab056a2773549d0f926b205aa7411a97e94062f2373b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b5b72d3f3c83ebd840e6b8988c68e6f89cd8b00784f566cc2f52f50021fd1ab4`  
		Last Modified: Thu, 02 Jan 2025 19:29:28 GMT  
		Size: 273.9 MB (273913578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4facc6dd9b1511d29f25d6cdb5894b46acb65614fd66ef4e6c1d9a6c7f94e`  
		Size: 9.1 KB (9066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:07d63b69c408eb5f1024971ff81cf0456ca3af98755ad5c43402eddf0e929f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11896969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281dd06263cfa9233a5ef217c49febd68559038b867bf1d0d030bbc29a4120ae`

```dockerfile
```

-	Layers:
	-	`sha256:88c5bcac19839ff33e19ca8ac6b7ca8331d919f44761f0529b6a803697c8435b`  
		Last Modified: Thu, 02 Jan 2025 19:29:25 GMT  
		Size: 11.9 MB (11885216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c8abdd46e4ab83e19c08d3ff68f5bf0ee3ca3ef4910841b4b214e0c9735397`  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241229.0.293060`

```console
$ docker pull archlinux@sha256:4347db83d2b7f759a5c538d29b00bc8b1e60038201d84bda578aa5a0a36f0497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241229.0.293060` - linux; amd64

```console
$ docker pull archlinux@sha256:e876b97415a60942fe8dc858bd63be541ea9e544e304fe64db774a50b5ab0888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273922644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75ddc14b412c54f0546ab056a2773549d0f926b205aa7411a97e94062f2373b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b5b72d3f3c83ebd840e6b8988c68e6f89cd8b00784f566cc2f52f50021fd1ab4`  
		Last Modified: Thu, 02 Jan 2025 19:29:28 GMT  
		Size: 273.9 MB (273913578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce4facc6dd9b1511d29f25d6cdb5894b46acb65614fd66ef4e6c1d9a6c7f94e`  
		Size: 9.1 KB (9066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241229.0.293060` - unknown; unknown

```console
$ docker pull archlinux@sha256:07d63b69c408eb5f1024971ff81cf0456ca3af98755ad5c43402eddf0e929f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11896969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281dd06263cfa9233a5ef217c49febd68559038b867bf1d0d030bbc29a4120ae`

```dockerfile
```

-	Layers:
	-	`sha256:88c5bcac19839ff33e19ca8ac6b7ca8331d919f44761f0529b6a803697c8435b`  
		Last Modified: Thu, 02 Jan 2025 19:29:25 GMT  
		Size: 11.9 MB (11885216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c8abdd46e4ab83e19c08d3ff68f5bf0ee3ca3ef4910841b4b214e0c9735397`  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:efed7c2151d9875426ba77d4bec4c8126a4f422c834131dc4d179c20a1242a8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:4bfad6b404e7e2ae4b8a36b048eb9d469e69445f5d2196e9ceec72468cca5d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152782285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c652e2bab60c298ad1aa7099354fd534a79c84e8179d36a45612d8f60887aec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9b7265eae795fc1044fb1a9ad407f315fd7f47f8171b3d6934ad0dd34e7c2882`  
		Last Modified: Thu, 02 Jan 2025 19:29:35 GMT  
		Size: 152.8 MB (152773979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c01223f5d96e3452caf453a754a8782a236f112179996e540b0c33e63b63f7`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:8bb0af37c95a3ba4a150df5169d2a3992fd4f8c57ed5381663bf07abfb54927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8089740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cb71c59b5771c19b16afdf036b39620fa029d0a1edb336b2378f504581bd76`

```dockerfile
```

-	Layers:
	-	`sha256:4759a3aef3624507e0c85dc69f41b813dfb35571ca16f268d3c4fa669b0d5ecf`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 8.1 MB (8077768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cab5c3f90a382ab3b36ac06fc112696065a6f351e529876f23fd7db25d1c31`  
		Last Modified: Thu, 02 Jan 2025 19:29:31 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:83c6137d571e9c200fe12425cfb8f568d2b07c4bfebcf54a85752cbdab5db402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:1fdc20a8cc97aa4e33705ee9458e97d0768a53a19fe4658f88b8ed0fda084dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323773511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0516e649224737387e5d54cd8d688daf2f295843abad8d22704fd8dd9b8157f8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f5328e0670e08fe414577918346f76fcb4d4f11d79607ca4de12c8ccf9a794af`  
		Last Modified: Thu, 02 Jan 2025 19:29:48 GMT  
		Size: 323.8 MB (323763288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d512af53f6bdab09a1a17db17f768ac11a2af7c63058ff13a474dcb9b5f1d4b`  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ec4a71aa2d6be867da722570d0c04aa0ec293ce666a1f3b15e2620d9474f9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa3fe87abbc1c01628b94fa5ccc88653228a2f151860029c2fa0ea470568cff`

```dockerfile
```

-	Layers:
	-	`sha256:69e57fae915251e1ac5985cee8a0673b0f1bdd96e56db5cbf122ae12e4d95ad4`  
		Last Modified: Thu, 02 Jan 2025 19:29:43 GMT  
		Size: 12.2 MB (12153736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4a5129e1bc10603215924119a907c069c8a01c8bb976b73765d7db9e8727de`  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241229.0.293060`

```console
$ docker pull archlinux@sha256:83c6137d571e9c200fe12425cfb8f568d2b07c4bfebcf54a85752cbdab5db402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241229.0.293060` - linux; amd64

```console
$ docker pull archlinux@sha256:1fdc20a8cc97aa4e33705ee9458e97d0768a53a19fe4658f88b8ed0fda084dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323773511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0516e649224737387e5d54cd8d688daf2f295843abad8d22704fd8dd9b8157f8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241229.0.293060
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Dec 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-12-29T00:07:35+00:00
# Sun, 29 Dec 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241229.0.293060' /etc/os-release # buildkit
# Sun, 29 Dec 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 29 Dec 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f5328e0670e08fe414577918346f76fcb4d4f11d79607ca4de12c8ccf9a794af`  
		Last Modified: Thu, 02 Jan 2025 19:29:48 GMT  
		Size: 323.8 MB (323763288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d512af53f6bdab09a1a17db17f768ac11a2af7c63058ff13a474dcb9b5f1d4b`  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241229.0.293060` - unknown; unknown

```console
$ docker pull archlinux@sha256:ec4a71aa2d6be867da722570d0c04aa0ec293ce666a1f3b15e2620d9474f9cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa3fe87abbc1c01628b94fa5ccc88653228a2f151860029c2fa0ea470568cff`

```dockerfile
```

-	Layers:
	-	`sha256:69e57fae915251e1ac5985cee8a0673b0f1bdd96e56db5cbf122ae12e4d95ad4`  
		Last Modified: Thu, 02 Jan 2025 19:29:43 GMT  
		Size: 12.2 MB (12153736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4a5129e1bc10603215924119a907c069c8a01c8bb976b73765d7db9e8727de`  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
