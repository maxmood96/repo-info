## `archlinux:base-devel-20241013.0.269705`

```console
$ docker pull archlinux@sha256:291198370afb8645d8341adfc354a407c0f981fd66a3bd89a267080db05314c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241013.0.269705` - linux; amd64

```console
$ docker pull archlinux@sha256:cf078f3ed4c05215655cf546ec9baf1a722c956dc615a83afb9504ba5f2de2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272207868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fef481d84240d74d79f1bf7ff90814f04d3e3014a28672e8236941292a858f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.version=20241013.0.269705
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.created=2024-10-13T00:07:34+00:00
# Sun, 13 Oct 2024 00:07:34 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241013.0.269705' /etc/os-release # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
ENV LANG=C.UTF-8
# Sun, 13 Oct 2024 00:07:34 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e76fd01d88ac44554cbddc68bc825ded8ae4866aeb8709765151c2b9cdfc95d4`  
		Last Modified: Mon, 14 Oct 2024 16:58:37 GMT  
		Size: 272.2 MB (272198866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea70b41381990070a0d797c943fd2e654e382d1223d9fb0a7ba106397286a3b`  
		Last Modified: Mon, 14 Oct 2024 16:58:33 GMT  
		Size: 9.0 KB (9002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241013.0.269705` - unknown; unknown

```console
$ docker pull archlinux@sha256:ab2c1268d29e0112e8915372c25861e5a230ff20078666b0f152ed03611f67fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e29df3c2a92e91668ba098d2fab29e941a330b354ab048a70b2c41f1c888ff`

```dockerfile
```

-	Layers:
	-	`sha256:1b2b3499eb47cff39b43b50198c0873f43e8566eaa3599661471616ac845991c`  
		Last Modified: Mon, 14 Oct 2024 16:58:33 GMT  
		Size: 11.9 MB (11900567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efa016cc5092fcd316db4ebb0bbdb0b5b3bd0404d7f0fa71f8fb109cf0e228f`  
		Last Modified: Mon, 14 Oct 2024 16:58:33 GMT  
		Size: 11.5 KB (11541 bytes)  
		MIME: application/vnd.in-toto+json
