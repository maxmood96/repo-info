## `sapmachine:17-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:7866ac05cacf99e302bfb13271828b9da63a851e593e144222062e371f0cdfd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:4b3d1190472cd18e4ce185eb318eca9404d806dbe9b9d2575ed94bddd68c3f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82608936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e3b6a34c0e59a4a20a9c58f15b3317c21a42a306138cb4704ce6152f0ac265`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ec5443365884feef2e12ffdb8b72df371aebadd206cdf1ee2cef7b84591a40`  
		Last Modified: Fri, 19 Jul 2024 18:00:07 GMT  
		Size: 52.9 MB (52903783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:609c43d2370d18ae65d3066cd656463ce4113ac601ee3f7a0677c640c3f5b0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b62332643458b9bdbf1ce1a517dad9b874290766695ccc8bad0b2b0d4c69a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7530b3acaa8e67eeee22ed234b60b293ff400733d334d83267b321abfb84aaa1`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 2.1 MB (2124106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602fe895e275ef0d60ba85e0ca3da1d8a83fbc45211746b2783e86bc61132f4e`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

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
