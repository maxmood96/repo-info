## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:a20d103ba70c910b40a274748a0bbb43d96f4e37ef45ce367c080aee370dfde8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f5d80e223b925204224653f63ddc2bdb2ece26691cad67c3a7e526a0f1147f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4009240989a60ea769d91858d428615edb2ee2ac54fa2e1fe85883b83548bc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad59c724b2d7e7041a88eae078be10f472732091bab7b3ff59e2bbd5056e65f6`  
		Last Modified: Wed, 29 May 2024 19:57:22 GMT  
		Size: 266.2 MB (266230027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e81a3aeb405ec80b4084aef14b8997cea2a066263c3b5bf3218dde94801e58`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 8.9 KB (8939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d61ec44f785a760a1381e1283aaa568c4704a72073bef9e65499dc9286369b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11443681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3997782d4cceaf17cb4eedd076574ed31d5c32d445e56e496d3c466fcba40f8`

```dockerfile
```

-	Layers:
	-	`sha256:c104f7a606c0dd987c990b87afe2b92e5803be27f08b84047589192c1213ba91`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 11.4 MB (11432227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce3c5f8e22cac3c19169bb8b5c9e7bfa626a32629acf911dbc0a8f73f51feef`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 11.5 KB (11454 bytes)  
		MIME: application/vnd.in-toto+json
