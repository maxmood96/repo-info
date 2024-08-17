## `sapmachine:lts-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:83a5b36fa3f6e99a12389850f691be114f5c50b4a8a2bbf8e196d6e029e2ad9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:9816693d410cae4a5f21b2de850956cd6aa055409e9143e96354e607f8a9ba8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85798258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3aede9024769185bdf23ecbec812dffa6f51d2141fa4aa18f7c536e77003cd1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db10508b015cea2f0275749502fe1d0f35c2d847c44c645967fbae91a2c1ff9`  
		Last Modified: Sat, 17 Aug 2024 02:05:46 GMT  
		Size: 58.3 MB (58286489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:89832a982c10d6c87419c295df06e0fe99636c8eba01954fd08190187cf86734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c22c71243f265e6291f1a2914b970c72c79fa9da97d04dff2dea37978bba395`

```dockerfile
```

-	Layers:
	-	`sha256:36137c626e6930ae785255d473fff30f6c03416c6c134faf3992932fc7a76cc7`  
		Last Modified: Sat, 17 Aug 2024 02:05:45 GMT  
		Size: 2.0 MB (2044953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248933f4dd4ab63dd11046de8d41498fb974cad3462b5977b49673bc1787f8a8`  
		Last Modified: Sat, 17 Aug 2024 02:05:45 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:38c159fe622bd0f3bd364ef0af808e7f74bbb2320fa8fe191be38434a7827225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83356142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7a950cf221ab8818e3209d4f840faa59511491625b54a467155ac94574b08e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116543016badff001297198bf58cc9c17593c3291b831212381e2af2928f3ff9`  
		Last Modified: Sat, 17 Aug 2024 04:28:30 GMT  
		Size: 57.4 MB (57381925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:58eb490b1b64c7e20f869d5febbaf6711efa50dffbba584e40f25e0abeab95a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3832b60f9b30ddeb8b3457c9586c82dcd7d113cb0c374454f2b36a4ba7ede85`

```dockerfile
```

-	Layers:
	-	`sha256:b31639f17df3e71052cf8dde7e3a966b38da5a2277cc82d05cfdcc7c1fd67b25`  
		Last Modified: Sat, 17 Aug 2024 04:28:28 GMT  
		Size: 2.0 MB (2044604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d58c58e6af5665464a1c0fa2b25ff344d9756eb71de6c6d97975b6dce8f68a`  
		Last Modified: Sat, 17 Aug 2024 04:28:28 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4c2f8517c855488dca8aa9b8a3d463417060316a84cdd40b934b104213b74cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91385698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd35f259f4642813f3d40c6e3e0a402cd21eb7f1e70b0645bf34a777c500275d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc22dc15dec007224d95ac8c21f57edb6b117940b15915808cdfb8127ac52787`  
		Last Modified: Sat, 17 Aug 2024 03:06:51 GMT  
		Size: 59.3 MB (59308558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:62c88d63782c71655e25aef54011cc236b00c87f9775183128d9d1c5799ab930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2058090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576f42e76043c7d7356046774663fed6043aa5265a7b3b27f990085c87a7965b`

```dockerfile
```

-	Layers:
	-	`sha256:890029288d5ca8bdf0a5e9493e376fc96b0c56e433e7ab38f74510aa5a9cd6d3`  
		Last Modified: Sat, 17 Aug 2024 03:06:49 GMT  
		Size: 2.0 MB (2048667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5cd2c2d5672911266aa0397ff4a7848f221abd57edb63ef16d215c8cde70a07`  
		Last Modified: Sat, 17 Aug 2024 03:06:49 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.in-toto+json
