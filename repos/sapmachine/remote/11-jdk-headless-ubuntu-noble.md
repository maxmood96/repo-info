## `sapmachine:11-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3850ae0b6d12a6bdc22be9f44694abfe22e9f57a12884f9298b85d95255eff93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:055c04e9bb811659d0e97214fa28fa02cab09234821b91d5ac1464c81a8ff942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232081485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c88390f1164b946d37f57604e3a5e2ec591f2cbbdb7d93c4c85bddeb3a4ff5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecc0fb0ed46f7f72f0c32a3f7bf77ffced367a496b104cedbaee4d1f2d3e6f3`  
		Last Modified: Tue, 17 Sep 2024 01:00:59 GMT  
		Size: 202.3 MB (202331657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b6aa108fb7979602f396736fb5829a415ba2ff2ab2a7c09065ae9175f45ea288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b20d1833a56b1458a83dd7db48328a6b3767846526a35356f0d581fcd97964`

```dockerfile
```

-	Layers:
	-	`sha256:1e09ca4a19fbdc4b3349309ca9a77796b037b8347ae452aa63f8864a792e5b27`  
		Last Modified: Tue, 17 Sep 2024 01:00:56 GMT  
		Size: 2.2 MB (2227638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:febb8e540f3e055bf615123744e91655146255dec82fcfa203e0ce7ea9a88b25`  
		Last Modified: Tue, 17 Sep 2024 01:00:56 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1f9dc825fce1239b07e0a5b6b9af7e12f7313d9313d922689a761c7a87cc487c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227276244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7108efd723e7347671e0a31c254478f508fa679844cca3237db0f27d3126d3e9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c6656fa158ca6d114bffae348f97442eb788cde2b554322d5e0bc617f486ae`  
		Last Modified: Sat, 17 Aug 2024 04:42:50 GMT  
		Size: 198.4 MB (198432558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e9c6298e13f49031b95f350136c252e42d45bf563da8247206011a1845f201e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc29e8f3aa94950df29fd803e2eb37feea107c21fd20aa70ba229e38411f337`

```dockerfile
```

-	Layers:
	-	`sha256:d78df5a1b0d3d6123fbc6e7149e4c2eeb3f439617f7c5a8e781a5a7203ef630f`  
		Last Modified: Sat, 17 Aug 2024 04:42:45 GMT  
		Size: 2.2 MB (2226190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59bdff4545727ccd72c11cfdca9b650272eea67742004b61e9a4c49afe92b52e`  
		Last Modified: Sat, 17 Aug 2024 04:42:44 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:312c37d475e370ea48101aac5a5a46faf04149bc42c3f70cb92933d2919b68df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221031579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd30cca9d33e5a3416fe2580dead7ce93c5ef95a35a0159acd2810b5de32047`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7125b2779ddd966745bed5f88c1a8612f240d99ccd7b313f3122cea81289640f`  
		Last Modified: Sat, 17 Aug 2024 03:29:25 GMT  
		Size: 186.5 MB (186524007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ee96547c73b9101b2dad5c32b9bb56d4d3c3dce766d91ae49bcdd258f97715e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2235807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bc40877931f57c9e298dc00a261a384bb119882611a8425ecdbec32ef9645f`

```dockerfile
```

-	Layers:
	-	`sha256:59e5e22883a14e97ad5a2d08b62879120e035283daf61165eeccb6aa7252fe74`  
		Last Modified: Sat, 17 Aug 2024 03:29:20 GMT  
		Size: 2.2 MB (2226392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7510d2e1a4f1df78d93569e34ba382a4538a530000c93e19e75ffb572c1d8d0a`  
		Last Modified: Sat, 17 Aug 2024 03:29:20 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json
