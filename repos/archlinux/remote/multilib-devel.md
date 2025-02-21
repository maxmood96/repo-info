## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:a1d165d45e611a1b87f596fc78b313d8391902672bd9013f9616548a705b6e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f3c004f01ee43a894a7a3dc19b9b606c7b26624afdfda8015a6a74312614e4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329487557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b468e2c5f8a40e59a573006cf05b517ec5bec2eedab8fe4661af401253f5698b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.version=20250216.0.309127
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.created=2025-02-16T00:07:33+00:00
# Sun, 16 Feb 2025 00:07:33 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Feb 2025 00:07:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250216.0.309127' /etc/os-release # buildkit
# Sun, 16 Feb 2025 00:07:33 GMT
ENV LANG=C.UTF-8
# Sun, 16 Feb 2025 00:07:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6d9a2c0d9b66041daae21c05e3ad4574def9c5fd04ee65c782308d2ec3c0bab3`  
		Last Modified: Tue, 18 Feb 2025 20:31:15 GMT  
		Size: 329.5 MB (329477343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efe6812dfb51a689dd17986f33de56fa468aef442a5d53aabd5025527d59cdc`  
		Last Modified: Tue, 18 Feb 2025 20:31:09 GMT  
		Size: 10.2 KB (10214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:cc0ace19b8c8a71954fc34af7c0f5b2e5c63e235db7f95b1e3fd587f8b7eb555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12237566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1694d065e2552642108ce0a5d987242cf2be09d0828aebf1e8c55a0a2bcb07f4`

```dockerfile
```

-	Layers:
	-	`sha256:a26fc6000642457c9d046a26ad99010e95798b8a5d3110101c5f88c0d4a60327`  
		Last Modified: Tue, 18 Feb 2025 20:31:09 GMT  
		Size: 12.2 MB (12225756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2c65d39d0c2c80fbe70f73c25592f5e264d655db1dc618dd28c88d3f156f29`  
		Last Modified: Tue, 18 Feb 2025 20:31:09 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
