## `sapmachine:ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2bc645565092702231cef17e5f1bd33ed16358881619307b093957840cd4b543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:345ab0bb20b8d8b1f0f9e73bde5b265e7c75a944c5df0ba256d1a37ff15700c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261612342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6195beea992cb3077538f57c782a64f7b1f86cd4e84224707364b9153afd88a`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d0b72241c9cdcc141ab21e3c4309eaa68656c6e18c45160e79cb3995fa3e5790`  
		Last Modified: Tue, 02 Sep 2025 21:43:09 GMT  
		Size: 232.1 MB (232075407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9aba6dee3c6e4991001c68fceaf810c8a9c537ffa49ef5d2557eda61cc49c2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0809b0d21898ea4cdad0b39ad51fc3b73cc446bab5ca303c93464b86b116a438`

```dockerfile
```

-	Layers:
	-	`sha256:3e6da2d9fbd00e0471807cad58c78f2f4470fb73fb6cefbf71c44b6740fd46be`  
		Last Modified: Tue, 02 Sep 2025 03:09:27 GMT  
		Size: 2.6 MB (2621736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d3d6ea8aca0f41a618c16710e6b8319f7604a94a4425500f0be1d85d2a8dc7`  
		Last Modified: Tue, 02 Sep 2025 03:09:28 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5e761a9d496c8b122fb35f168f57b8deedffa36dd6eee0dad59b26357e7de662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257324995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8d10d15e46e7209045e52b5717a751dc1f1160a1af45e1e60de3b9a9f9d7a5`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9498facd9c1bd331f5bc4513adf0f27d58685854f66fb67641e709a17ba38a88`  
		Last Modified: Thu, 04 Sep 2025 05:22:29 GMT  
		Size: 230.0 MB (229963526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a5bed6cd9074a8444d7026f585cff3679b483e046d52bfaf4e0257b09b069c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8520606a20fd6ca88806d161aa665502d9820907339bdc05d5e929e8ed1d5ae3`

```dockerfile
```

-	Layers:
	-	`sha256:110ba9f548cdf27453a0a13bee6ea74490c690e438301424371ca1fb29053231`  
		Last Modified: Tue, 02 Sep 2025 06:08:36 GMT  
		Size: 2.6 MB (2621511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e511c788aaaef3cc44c8b550a6856127d6323a64f681e9b3435b53e19b9b10`  
		Last Modified: Tue, 02 Sep 2025 06:08:37 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:85c931ee3ccd7720045f3fb307cb2dfdc0a536b27aae14e0163b9149e4166971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267269739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbd41e0034f6a1f99635484b9d580cced74fdeee7d327cf80faa2b1ffce3a5c`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:17663ca7a97bc029f2a9f8d32f709ca8edddec0093e5aa7f0b870b3874e7f418`  
		Last Modified: Tue, 02 Sep 2025 18:40:17 GMT  
		Size: 232.8 MB (232826515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d61f6cca173f81b41c61f886eb6d77a66d03ac10db826028a17fb5a58ec77dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3514fc28dbf455bc113fc0c88eae6abb1c488067a24151f87f6176d617e4024a`

```dockerfile
```

-	Layers:
	-	`sha256:8f3209af7db224b257c4e182dcb263a51d377a792affcb7acba41be44a7cd30f`  
		Last Modified: Tue, 02 Sep 2025 03:09:35 GMT  
		Size: 2.6 MB (2617335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb06bd346d2773a7b5b760f54a8dc13162d2f41310c19520ac024f13a478bbf`  
		Last Modified: Tue, 02 Sep 2025 03:09:36 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
