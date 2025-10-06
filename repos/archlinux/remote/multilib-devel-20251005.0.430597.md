## `archlinux:multilib-devel-20251005.0.430597`

```console
$ docker pull archlinux@sha256:9c2a97563205f30cee1b89eadd37e395b95119a2beb5c3d47ba6eb5c66c566c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251005.0.430597` - linux; amd64

```console
$ docker pull archlinux@sha256:849a203ca9d073b4a0e6319f894058651f5ff820782d98551fc32fbc01609a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341657929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7198f253c58fdd64bb79f20545d75bfe684c7c6ae6d32a9772d221faf7b77499`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:57d32341d0b304edbdd20efcf9481afeb1fb71b457948c77d909ebc150363d3e`  
		Last Modified: Mon, 06 Oct 2025 19:51:26 GMT  
		Size: 341.6 MB (341647654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef2d5695280fef0de17375d8fc55aad6a24e3a57f486684d7c1ec271748ec15`  
		Last Modified: Mon, 06 Oct 2025 18:55:35 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251005.0.430597` - unknown; unknown

```console
$ docker pull archlinux@sha256:c1d30bcfa1c166f36cecda5e159a8899d174af36aaeba4b0e7f4dad1420c6bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12400183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640f98c73b416a4cdd411101b281c688ce08ccbc1f79b8728accbf166fc122c`

```dockerfile
```

-	Layers:
	-	`sha256:1fc784a31e518e40643ca31df64bade42c39955b1ebfa24ec82662f6c1aeb1ff`  
		Last Modified: Mon, 06 Oct 2025 19:48:33 GMT  
		Size: 12.4 MB (12388372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22eacafbbc8af6591d002ca0b066e314ef827d493d5283e795026e4a1004230`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
