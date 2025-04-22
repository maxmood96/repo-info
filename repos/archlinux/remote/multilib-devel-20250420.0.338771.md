## `archlinux:multilib-devel-20250420.0.338771`

```console
$ docker pull archlinux@sha256:a9454267500cb19e43ce9d8f276021f60ac16f90b90a5b94cdae8c0619e58266
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250420.0.338771` - linux; amd64

```console
$ docker pull archlinux@sha256:a31b1a042ca97f5980e5f3042b8107ab1c8089d7754fae7903652c38a42fd5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331756959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7498f9f422b380616dae9cf2b35fdd81d50035db475d0195da20034dbfb84781`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:974b446697e9df1a9de12f2eee3522356a152f031b88796f709ddff7138a73cb`  
		Last Modified: Mon, 21 Apr 2025 22:35:20 GMT  
		Size: 331.7 MB (331746663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c42aad208d10e2a974370e88bbe7c59ef5ea182002c108842f8a82a37b803b`  
		Last Modified: Mon, 21 Apr 2025 22:35:10 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250420.0.338771` - unknown; unknown

```console
$ docker pull archlinux@sha256:816bec377024b31c9d0e9301336b59bac8de6afedfbbe074df59b2c20b7d2045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12266637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c0e0f29d3dd8863ce24bf061124be99d59ab2f3ee3a65c083372f481edc854`

```dockerfile
```

-	Layers:
	-	`sha256:eb89539594f1987717d8d678eee84c24982c8f4f95486eaf1ddee199b2373cfb`  
		Last Modified: Mon, 21 Apr 2025 22:35:11 GMT  
		Size: 12.3 MB (12254826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a0ccd60cf8cc9a43c4787fa23fb1bd98836285be840075c8d826a4ae56fc01`  
		Last Modified: Mon, 21 Apr 2025 22:35:10 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
