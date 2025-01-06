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
