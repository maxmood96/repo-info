## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b110853598ac8526a6feb162b408d72fd45290efa6d8eba25753c9a49633709f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:519097be57855db5542c8f2ebd3adb3ecc227dcd5ac8a6a03abff54741fb177f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271740726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89f6c87211862b4036339df6f4049d107e8caa535fecc34e584ea010a076ac9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20240728.0.249973
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 28 Jul 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-07-28T00:07:38+00:00
# Sun, 28 Jul 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240728.0.249973' /etc/os-release # buildkit
# Sun, 28 Jul 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 28 Jul 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:02456fbfa541313d4610d69c6ee80b0e3bd7e3af01f1215c5fd255c79c026988`  
		Last Modified: Mon, 29 Jul 2024 18:57:04 GMT  
		Size: 271.7 MB (271731685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1408e08202e0909786137de5d8856032d602ff18bdabb67b411c2ba43254e82`  
		Last Modified: Mon, 29 Jul 2024 18:57:01 GMT  
		Size: 9.0 KB (9041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:16da886ecc37a6f09f68e7db49a2ff483410edac825264f4e5d08f6b2be27132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11807894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0655e80220f6cc41f0f1f44cfa1b09b87d242675c33ea36d9536894d8660c0bd`

```dockerfile
```

-	Layers:
	-	`sha256:ee04007c105d1d87f18df366f2cf396daa7e38ac639a61db6d4d8073a83db654`  
		Last Modified: Mon, 29 Jul 2024 18:57:01 GMT  
		Size: 11.8 MB (11796391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8749cd4df133cb14387a58bdeda77ebedc394e4f41d6cf9618638585b42347f`  
		Last Modified: Mon, 29 Jul 2024 18:57:01 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
