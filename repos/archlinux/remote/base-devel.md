## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:60aaac6e5cb608323480bc3b49e9110183f3dba6baa0c5e57dc315f4365bdf42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:81e52e1f2371eb0aa8cabc06ceb0a5dd83a8922874a898dfa0680d65bfe2964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278602887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbea432e68fcb65b7085457fb60714e702b07d8d4a871be547b57c7ff75b811a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.version=20250202.0.304438
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Feb 2025 00:07:59 GMT
LABEL org.opencontainers.image.created=2025-02-02T00:07:58+00:00
# Sun, 02 Feb 2025 00:07:59 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250202.0.304438' /etc/os-release # buildkit
# Sun, 02 Feb 2025 00:07:59 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2025 00:07:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6132708ec3c2a0f14172f35bddb52ee1e6cc2a7780f822e4a251821b9be891fa`  
		Last Modified: Mon, 03 Feb 2025 19:28:00 GMT  
		Size: 278.6 MB (278593852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe56e40e02767b104fcfe35211e7cdc487c5a341081fda052a551126e48076a`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d976b5d33209fcad192e77e11601d050c099a6350d4074e4df423de7fd29ac68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f75131ec9424866f2afaa1c8cafd1ba7de562bcfaa287828dac08ecc655a922`

```dockerfile
```

-	Layers:
	-	`sha256:69ee1ac4478e893f3b2befd53892a58e151f7525b15cdc7657415cc4b2295449`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 11.9 MB (11895956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbacc84a84cc36008654c1644acc495f1f29b7171a78b35c11d5c30ea74137c`  
		Last Modified: Mon, 03 Feb 2025 19:27:57 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json
