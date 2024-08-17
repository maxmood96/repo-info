## `sapmachine:jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:d13ab01180cd372fb3489edda3d427d1d69418114d4da67831bf5c36cd4ccea2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:f0f47dd21b217ac3afed4845bdb27eb7663865f5ae953ff8910b32b7848e3475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239074160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f840bf60bdd9acafb5fbacd388236b76ab96798d3b79ee968b26191673b7790`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c2a9a2a837596e17c8538352de031181825c5e68490deb474d07c3682652671f`  
		Last Modified: Fri, 19 Jul 2024 17:59:21 GMT  
		Size: 211.6 MB (211562391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a78b5d8db6d2dfc5847dd78a95995a93845bf87f6fe82c4e99cfa194dffc0e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43ca56b37d9f0bb6e5b0edc048c0636ee8d44c52f1dc2e065b44c6c11f22597`

```dockerfile
```

-	Layers:
	-	`sha256:75fe3e4b557d830b5d7b48a3a4710ae12d554bb4af1189d7a2c8449256822820`  
		Last Modified: Fri, 19 Jul 2024 17:59:18 GMT  
		Size: 2.1 MB (2129209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6b652be7adeefefb34eb499f8790294cd98e57bc01a188021d7ff0b79e4111`  
		Last Modified: Fri, 19 Jul 2024 17:59:18 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:69d1603b5bb6cb99afb79200effbafc2723cb7d8fff9674334a4b8cc3785f2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235529738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba2b4c6ab2e004873f2b115c4ee5a6724511b89f2afb8b03cfc09c2b0db60e8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a667c167f05dbcc7d9bba06d6b97827aea75850fc9263fa96ea9e93401d3da84`  
		Last Modified: Sat, 17 Aug 2024 04:13:19 GMT  
		Size: 209.6 MB (209555521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c39b8e21a9bdd4cee751dff0cf6859a856a2b109860daf700e19d0bf0741ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc85ba961138df43710ece27460f2fd68f91165b23161480454bb560c9387df4`

```dockerfile
```

-	Layers:
	-	`sha256:b3b73e2dbdd0cb5e64a6cffa0872403272b92fa8fe339a41a30f8105dec25e1d`  
		Last Modified: Sat, 17 Aug 2024 04:13:14 GMT  
		Size: 2.1 MB (2128229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7be0fc6c1811187a6ad84acd228d16402bb2ccf223d3a52d8b78beb7205406e`  
		Last Modified: Sat, 17 Aug 2024 04:13:14 GMT  
		Size: 9.7 KB (9681 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:28f75c558cbcd177cc013ecb6bb870e9ed149d51be4f3ddfbbae9cc3d1551020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244192764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97209926981e2b6f98629d90fe981aec649fc74127a2e25bb6cd770ed9238784`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:79eeb962c3927659a115eb2f34947c59719c0d4150c5103d23c5a540e94cd779`  
		Last Modified: Sat, 17 Aug 2024 02:41:42 GMT  
		Size: 212.1 MB (212115624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3514eda1a0645f30d480648ea0d84b2c0e3ebf4ef04f2b349f291c98c31f2c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369d1cc5e544ce76c946b86872e089bc920604c5119de27d005e40421ef84624`

```dockerfile
```

-	Layers:
	-	`sha256:884cd616296ffcec6885d9aea13fa99fbc87d025c331e1eb9280b2ef5034e8eb`  
		Last Modified: Sat, 17 Aug 2024 02:41:36 GMT  
		Size: 2.1 MB (2130355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57862c9dc591ad6ffa2974b9134cf79470f0335733ab6786348d6bf9bd7e7003`  
		Last Modified: Sat, 17 Aug 2024 02:41:35 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
