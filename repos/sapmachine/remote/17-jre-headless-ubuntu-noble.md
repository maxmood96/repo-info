## `sapmachine:17-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:393d5d31f20f1776265289640b1cd41685128b7bd53bef13903d7d8cd2797625
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:7bcc285d074e08a4aef900caf13465d890698292900e54e98c1472b16177fcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85061317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dabce3b56281e86aff12d6bb68fa38215d0dc858dedfaf58ae621ce4af21251`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f823d3a8f08f3323a7fb687b07b2cc63f191b84f39e608a520528f07968251c1`  
		Last Modified: Tue, 17 Sep 2024 01:00:35 GMT  
		Size: 55.3 MB (55311489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0e5bbf24846cabf3c4fdbce130194267cda63d3e7a6b2f77e26e9c5fce3b103a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552861c2fb3cc60a65ba743f023f4b2d6d3c3a4c5a54165d8440a7ed76db5959`

```dockerfile
```

-	Layers:
	-	`sha256:fde8a14b3cce623c7494bd2a3cb8b909ff3e6c005e0e8fd69bab7f7e62596677`  
		Last Modified: Tue, 17 Sep 2024 01:00:35 GMT  
		Size: 3.1 KB (3149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc058665bd2e919e71002cccaf8fc5f19b9981e0f62a9acc80940fb95a40e44d`  
		Last Modified: Tue, 17 Sep 2024 01:00:35 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c813fff7dfd0870af4b68ea1dbbe73347f69e22384f84d5b546bfd80ee2912d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81131865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960159d134e5afec625a0ca956911c355327b6cfb61b1b686af0d1b7e69f4c6c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc6935a46f74314f0b9c948d33f850606669ee9351f14424ca7d7c884411aba`  
		Last Modified: Sat, 17 Aug 2024 04:32:49 GMT  
		Size: 52.3 MB (52288179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9d6b284d39aeb016e4c419e06de52de01df31dd016cd76932058887407702605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2efe0c55a0624b873e2e0d02d4fdae8846180b3f9556803369eb06ded634e86`

```dockerfile
```

-	Layers:
	-	`sha256:9233ae12fdcd7f7a833a65284ba2419039c4c503903dfffad709551e5b91f882`  
		Last Modified: Sat, 17 Aug 2024 04:32:48 GMT  
		Size: 2.1 MB (2124588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20235ab49ed19cffc602c96769bdeeb7ad25f1906b86a8efa2a2bfd686bf2d9f`  
		Last Modified: Sat, 17 Aug 2024 04:32:47 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4003ee5b579fb9bbcc8adee06317daad518891a758fd3213431ca3e50659163d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88839739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a058f9337d8bfa970a038c9ca7a67920e97815fb8c0282835041c07ea8322ed`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac01a6d0f1b1857e89251dcc3e5bf9dbb0c5adb6c489692f1c5a1c2af7d4ed4f`  
		Last Modified: Sat, 17 Aug 2024 03:12:57 GMT  
		Size: 54.3 MB (54332167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ca0c53c924ea662a90ae782e1e7298b5803a7a5a38be50066ff61d234be16c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a0a2dbd6350af8d12813a1784e59df9b267345a1a21135d0cfbcd0ae8d9ddb`

```dockerfile
```

-	Layers:
	-	`sha256:c284fd67a955bb468322be723756a7f1f884b0c6b6b047a58e52d98208a5d273`  
		Last Modified: Sat, 17 Aug 2024 03:12:56 GMT  
		Size: 2.1 MB (2127992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b32985b71176497295fc50e2af0718b567d7828b90b15219f5e425056d62bade`  
		Last Modified: Sat, 17 Aug 2024 03:12:55 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
