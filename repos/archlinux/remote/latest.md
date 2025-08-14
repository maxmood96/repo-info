## `archlinux:latest`

```console
$ docker pull archlinux@sha256:104d24b4464e89a16566d3e68ce0e2707aa15258c690ee9bef755930e8bc1c2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c8c254d98a4d8a768a3df6664727d7fc47c62b7fe680db014182c7d5745cd63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168824318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e8ea7cbe1d296ba02abd87dec90b798901bc5324b4562bce7438ac7d44cdc2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250810.0.398652
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-08-10T00:07:35+00:00
# Sun, 10 Aug 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250810.0.398652' /etc/os-release # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 10 Aug 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:99c7ced3048ae449d7bbe868fdaae1794ddf29670e0a8e66476355dce22d3e82`  
		Last Modified: Mon, 11 Aug 2025 19:48:29 GMT  
		Size: 168.8 MB (168815972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f76e6e58198908de29c433b05f6a58a12cf634457cf1353c9f7f150646842`  
		Last Modified: Mon, 11 Aug 2025 16:41:46 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:40122200033cb0780c5a2d37e455c41bfa7e966c438a24262be35ec377878c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e70a861316fb14ab79d0433bea4832f12d70583ddb6b1cf05a96b63efef04d`

```dockerfile
```

-	Layers:
	-	`sha256:11e6c7542a04c87bb06d2a610e86d83337140b55ab0c91292b1bc92a51e5c54d`  
		Last Modified: Mon, 11 Aug 2025 19:48:19 GMT  
		Size: 8.2 MB (8162399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd693ca89249bed05ff6361ea9f9065ca971e556d84cbd5c62692652700f323`  
		Last Modified: Mon, 11 Aug 2025 19:48:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
