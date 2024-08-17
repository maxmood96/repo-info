## `sapmachine:lts-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5455243176321c8d46f9e20417be127830ed48351863df98d3fa678f0f86fb6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:70ac926c069c49d8a25011f8394a09b38ff6a931199582be30f100c5f7a17b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88847859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d321e252c6a0328c7a72f3dfb31afb21e578fd6ea7e48f32668fd0e2f09fadfb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d78a89a805010193e2582c2435291856b8a259a19dbcaa5b4be30007a65e5f9`  
		Last Modified: Sat, 17 Aug 2024 02:05:27 GMT  
		Size: 59.1 MB (59141561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:619d5c1463baddb95316a34dad0cd061afc4112d41dfe9ebd5d999ca5671b6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527c7c951e1cef6f6925e97174589f4d49345416869e36fe6c8562f7df71accb`

```dockerfile
```

-	Layers:
	-	`sha256:1b8baf1d621d0126f8f1539dc511ab95a19a0477b746c2f49bcdd76ff6f4d341`  
		Last Modified: Sat, 17 Aug 2024 02:05:27 GMT  
		Size: 2.1 MB (2127043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8e2039d82cbe4d4f1bb9b734245ebf63a611b6fa4551af694a1994378e2b4ef`  
		Last Modified: Sat, 17 Aug 2024 02:05:27 GMT  
		Size: 10.4 KB (10397 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:64916964f06f0350cf48a648423505d0103deafd943a96d1f1776b2591af269d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87086195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ffb2858d14041de9a2eede18a6939ea0b0dcb6b98597a564a6ae8331c309d9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f445d8a40d3d442db1ea570bcb5aefd0d82fc44c41a2d209ac8275b6d9cd02`  
		Last Modified: Sat, 17 Aug 2024 04:19:04 GMT  
		Size: 58.2 MB (58242509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ff611e31d09df97cbe0cd1e8bd7c5abb8910abf195856df731540d7424891169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b6b6dd1faa00dbbf494e7b6554e308fd75221f2c90dedc41a77444931a0809`

```dockerfile
```

-	Layers:
	-	`sha256:141957838e2a5e4806555e157e9c27f456ded59ab019cfe5e7f23d297022986e`  
		Last Modified: Sat, 17 Aug 2024 04:19:02 GMT  
		Size: 2.1 MB (2127561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9dc7b517866d2636af1fb2d1fc4c14af9bee2df620fbe0f53583f8ffe41ad7`  
		Last Modified: Sat, 17 Aug 2024 04:19:02 GMT  
		Size: 10.8 KB (10758 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:084e2e6aa205644efa89843625370344fe9234dfcf1a11112c86422a7eaca2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95142789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1946adb0d0ffe3a7fe97c9efe722deee03d8bfa9a5628330aea11c1ade1747df`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
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
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2427bafab1cc1a6d82872307b4ff5489c4febc3f53fe22bbe12b0075e5b9adda`  
		Last Modified: Sat, 17 Aug 2024 02:51:15 GMT  
		Size: 60.6 MB (60635217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec9774074c0ce08e93433d94131d457565e5e255d137303a752687f7e7af9a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25da7d0a2353e307450179e1f4cbbc8b1df95b4058d909260a25f6faeef0a097`

```dockerfile
```

-	Layers:
	-	`sha256:9a46a664b4cfa0ffb8d58b41b6acf1e21d5ce51a0e49445957d3c51f4b4a03b7`  
		Last Modified: Sat, 17 Aug 2024 02:51:13 GMT  
		Size: 2.1 MB (2130947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f4f0153c3bff99fbd2f36810dffecc1c4a42987974e80802e9bb2437d758fc`  
		Last Modified: Sat, 17 Aug 2024 02:51:12 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json
