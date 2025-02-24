<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250223.0.312761`](#archlinuxbase-202502230312761)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250223.0.312761`](#archlinuxbase-devel-202502230312761)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250223.0.312761`](#archlinuxmultilib-devel-202502230312761)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:4fb8754cfe434a15394e9ec4d7171b12f55f8b6b12bd02f643d2ddbbd060248a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:3a7ff222088d954173df233a61ced6a8201f13f60941c22d6e1fb69f0ed517b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158540452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab16fe2940c6991fd775a4bb07bdc0e7cc8be340f1afe54c7767b7d1f14e4ec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:3e2123c5b4d73d442f77ddda09cf084b535f4a6441073d1be8c8f96e19e1f854`  
		Last Modified: Tue, 18 Feb 2025 20:30:38 GMT  
		Size: 158.5 MB (158532132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6712b26246f21f16f7d62a4b8127e64785a617485e8b352b090d27c383c5cde4`  
		Last Modified: Tue, 18 Feb 2025 20:30:34 GMT  
		Size: 8.3 KB (8320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:7b3434b8955ab0c4766423198e4fd0dad1fbecc3a07420de5af8a866fd875fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8161821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5025c49fd8a3bfa3c78b87593a5dc85c2e42023c282f9ac783155e8f2fda048`

```dockerfile
```

-	Layers:
	-	`sha256:b986e20dfd2b032eb9aea5fc8eb54a7156e504e45050c291fc7e32519b2ee55d`  
		Last Modified: Tue, 18 Feb 2025 20:30:35 GMT  
		Size: 8.1 MB (8149850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b620def17ea8ad97365c9b43e7515412576d4f513f887ea9058a313b5c85ad`  
		Last Modified: Tue, 18 Feb 2025 20:30:34 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250223.0.312761`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:caeef94ae95a271932b12257e369f2972dbbe2f586c93a0c2b0b0845761cd13c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:951df25434f499b8347640c2783ae0947b23b437f5b51798bac11bc69d868185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279482279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd021c7fbac2f46df87e291d78f0acb63d220f9c187ecb79b59c52db87c3cc19`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:766bfb0508c63b1a37d31b5663ed698d69413b056fac69b8c517a8a1a2039709`  
		Last Modified: Tue, 18 Feb 2025 20:31:24 GMT  
		Size: 279.5 MB (279473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d0b238d6ed00934480fbc0c4cb7fa53092c5d360d83cde63772ab1fd82262`  
		Last Modified: Tue, 18 Feb 2025 20:31:17 GMT  
		Size: 9.1 KB (9063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8e9a510bbd22cf8bb36a4038f5a9a214f3629416618b037b5fb55f203b2092d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11968995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d81e6f30510ab63b8b3ae3f70a4991fc563eda381bcec0b74b9a55281e17ac`

```dockerfile
```

-	Layers:
	-	`sha256:56ce7785aa3730f3221de44cc2081dbff647b6830426393adc854546148a4464`  
		Last Modified: Tue, 18 Feb 2025 20:31:17 GMT  
		Size: 12.0 MB (11957241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f80386277b0a620c70773c1121ce215cebb17718a85de4e4f2a620c3ac1ac3af`  
		Last Modified: Tue, 18 Feb 2025 20:31:17 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250223.0.312761`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:4fb8754cfe434a15394e9ec4d7171b12f55f8b6b12bd02f643d2ddbbd060248a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:3a7ff222088d954173df233a61ced6a8201f13f60941c22d6e1fb69f0ed517b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158540452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab16fe2940c6991fd775a4bb07bdc0e7cc8be340f1afe54c7767b7d1f14e4ec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Feb 2025 00:07:33 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:3e2123c5b4d73d442f77ddda09cf084b535f4a6441073d1be8c8f96e19e1f854`  
		Last Modified: Tue, 18 Feb 2025 20:30:38 GMT  
		Size: 158.5 MB (158532132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6712b26246f21f16f7d62a4b8127e64785a617485e8b352b090d27c383c5cde4`  
		Last Modified: Tue, 18 Feb 2025 20:30:34 GMT  
		Size: 8.3 KB (8320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:7b3434b8955ab0c4766423198e4fd0dad1fbecc3a07420de5af8a866fd875fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8161821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5025c49fd8a3bfa3c78b87593a5dc85c2e42023c282f9ac783155e8f2fda048`

```dockerfile
```

-	Layers:
	-	`sha256:b986e20dfd2b032eb9aea5fc8eb54a7156e504e45050c291fc7e32519b2ee55d`  
		Last Modified: Tue, 18 Feb 2025 20:30:35 GMT  
		Size: 8.1 MB (8149850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b620def17ea8ad97365c9b43e7515412576d4f513f887ea9058a313b5c85ad`  
		Last Modified: Tue, 18 Feb 2025 20:30:34 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

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

## `archlinux:multilib-devel-20250223.0.312761`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
