## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:9b64088634fd4735991ced27444ac87254b6f8c8344910d47ec89fdc23d8781b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:e9015a5fddf3001741b7536df6b43d32e4515e47fefa3f66171826670efe8043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84055412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726f53fa83bce62babf5ba09b997e19cec5d1d6eae6d2d456ebba75e6356e06e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:44:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9ed56edc4625e727dab8608c69afcd9a33f8e70ca86959f6a772dc224f968`  
		Last Modified: Thu, 15 Jan 2026 22:44:52 GMT  
		Size: 54.3 MB (54329401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9925a093abcda5424517bafb9a9a0635e7e1d16d1566de2a7c31998725daf73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab20d2a6326515878f268ffa7ffb5b99fbdaa79b3966f3677388904e8b868eb2`

```dockerfile
```

-	Layers:
	-	`sha256:3b58925cc9fead7a0ae09ced3dc964f5f2bceba1a2d9777c2ff672d1d2657cd0`  
		Last Modified: Thu, 15 Jan 2026 22:44:50 GMT  
		Size: 2.5 MB (2517398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2410239c37447739e578b0d3dd567d01501218c9d27b0447134839a6563a6ae9`  
		Last Modified: Fri, 16 Jan 2026 01:08:41 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3815d61da9dd9757fccd5a748284b5be98dfeafd06b37f1ee0c992d4630ac079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82616909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f354858ee7adbb318ba469b85ccf9ea23ce06461b10db5c6a6410f7928b451fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:47:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:47:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:47:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badb85607c2e0c5dc66c221780a720c6d90457a143e964515535c4c7e0eb1f9a`  
		Last Modified: Thu, 15 Jan 2026 22:48:15 GMT  
		Size: 53.8 MB (53753085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a3b5f51566fefccc7b068ac13830fa3cc231252a11794125b16f5bb9211eab5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1806135b27fa92c8fc3d5ee094efc459992ffe410f12f64de57b4050204c1c0b`

```dockerfile
```

-	Layers:
	-	`sha256:482534eb2c7a4152992bcb968029931b6bddf0d3538a37dcdb92280726f40055`  
		Last Modified: Thu, 15 Jan 2026 22:48:03 GMT  
		Size: 2.5 MB (2517914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35bac696c94af2a7f72967320f3c31fac82757245c95ac696fa564f46f0f7b9a`  
		Last Modified: Fri, 16 Jan 2026 01:08:46 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6ca469484a052302eae778154a25a7746c17e60920ffc5348df6b643a3e984ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89829510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3076b81887ab069a6060be6628cd1c595a7ac2c00c849a6873eba3076bc1444a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:43:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:43:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 23:43:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a462630986a7d5afded01887eefac9f337bce068aa1866d433a12734544eca`  
		Last Modified: Thu, 15 Jan 2026 23:44:15 GMT  
		Size: 55.5 MB (55523351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e566f4c3beb20250f28bc1518a3e376345180f0640176d05fb72f9ed9649ea2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b028848875e48eefad19bd9aba31b8f29244979456e9c7c0d1c02057952509`

```dockerfile
```

-	Layers:
	-	`sha256:ed39f4afc622e399a0b425b7acc270c2bd4ffad8ecaaa5dc66392add8f9bdcdf`  
		Last Modified: Thu, 15 Jan 2026 23:44:14 GMT  
		Size: 2.5 MB (2515479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af140eb0d45857ca8d31db1fd8aa4ea29e7626e3d1ca007a9a01a6acbf971c4`  
		Last Modified: Thu, 15 Jan 2026 23:44:14 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
