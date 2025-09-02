## `sapmachine:24-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:0b0f38ccf05439d44f156b92de84a08af24a36a817399ad6fadf1a635809c7f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:8232a92a4b13f3b4cb658a54dc1a9428a9c39e4ada32af069c2e185b373561c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260388157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8173067c708a1587b54371154362c579807b32ef3dfb807f1aedd11c8a553525`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a50d830cd7b89b3c083bcadf71169cd5bce29d82c5a77ea1723a4c948aa76d6`  
		Last Modified: Mon, 01 Sep 2025 23:11:59 GMT  
		Size: 230.9 MB (230851222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b3fdfbbca8dd8249cb98d51c944f4a31abb65b38b10836e8ae5777312988ac5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5029120900ff2e2bc12849ebf25ca972d7398e83a113ca0bb09ca80a80fce6d8`

```dockerfile
```

-	Layers:
	-	`sha256:e4ec6eaebce24d1155abdb9fbfaf02f15ef9b728780ae3dd63d5feaa9614758d`  
		Last Modified: Tue, 02 Sep 2025 03:09:15 GMT  
		Size: 2.4 MB (2369044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d818375c328ee06d94e042d46b8d295e6ea59b99109a7cf9e301ed53b3dad2`  
		Last Modified: Tue, 02 Sep 2025 03:09:16 GMT  
		Size: 9.6 KB (9612 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a6697c8d09d394d54bacab2af7e251ad613d9260da7565c20a1e49fedb825948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256109602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a03cf887a302b321769f0192bbe424ca908fd280155d701da47ab5b5e97d7a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d19a104efb799a2ed0a3c213272b79f4d09b6bdb4522dfff52293047438b14d`  
		Last Modified: Tue, 12 Aug 2025 21:16:41 GMT  
		Size: 228.8 MB (228750355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a295e5c1de64dcad714011981fc0c99ae316c3fbce082749c2875e76d9bfb943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5d1bfdae80c5761362f9ead23c233953992fd1d51013f67d2d53928291d1fc`

```dockerfile
```

-	Layers:
	-	`sha256:8676d08e84ade4f4e2dd65655af4187ceef3cc25e6eaa4360b1c8339742ac13f`  
		Last Modified: Wed, 13 Aug 2025 00:09:07 GMT  
		Size: 2.4 MB (2368721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c522ff647a4952f7693a4f8215eb1b1c49e0d6a568ea65d539c0f4c685bc21`  
		Last Modified: Wed, 13 Aug 2025 00:09:08 GMT  
		Size: 9.7 KB (9740 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:91f271ba084f15345228430b3d3eb0ff0cedd78945b4b02969e9432a89b01a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265888759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f664ce45dcf354d654f82741d4e76474c1ae48127ae43d6cf1bfae2e2e1a7ef9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d196f130162bea70ecbde82135c8d8fdba726a4768bdbd14cde0d2f3d0682`  
		Last Modified: Tue, 02 Sep 2025 01:56:50 GMT  
		Size: 231.4 MB (231445535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:948614fb4dbeb382b2d4c0e2544f4c93a7c24a33af447e54880ce1005acd23e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53211646ef43d9cf48026855b1d94d9e43ff542c81b76f4f755685470e3648c0`

```dockerfile
```

-	Layers:
	-	`sha256:e2df7ed11741346e529cb67e09fbecfcc09403ee58e3139d89a8a0f782be879a`  
		Last Modified: Tue, 02 Sep 2025 03:09:23 GMT  
		Size: 2.4 MB (2364517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ecfce23053cdbd4a1981d4f7eb0f762fc98bd3c70d6effad896a5d7e6db3794`  
		Last Modified: Tue, 02 Sep 2025 03:09:24 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.in-toto+json
