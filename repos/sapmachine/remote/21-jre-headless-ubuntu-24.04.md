## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:81237cce419c39a49cec80b82eb079ee5cc89476441cfa7a22a679bd5370e28b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d8fd7db96652922e72db91f96bac93a6aa38ab54947ebe5fd1425e11ae5fc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88846741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f896581cd1f660379d9852010237ad10f45aa3f14fcd89599d6791c82731b`
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
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f33c9db92523acaa27ac6562e59c86087858df90084e8a9cd970e24e617d95`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 59.1 MB (59141588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e537c21fabf635fbd58e6d75b0e5cafde53ebca51646c4987b5754e85822096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e67d0d6b39c827efe13c54e8dc4e66f81397f8098555569d090385811e617a`

```dockerfile
```

-	Layers:
	-	`sha256:232437f512984513abe65b1c23321c1854e8a71a3c574dced9c3e875433b95c2`  
		Last Modified: Fri, 19 Jul 2024 18:00:11 GMT  
		Size: 2.1 MB (2127043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686b51044d30b4356c201f59a682c6975cfd1ee45f19d4d77c4d9556c3d025cc`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 10.4 KB (10397 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

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
