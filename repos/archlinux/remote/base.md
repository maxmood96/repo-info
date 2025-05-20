## `archlinux:base`

```console
$ docker pull archlinux@sha256:c0965d07320c79ca2e3a1cc9e303757f6b0055aa0437571523f5eedf78b15690
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9fa258bd0dfa27b6993d28acb34832a3f94d9ef61d3357c8c73117508b17b21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162330911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8174adfffde89ff3606b3c9753a9697d1870fef607c25c859c75f1e53258d4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.version=20250518.0.352066
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 18 May 2025 00:07:44 GMT
LABEL org.opencontainers.image.created=2025-05-18T00:07:43+00:00
# Sun, 18 May 2025 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 May 2025 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250518.0.352066' /etc/os-release # buildkit
# Sun, 18 May 2025 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 18 May 2025 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:99a048503a97044f04b8022dcfd166a9e0637b56ea0e41796323764dd2eb2749`  
		Last Modified: Mon, 19 May 2025 23:01:39 GMT  
		Size: 162.3 MB (162322547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fed4f35c8e48a595faf53bcb00201ec2e1e71c970b61ffd550806f06d9f5aa`  
		Last Modified: Mon, 19 May 2025 23:01:36 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d0df1ba58b6cabe7c32dda56cd616d58a212c1ada0afb9477bc5b4e7eb780b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8180810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dcc064dd1543e1948df36b4d48bbfa2be02230bee38acfb546ba8cfbd9ffe0`

```dockerfile
```

-	Layers:
	-	`sha256:ed126e2bed0c7303d11f28253eeed2c730c5d1865aae101051e1dec326c113d0`  
		Last Modified: Mon, 19 May 2025 23:01:36 GMT  
		Size: 8.2 MB (8168839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330cc0794d0c91afa2f316bdfde947ddf7af56bb1ee4b19babef53802ebbf922`  
		Last Modified: Mon, 19 May 2025 23:01:36 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json
