## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:ddf93aeb00bb0be8dd2aadbd643df87c377e2f8726740303e6c44c7090e10958
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f060ca5c442d84181890d7da8c2aa5e417461284d9bd53349ec382255ac172b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322033407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d25e6dcbb4408f220a503251a6c8f577930f571883648f75e438a244896c006`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240922.0.264758
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-22T00:07:28+00:00
# Sun, 22 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240922.0.264758' /etc/os-release # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:af8cd7f7e1674adbe5034430b3436c5d6f18139c2874c5b6dccc976d10e524cf`  
		Last Modified: Tue, 24 Sep 2024 01:01:02 GMT  
		Size: 322.0 MB (322023290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0728a7a6acfbd344c411fa9b8d285bb2f7a0ca9eed9c8bbe2547b97b79eb0b59`  
		Last Modified: Tue, 24 Sep 2024 01:00:57 GMT  
		Size: 10.1 KB (10117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:418c036fa6b5f6794ec089722431e97abdc54df35ddf8a34bf2b5a338b2dd188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c38cbab71b56f267bf8f4634acf241001255611e093755c4b621d75aaeb18bd`

```dockerfile
```

-	Layers:
	-	`sha256:c5d329deacd452b4bbc1f7a075485844a80c9755f285b2c4c087b1e4ff91383f`  
		Last Modified: Tue, 24 Sep 2024 01:00:57 GMT  
		Size: 11.3 KB (11341 bytes)  
		MIME: application/vnd.in-toto+json
