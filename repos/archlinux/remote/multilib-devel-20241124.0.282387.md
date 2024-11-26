## `archlinux:multilib-devel-20241124.0.282387`

```console
$ docker pull archlinux@sha256:21ee00acf5700be693c441245103c1a379fe5be67d095629e60a3e2d48de7e4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241124.0.282387` - linux; amd64

```console
$ docker pull archlinux@sha256:b6ba00ddf979ccdfa8f91ffe50679dcfd8e626b26395a58a5cbbc0991e3f174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322288757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cc884d991aa3d8a713d7a55a07032b534ad2e37082fb6a9ffdd5acaac4ec77`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a6264ef3f56194f7e1c6232cf9df5491f14cd5a516e567990264e87feae1d721`  
		Last Modified: Mon, 25 Nov 2024 20:25:12 GMT  
		Size: 322.3 MB (322278518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4801d8c4cbc3bdbc6548534820c5c5d771d66f25c77feb931358bb8109474b83`  
		Last Modified: Mon, 25 Nov 2024 20:25:02 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241124.0.282387` - unknown; unknown

```console
$ docker pull archlinux@sha256:85dbdc55e30e0bb61c95cbe3f212e8bb00be5053554b882c8728450e482f1d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b609b4af0dbdd86a5d1cc10764efcec7acd269cc251cc2a369029924e440b1`

```dockerfile
```

-	Layers:
	-	`sha256:43ca7f46cad5b757d77d5e5e50162a155ad2a0e727d70606b7d8375aa909dfd9`  
		Last Modified: Mon, 25 Nov 2024 20:25:03 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94666142745f37a235589a36d2449ab4ebcb1a36048b6492776617d876742101`  
		Last Modified: Mon, 25 Nov 2024 20:25:02 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
