## `sapmachine:jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:013f7e96c6c6b1402fc3433696f13eaca0911ac1c1f79c7a9d93ae70c932dc33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:1f5216e61ab4fb65fee004386eed91f2375d5546c34bb367327faace57ea63cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84988660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b9d565fbb1cd5eed855c8d600d7178f27977950398280c7cc5417fd9e745d1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f052767a95b07d7479429dd0d2ed15833a3fcee1497eab963011f36583e7066`  
		Last Modified: Fri, 19 Jul 2024 17:59:16 GMT  
		Size: 57.5 MB (57476891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aef87b3054837809d8c5f7ecbe803a91cf782069e4a11f036b417fdc20bb95bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25cd9c10d69beb4ef2015b659c31627cb992e767bc1e9c3ad57f6003b6a4991`

```dockerfile
```

-	Layers:
	-	`sha256:889981fb3ad554be47169c7adce34ca492b93fc7e29acf4cfab012ec2b88dad4`  
		Last Modified: Fri, 19 Jul 2024 17:59:15 GMT  
		Size: 2.0 MB (2045568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aec8986a0d1ca64b756dc791116f62087a92e5a88c0f9d2ea4715506ebbf5ce`  
		Last Modified: Fri, 19 Jul 2024 17:59:14 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ac0d2fa345b5668dae7d74cd519658d32f8dd217bd829cae70933f71d635e6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82490162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa3676f44e27f88ed11ed485954112835f8602bbe4b745ce931152201244cb3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1d4753966ddf9c1cd73278f8ca9e6ebce44684810ef841f3a0e3bb7d927f7d`  
		Last Modified: Sat, 20 Jul 2024 00:07:54 GMT  
		Size: 56.5 MB (56515945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eca418396e58978e3ee0bca3c153163a8508f3f4ad4eccfb2c30b6cae11cc8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d873f103e0ceb61260ac52b168b53998d9c4927a017d2767d65b157ee7fdba78`

```dockerfile
```

-	Layers:
	-	`sha256:74dc760f6fb3f1635883f0288e8341b9b28def5188ba9bf296e34a11b1b0e033`  
		Last Modified: Sat, 20 Jul 2024 00:07:53 GMT  
		Size: 2.0 MB (2044588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c1f320f6d1ebcb4a5bc01a10732156216f9bbc493b6df71a6acdf1ef536bf0`  
		Last Modified: Sat, 20 Jul 2024 00:07:52 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bbcf996aae54f414ecefac69b3ba73b66c88758d26417ea124d96818f9cd1d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90446970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ec2e331600bb97c7d1ad1629b92dd8b794ecb41614fc32dcf6b8d6522a69df`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c36c8fdf10b97a86533f17eccfce6d0ba861e2276e6158c1c6c5583a87fa5c`  
		Last Modified: Fri, 19 Jul 2024 23:09:47 GMT  
		Size: 58.4 MB (58369830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9652f0e218d7983f233ff805ad8679b3d8ca5228aeafd6102de863baefc25136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2058058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3a19703e20f58e77df5a04bb56b1005487ea5d8e5099f8da5a431ba42e07ba`

```dockerfile
```

-	Layers:
	-	`sha256:5c814426034b33f54ef67fad9192e77a09a57f72399d9f0e443d24965e215617`  
		Last Modified: Fri, 19 Jul 2024 23:09:45 GMT  
		Size: 2.0 MB (2048651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef63e520278dfb0c94b5809396e2a50cfa71dd13271d0ab9d0f7de93b22ca661`  
		Last Modified: Fri, 19 Jul 2024 23:09:45 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
