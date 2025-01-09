## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:9ecc262fbd132fa18063fc304531e7dcaf55914fa0ff994096d892cb3d70b349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:26979d8c51891f396ece05f2c90b53409cae63a87772a2877b5f1bac54da9e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274213234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1447420cef64fa70a34e3ca281f0026e5cb5c9ab2ab0c1342a66ef44585e3ab6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:680acf88979475a77fdde57deae10e0d8eb993a7fa27c17ea6fd78b65cfe855e`  
		Last Modified: Tue, 07 Jan 2025 01:29:59 GMT  
		Size: 274.2 MB (274204153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100804ba99fdbc32e55b6f12d0aedce47acc4cea4bca527ba0a7e7acadca624c`  
		Last Modified: Wed, 08 Jan 2025 17:58:47 GMT  
		Size: 9.1 KB (9081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:1dd85f8569762b98ea87e074c90883936d1db6607f7d1db9ec07e3c93f921d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e97937616da1706ac16b85533cd21d1afd388b9938b013a56e0b301fe4b6419`

```dockerfile
```

-	Layers:
	-	`sha256:dcb1c443c16ca59c7b58814eee54cb028987b595258f627e91ea9b551eff676f`  
		Last Modified: Wed, 08 Jan 2025 17:58:47 GMT  
		Size: 11.9 MB (11896302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f906c019f07af9f364187d9b8b62e582e755180382c5684c153d76a9884581b`  
		Last Modified: Wed, 08 Jan 2025 17:58:47 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
