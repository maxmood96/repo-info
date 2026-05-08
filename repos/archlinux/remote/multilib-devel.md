## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:98169d312640757c3f9fbc5f91c48b6ef5963da789fbe88b0889418f6f233e4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ad87a9b436197a5e25abf2f5b202bf63be776183bad12616f6ec80199cf482d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275758734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af28ca4534de49ae005e159344b62cae7f473dc060869f033eb0ce3149ee2d08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.version=20260503.0.523481
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.created=2026-05-03T00:09:00+00:00
# Fri, 08 May 2026 00:02:33 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 00:02:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260503.0.523481' /etc/os-release &&     true # buildkit
# Fri, 08 May 2026 00:02:39 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:02:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8951f99ef7054daea6754cde72fc40693309fac635c287747b166ae7aab04943`  
		Last Modified: Fri, 08 May 2026 00:03:26 GMT  
		Size: 275.7 MB (275748374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0633fd9a26c06df0d03ae07ceac7e3df2ab689769502a4a7a7beb94739aa02`  
		Last Modified: Fri, 08 May 2026 00:03:20 GMT  
		Size: 10.4 KB (10360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:62a319e8fe7f939908a6c93dd5988079c2d93eb8a6ad28aade2b00173321bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12318897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa2f71c15a41baca3a95cde3c2b3eeb310dfa5262767ac620d9fbe879ab129f`

```dockerfile
```

-	Layers:
	-	`sha256:28257b1970bb43035f51c37a1292e0d13ab330a8d7b9f0642ee6b771dc79e027`  
		Last Modified: Fri, 08 May 2026 00:03:21 GMT  
		Size: 12.3 MB (12307047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6414041c06bcecfe359359ec3bb5ef24defb75ec47d81a8c9a0e7b2a98409316`  
		Last Modified: Fri, 08 May 2026 00:03:20 GMT  
		Size: 11.8 KB (11850 bytes)  
		MIME: application/vnd.in-toto+json
