## `sapmachine:22-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:8dae11e91e52c18ae6d35fee0a73f44a91f3debac1c1822ce9245a410f56b042
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fac65591d53cb92b87dedf9ea576fa6a3e3e66819e5346ac92a83d5aaeb9cded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239264876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b88604996a8135bdacd73e39b6ea66371af148d9db5454d91576b8a8fb05093`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6023714ff61511c802cf05f56fae870943618dadd7732ac29fc67a30c43d1d7`  
		Last Modified: Tue, 25 Jun 2024 22:59:14 GMT  
		Size: 211.8 MB (211753107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b8e2396e628c0fc6e436d830aea84d0f63d5a930f8ec661313975523a8cd36d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2114366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f22fc05cafba631dd68234be26fb4b9afec260c0979757b0f93b7e8aad247c`

```dockerfile
```

-	Layers:
	-	`sha256:d29b97247e240449f308fdc42dea7ac2aac3e04aae04c9923c49cf0a1127ca27`  
		Last Modified: Tue, 25 Jun 2024 22:59:09 GMT  
		Size: 2.1 MB (2104990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718c528eeb719cf32472959da7165ab42f66181f5a6c8d6b70f4410bde451b55`  
		Last Modified: Tue, 25 Jun 2024 22:59:09 GMT  
		Size: 9.4 KB (9376 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8c25a1bd2237b75511181b25b5d3d86df1a9dcf8ae69b64e2d2d69f210e9183d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235694706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f11448230842c1a503a1c29e67f0e804039fbde6d9ea3fcbf75a16f80a43354`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eaf5e213338ecb76d0eb5d57cf2408354448369f8b867507894a91a49cf21a`  
		Last Modified: Tue, 25 Jun 2024 23:59:59 GMT  
		Size: 209.7 MB (209720489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4a52f3e0d1ccb042a1ff007a0e895915be46431f11c746ce18d907ca584fb2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2113711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e0341b4d77736e303bacf5b1f7f25b020658bf0548fa2bc8394ad343d40dea`

```dockerfile
```

-	Layers:
	-	`sha256:7b8ba205476445855dd459d43dfe3adcac0d93eaf01752c261642ef3c6854864`  
		Last Modified: Tue, 25 Jun 2024 23:59:54 GMT  
		Size: 2.1 MB (2104010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70d38cd7eb8bb2cd6cc6fcb67000c5d3180de0260ce961b17749314c49bc4c9`  
		Last Modified: Tue, 25 Jun 2024 23:59:54 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e1377c43768802fbb9f29b710e707898328d621b28e6b043b3b42f97cc861094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244360658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4e426df87d6332f62703bb1e7345dd2cd93b9c61d605355e4b7fcae578b91d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6db62ad3abc99b0974bc5db4898170eaf0f469481ff05ef4f34742eec37429f`  
		Last Modified: Wed, 26 Jun 2024 00:22:09 GMT  
		Size: 212.3 MB (212283518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:34dcc474b7c327dabd58de4bc1050627ff591a7bd5d9395af1bbe57611d6f37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898cb0c2d751a80a7c5063d63305c15fcd0a2f0d2ad6d56ad549b68032b94b6`

```dockerfile
```

-	Layers:
	-	`sha256:ae64ae1f67ede39ff77be75a6765e4d6b492272a85775f5770640f5e5e99fe4f`  
		Last Modified: Wed, 26 Jun 2024 00:22:01 GMT  
		Size: 2.1 MB (2106136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2800cfe5659e6f8466b45c5e5bda13712d2cc71d7f0fc10068403e370af0c607`  
		Last Modified: Wed, 26 Jun 2024 00:22:00 GMT  
		Size: 9.4 KB (9426 bytes)  
		MIME: application/vnd.in-toto+json
