## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ef67d5514ae3ccefbd9f423af94656ec7bcfe0afbfaee6e0defe4ddd2206881a
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
$ docker pull sapmachine@sha256:ee4a7f88902b920a60bfa311d79d44d927a3543b5d89c3f5ca812cb40e2d163a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84053353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d15026e88fbdad34873f8a13062a2db90f82f818c5ac2fdfa2f693a720e124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7c32677c5fb336c1bc23d24aa7c57d78684fdebbcac11757ba13f2dc827c43`  
		Last Modified: Thu, 13 Nov 2025 23:39:32 GMT  
		Size: 54.3 MB (54328665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3ec33338a06d27b53e71f53f83dd99e0f1d589e03e577a8a3c44292eabe9fca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddb201aafe3f9bdb2e8a43920fa331a602d21e6567e7fa50b38e5cf6c34bfd0`

```dockerfile
```

-	Layers:
	-	`sha256:fc9da0cf6375e5b49c7981dfed4d997db9b729a1ffe40a8589857a5962d33783`  
		Last Modified: Fri, 14 Nov 2025 01:07:45 GMT  
		Size: 2.5 MB (2517386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7997761b0ee1c2e49afbaa3e70f25710b1403d9f9a5ac77c20d00751fa4ca2`  
		Last Modified: Fri, 14 Nov 2025 01:07:46 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:25904cd1cf9d0d8b5064f8e92ccbc509302c7a081448f790e57a67028d6e0b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82614101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0a1cf060239beb12f2fa6598457b3461020b679c0c78a7f61df25265d16af7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:38:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ffefd65fe932382bd013567ca98c24a09e609b8dcf0d22bd816a9a25247e9f`  
		Last Modified: Thu, 13 Nov 2025 23:38:53 GMT  
		Size: 53.8 MB (53752144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:201ae9884316a1a7b71fbaa5d43b52dfe2267b4fbc5916f62fbb8f773e95e164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8789404e748d4bc7259aedaa34a1c12cf455121c92b5a8e05cdd5a6218e6f4`

```dockerfile
```

-	Layers:
	-	`sha256:bd2e3d714d04bd0b6363194a06dfa6941ed930e4538b6d3ea040d68e8e26c33c`  
		Last Modified: Fri, 14 Nov 2025 01:07:51 GMT  
		Size: 2.5 MB (2517902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e7037634d1aecc95dcbec40dfcbccd99bce85adc1b79378f888804969c37ec2`  
		Last Modified: Fri, 14 Nov 2025 01:07:51 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c65e278cd024633c04b4f14695bac66b24cae5c4b7b786468460c8ef3a960429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89828436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1a6fee63947af9f0566db08b33f15cb6e220591ac2d1cb504378970694a51`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:47:04 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:47:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 14 Nov 2025 01:47:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d095e7264db69c71d8ed66436083a20392cbbb632de5dd631bc5d6c2ad8b51`  
		Last Modified: Fri, 14 Nov 2025 01:47:47 GMT  
		Size: 55.5 MB (55524012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d42f83c8bc5f99d199a40f51671aecaae34930a5b005f859cdbbe2e0d285dc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6c9846cc22007347c90ddf11ae27006394987411e9e739836c24d973f3baa8`

```dockerfile
```

-	Layers:
	-	`sha256:c17e7a8099475b83f9404c598eb069a1d9ca31d8e312cac163791e78ebf42c40`  
		Last Modified: Fri, 14 Nov 2025 04:05:22 GMT  
		Size: 2.5 MB (2515467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819df2939eab7d216159720b5f2eb43396e17e51124605ab9e511d3013dedce1`  
		Last Modified: Fri, 14 Nov 2025 04:05:23 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
