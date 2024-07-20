## `sapmachine:lts-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:6de1e39cde2e313ce189a180bf2c4286719fcee7543d1815d806d226ca669b78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:481e6280ce05a63c9b0c366c626db65e009c1ab80f3f6b9381e928b51a4bcb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86998429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ad374fc84d5b4b8936f9e807e5afaaa5f2f536a8a7b5b8facee9274ebca07f`
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
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe10d8ce2179aa9d477af97bfef33a1eddbccb68a4a321530fced5946aa6635`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 59.5 MB (59486660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f279a2efaf04eb1f1e36cfcedc6c97e9ccdbe1ff9e888176d6dcaf1affc7d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbc26cc7e58cf86687c490990eb0c0fb421e32b0ac7ffab0b880c3026333f52`

```dockerfile
```

-	Layers:
	-	`sha256:4c12b91bdfc12aa6f3115a2484cace9e7537692390dd463ade905a8e7310ddd6`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 2.3 MB (2282204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b3d29ae586fc5d346776574d2a3e73371b5d7cbcd7b6f68c7d3eb61c412246b`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:de846fe5c8ba97fd912e6752d8ba73ff3fd0f324298c0fa73cc6c7ca7a53464d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84555122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d13290acb459c0177ab7c6f968c43810bce1d76ae6c021382672d55cdf7084`
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
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1f57f5d20b69f9a8d82547942bcee5c8da06451960fbcf6cdc6ddda8f96571`  
		Last Modified: Sat, 20 Jul 2024 00:19:32 GMT  
		Size: 58.6 MB (58580905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b5f6f963b9d27b71dad1ab61bedfee2aeddbeb5edfce79d240df48c8d413285a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83f68b3a3c62aa80e6573c0eb188598a55e28ef89be8c696eae3cbd300a29f1`

```dockerfile
```

-	Layers:
	-	`sha256:f01dfdcd681c3976843116cdce241ee4e43c7bfd347d04c02572574836fec1b5`  
		Last Modified: Sat, 20 Jul 2024 00:19:30 GMT  
		Size: 2.3 MB (2281864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f86a885195eaf4502c5be4bd299487cdc54a261afdf623e3b714397fe4efdb`  
		Last Modified: Sat, 20 Jul 2024 00:19:30 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e6e078c7f31edf22b2bc5432b2cb68896fc34a7562f1dbc6762b9ed99e5e205d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92748432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b54f72f42e8181ba4d84264a29e7ba3d1f93cdf8be18dec00d0037a4f00cd2`
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
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3f23b07d47f7f749823dfa559b3a951215317151b08e8417759b182d53b3b7`  
		Last Modified: Fri, 19 Jul 2024 23:28:19 GMT  
		Size: 60.7 MB (60671292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b93808d5e9a41510f4824021d1dc1581bee22e133865d36613fb03ab51289437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef35d865c70de3b6a55fd613de8ac25661e78d705b93ab68e96bd89e42b3d2`

```dockerfile
```

-	Layers:
	-	`sha256:a08194551dac1073fc7a3f7486b677fb5b850cd39a992ad50e76b404daf4966b`  
		Last Modified: Fri, 19 Jul 2024 23:28:17 GMT  
		Size: 2.3 MB (2285981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:889013efd485e7cc6441e9c7824affdba6cec314274a4c948d8bdad0f2038f80`  
		Last Modified: Fri, 19 Jul 2024 23:28:16 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json
