## `sapmachine:17-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:bb5aaf950afd4c08f2fbde1c77048756ecc731b45bc48baa478a7b5569eb5c69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:85e28b634360adffdb4db14990736a642dc22a91b0a02d33c3bcff9700f86e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229585885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d913978e83ffe39f3d71a1dd24b052401ed7e0df0e19e4f113c0ab2fee6991f6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd67323e43a3b07f99cb66c5d9c780b874214bd022db16076e8b70b343a87e1`  
		Last Modified: Fri, 19 Jul 2024 18:00:46 GMT  
		Size: 200.1 MB (200051830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd3ce5e629644707248105439fee3a3e1b5082af204d0a60dbe6f5214cdf353f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da6affb3f60d2e30329e04f6c529049cb065c6700984d6cd3b000123be795e`

```dockerfile
```

-	Layers:
	-	`sha256:746e57e60d9f12a8fa187957223da71dc26ca15960b3e36dbd2590735c0fe1fd`  
		Last Modified: Fri, 19 Jul 2024 18:00:42 GMT  
		Size: 2.5 MB (2471217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6a71808061110e57ea6195e0c4700c6970fcf66a87a2e0aa3001880509921b`  
		Last Modified: Fri, 19 Jul 2024 18:00:42 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:283df39199c5aaf390152ec7ef2cd9380d60b23389c9d574d31ad8b1a3060ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225858623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4203db5a71e273e23ce51891b459568306a87c9dbd70e389ffe985260c860406`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b2c898e57b51b1b1921be643c5985408fbd73fe1952cce6d2708d12471af78`  
		Last Modified: Wed, 03 Jul 2024 00:02:37 GMT  
		Size: 198.5 MB (198498598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e503d82df30fa39051898c46bde01baea03f89a556da496da51a53999f24299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753f508be6467a49a8badeb178d67e3b7adf863757c50adca98f5d3742c940ac`

```dockerfile
```

-	Layers:
	-	`sha256:e9c7b5306c55fcae7f6f46741b267a9ada19b7f41a18eb2632bb137fc1f88b76`  
		Last Modified: Wed, 03 Jul 2024 00:02:33 GMT  
		Size: 2.4 MB (2440231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65ac9fdce18c309c5b6c030e3ca914a4343e42aa0bec7cf1993fd38af1294a08`  
		Last Modified: Wed, 03 Jul 2024 00:02:32 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3868a0db37f001206e4be01267d78b51a18ffc02161e8bf05cbcc50d823a2a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235427920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0eb01efaeea34678a9a2fa060415aa408111febf54dd5d660fe42b415faf9e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4b182e9d661a14400a32faf9002fdfda4d1169ce75cde04f94b0d4beb623a`  
		Last Modified: Tue, 02 Jul 2024 21:31:28 GMT  
		Size: 201.0 MB (200966839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fc119e35cf32d03da6146758d8d5e02a9ea6084906480983cd10c9cee4aea810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6224ac77f7b120a31929d9d179193c882cf85a79ba8bac7b2f7aa1be88ab82`

```dockerfile
```

-	Layers:
	-	`sha256:b9e274cccbf4cc110dd0e63908eaee6d2758dc5f4e2ab42255dcbe4d3f3f95f3`  
		Last Modified: Tue, 02 Jul 2024 21:31:23 GMT  
		Size: 2.4 MB (2442557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8961ada9c4bc1b2deba52cf7d6a1e88e8ab5cb57f2980963127cf8a6bcf29937`  
		Last Modified: Tue, 02 Jul 2024 21:31:23 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.in-toto+json
