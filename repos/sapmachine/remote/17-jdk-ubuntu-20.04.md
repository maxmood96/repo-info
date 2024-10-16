## `sapmachine:17-jdk-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:0ee4ca1d2fde0dd384fa3337fbb8dbd03ce101a7e7ab972e41df71b854ba45b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:03fa9291cccce6373078ed172ccd395dcd4b17f384c01644a458c41ec73673ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227109021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c674cf83343dccf5534c528369820c88876b67ce4852e681f9d174f31a7247d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae5097f94bf770f1428d34eb7852c4eeb97a25b14d5a567614ac47d2fc9d85`  
		Last Modified: Wed, 16 Oct 2024 16:18:30 GMT  
		Size: 199.6 MB (199597961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7d51fd4ca6f526b4b98de6ec2bcf26e71cff2fa5409c90b7bd917a604f7dabc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6a4006ea397ae12aa72fb8bc56514e36339275a8e82d35456a77b519d227e4`

```dockerfile
```

-	Layers:
	-	`sha256:2231acc2672f042adfcf5433897f633ec8a3d9ec6045bcfc7d28255d57a182cc`  
		Last Modified: Wed, 16 Oct 2024 16:18:23 GMT  
		Size: 2.4 MB (2364009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ae4243ab9fd879da8c03b5756d0105ef2ad9a6b807bc3dfbd7732298f64462`  
		Last Modified: Wed, 16 Oct 2024 16:18:23 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:60db8af7692aa243ba7d253880b598381c1e29801d396b6a4c640abf31441a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224193545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e0a5ef4bbb5a52cda4b6fdceaee36ebcde7b85dfb59195ce31fc43430e40bf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c979cba86697b68b4a6c26c5c937c6518377e222d84fd7f00b5e340c338e58`  
		Last Modified: Wed, 16 Oct 2024 04:42:40 GMT  
		Size: 198.2 MB (198219717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8ea24d223515276a312c1b3d58ab38a5024671c239557e7275699965e5b7add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198614ab2d4fabf199d4d718f3a4ef09f947d4c27c8519d714d3ff2597300248`

```dockerfile
```

-	Layers:
	-	`sha256:a6d34c04ed225c86814ae81de4d73c6e6d9bdaffd8294fc59c8ccfcd3759acc6`  
		Last Modified: Wed, 16 Oct 2024 04:42:36 GMT  
		Size: 2.4 MB (2363693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813ca5874919ddcca6ace45c7dc5ad865ba36df7b305f846815dd90fe723efc7`  
		Last Modified: Wed, 16 Oct 2024 04:42:35 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c9b68046200ca4e40b65f1fe909826174c773dcac6e7457d342bbb330752d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232363314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfbb47fca5182c2a570e392b959db3f3b4f805dee30f81144a93fc0d2062ae5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a6c49495a3009db137cf141f4c6262cbe134a50809aac40919a5737fba3f8`  
		Last Modified: Wed, 16 Oct 2024 03:03:43 GMT  
		Size: 200.3 MB (200286808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6bce7332fb7b2eeadaacc778b7d0877986039cda87196dbe8e8bccdbd52219b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15380992ca60d1a048c19f6eb85a5a83a7bba333adf6cdead345131cdce91048`

```dockerfile
```

-	Layers:
	-	`sha256:5c5d4cf3433371786f86c00866aed6504e647d0e22ee3c70278417b20672d16c`  
		Last Modified: Wed, 16 Oct 2024 03:03:38 GMT  
		Size: 2.4 MB (2365849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fda4029c1aab95c121e813bcb07799aa1834d1d9508f589559964292cb3f1ce`  
		Last Modified: Wed, 16 Oct 2024 03:03:37 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.in-toto+json
