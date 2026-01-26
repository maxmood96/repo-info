## `archlinux:latest`

```console
$ docker pull archlinux@sha256:3706b9784abbea6c3cae6da206b0f3fb3b7d363408db591604578bc32e022359
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e4ed0eedd03eae66b22fed7ed701bf2f613006ba53f17cbd7052210b0266eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f60429ea8275a3ff82d7b68acba38254601fac1a2b8703ca177b32e12f4c08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:35:23 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:35:23 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:35:26 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:35:26 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfa1d0a816e4d378cf45371b96ba566c4685aaaa97ff23e1b3d7460c5346938`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.8 KB (8758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:4e3a1a63a8528a69291e7c55660cade89e8f6d059f29063668aac8697584c097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe11e20c4d32f87d6bbd1d16687621492a2d8f833b9752337d61602987924f8f`

```dockerfile
```

-	Layers:
	-	`sha256:198bbfd8e144914aa40395c9717ce5b4a3222a3ac8308f20f9886f5e875c4ed2`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f941c6325cc9b870babe7067404882ef1c0a36981a131fca2cf27b1ea41ed6e`  
		Last Modified: Mon, 26 Jan 2026 19:35:52 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
