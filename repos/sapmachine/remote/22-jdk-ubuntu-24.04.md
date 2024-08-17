## `sapmachine:22-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:7ca9b81ab7b196a15fc5964d079efd8ee8f2a07257b38464a4a0c723da5ed2bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:616db9b880b0040811a53bbb05d8fb57b17a70cc4bf61c60c707df378b615250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243324380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dbdbe80ad7019ed769571a594f369778d703e93f76b5d45c1cf593fec47ae3`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d37c1d5d74bda5f284248a9007a99d32fd9befc00092a90c240e9979929cf4`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 213.6 MB (213619227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:412d7a82a40e7d84e35798e4715db33dc33bbd9b6846f1b8b53620081fb86c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af56943a2d6a071c119e827c10a38c6e4b89a989e042081a2d1a972ef1c3e06e`

```dockerfile
```

-	Layers:
	-	`sha256:8b36dc8b289646e34058fc60c62b4111f9708ecb3a98018aaa33161592c6b5ad`  
		Last Modified: Fri, 19 Jul 2024 17:59:08 GMT  
		Size: 2.5 MB (2450190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c527e7ad99b822bfaf10d386d52c8e1444137c041c7820fcd94650a1edbd43`  
		Last Modified: Fri, 19 Jul 2024 17:59:08 GMT  
		Size: 13.0 KB (13031 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6e05ec331552641116f8366a13149ca759865e30191aebf0dbc6676b5d48fc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240454773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0e1b64ea21f3690115798ed7f58e723bb81b3225c43496797011597dcbf14`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfadeeff48aee1833c0bcead3ce70130628740a0c8f0a5679b3e4344f0147c2`  
		Last Modified: Sat, 17 Aug 2024 04:03:59 GMT  
		Size: 211.6 MB (211611087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38e0a738b745d9bdd2ffc93be8635d9c80a85ce5de970e978c2d358e7d94144e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a83787ba32ec24c155485e9b0f533a35998192612c895328987351188fbdc78`

```dockerfile
```

-	Layers:
	-	`sha256:4d1e47032872c88cb2116d7bccb372cce451d8cacc9825ffc7de7dbf2bcebc7f`  
		Last Modified: Sat, 17 Aug 2024 04:03:54 GMT  
		Size: 2.5 MB (2450194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b292c145fd4ab8f40e9e6e0528f0002676a27935a99da5a77e611438ab38a5`  
		Last Modified: Sat, 17 Aug 2024 04:03:54 GMT  
		Size: 13.5 KB (13498 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5665c3b0deec567a01e4db7222571dcd1c393ead38907eaae35ce93f045bb4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249346449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c92cd2bfc52a4f690423ba4c4510df343cee55b8a01074e85bd46f707198cb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9532c4c5000556df154a237634817f3c1c27c39c6d8ec47c69390d07b795c34f`  
		Last Modified: Sat, 17 Aug 2024 02:25:41 GMT  
		Size: 214.8 MB (214838877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0960389cf4d88fbdd26f532032c75fef2a321369adde25c9ec7c802cc346d872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfafc0a42b016e05f7dc35139b0d7a4a824510d56168037b27912c7520315aee`

```dockerfile
```

-	Layers:
	-	`sha256:30bd6fe42a5fa9fff576071f5fb3ca47d21309199fcbda0ffb89014208fced31`  
		Last Modified: Sat, 17 Aug 2024 02:25:36 GMT  
		Size: 2.5 MB (2451643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0029575b62885662a2bd82cf2c318f43e71faca1a3ae662396d44d75b04132f6`  
		Last Modified: Sat, 17 Aug 2024 02:25:35 GMT  
		Size: 13.2 KB (13153 bytes)  
		MIME: application/vnd.in-toto+json
