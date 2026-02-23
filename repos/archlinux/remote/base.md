## `archlinux:base`

```console
$ docker pull archlinux@sha256:bb1e5dd58eb79755e736ac530292074f4408572c0fbc4306cd62b431fdf356f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:d1f8276aa44cadeb2e24ddc4cb0d1652adbfa2b1e3666b605d7836b319152d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128244330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16627d83cac7e6bfdc3563c45b4524532f98b883c4d6241654eb19a394fe0dda`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:29 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:29 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:32 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:32 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b59995756522a75a3c4247abc7a41c128cb0ae714bc23abd8d4ea5a6d52f6609`  
		Last Modified: Mon, 23 Feb 2026 19:08:58 GMT  
		Size: 128.2 MB (128235739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371cb576f6bfe6270bc967bcba25fe654f27a04fb479e2cf49e296cd08061b93`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.6 KB (8591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b7b7515da3e20762269219a31b9b459a6c17d12dafa946a6a6e431214cf63381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfb009170c6534b9f71b5867254e29eb7f1c6496c8eadb65c6fbb814c1edf63`

```dockerfile
```

-	Layers:
	-	`sha256:740206aeb7f4cf06ad8019280f6d1f32ad6cb22ab4d0cb6a21c223cfdba8bb51`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 8.5 MB (8477557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4280616b848b7f7acf589a88e0ea0f9f96b1c7f514bff293a4cf4e29f69304e8`  
		Last Modified: Mon, 23 Feb 2026 19:08:55 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
