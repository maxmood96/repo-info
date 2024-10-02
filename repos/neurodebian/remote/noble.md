## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:be2f3716a4cec9a306cbd8d426117f8aab8727d6c0e9c200476a875338d9d419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:ba3a22d89a7a32732bfabedb6f8b97f74f7bf663d7bfd10ee35e90a14d2a5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e4911df4af3c3f01073a17ce1734d817aa7226671d53511d1849774a4d52c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657f2a0c259ff376993610ba80c419c5073712870b3c4102fc3fdc47621052e7`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 3.6 MB (3557869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f17957c9ae33ba95b7c1ae44535c130d7e8a9162b4c30ca673dff0bc86daa99`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d862893fb97f214fe809b8a564f061db2026ae314f8528202042c8db3129ea`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2243d0bd10d8e5d8d8b1fd7b85071b0e2e33209c7516489aa762758e173a6f`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 100.8 KB (100790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede965cd728e5c520133c9d29a298e463b405f1db483e381f6cf039e20b40e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691abb4119b847b8f00db93ef20163cc6264a958f96d64d276c39424ec3522e`

```dockerfile
```

-	Layers:
	-	`sha256:5d62bb1da4f37e3074d7ac217fac968beddcbc678b35366d4f7a76312ec7f33c`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 2.0 MB (1972437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2751407fb0c291db83cf3d75ddf8cbde3b70fc70869d8e91bc616ea92f5503`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 13.4 KB (13410 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4981901a57f223c1b9c8891c69885caee2fd40918860bb6ba85cca873a53a0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32545805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b59b6aff1df9ce330d718830cddac2344afbfd17f2d9bb3388ec169422c2da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d97f4c88babffcaa2541504a32c0a03166773de0a08bf0c98636dc16613977`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 3.6 MB (3556989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ac16409873f9bdc1698e67b746242ec770699376195c1c3ed68f171168f3aa`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316fe113f82a4d8a693191a9c1a292b0fb3d412c356c88cb147e63b90264753f`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03520ce4621ce6480c2bc6e4b7308731f458a108efd055cdd6deed3bb77b727e`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 101.4 KB (101390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf9021c868e6d98d032cc69d7693491d1fe3023ff5fa80663af9dce9b5741802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb8d4ae921713e80f86d7d927cf18d51deb01d257a38ea865052b5f73c297a`

```dockerfile
```

-	Layers:
	-	`sha256:82f370cf47cfb6114fa6a88a78795e7ff6f2559c5c3305a72fbfba6aa9050207`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 2.0 MB (1973482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fa90318a31deac3447b6fa554bcbed7d3186b765b2ccc8ecf219c00c76b6e3`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json
