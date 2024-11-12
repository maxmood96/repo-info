## `archlinux:multilib-devel-20241110.0.278197`

```console
$ docker pull archlinux@sha256:f756be0aa4648e20afad534e889e4216214e25846df2057b743e8846fbd89f95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241110.0.278197` - linux; amd64

```console
$ docker pull archlinux@sha256:bfeeb9641d53f7d9533b47c7d3a8d6de993c56af2e833f22f31b661a353a781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322288842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ea8b8396eacb2c730bce363a73c77f035936f20e2567e4d7dde8301da66c35`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3ab97c08b12194b39487459a35c6eae1338779f256278f9827959dea61a640bd`  
		Last Modified: Mon, 11 Nov 2024 18:58:58 GMT  
		Size: 322.3 MB (322278597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185935dc4d733369436d7800e5b89c125825533bc6730089b059f3beea3a0d42`  
		Last Modified: Tue, 12 Nov 2024 02:02:45 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241110.0.278197` - unknown; unknown

```console
$ docker pull archlinux@sha256:780ef94a07822cdcb10ca179663a40399e310a5a36f017896484fa5ade08024f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3011ab2523f0837a61f4f661ec9c40e39e3746f552e2ad4ae225c8cd2472bc1e`

```dockerfile
```

-	Layers:
	-	`sha256:ada1a30e8981df3ad033076adbd5ba627d5a2b2616d13ff1044b3507fda4dc70`  
		Last Modified: Tue, 12 Nov 2024 02:02:46 GMT  
		Size: 12.2 MB (12164481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5950ebd2dbb8b0259fbcb40f182c9844f630be2722b5b1687d3a97f1e7af88a6`  
		Last Modified: Tue, 12 Nov 2024 02:02:45 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
