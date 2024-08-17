## `sapmachine:21-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:73b7ef83c7a812eb7f9ee42d94fafa3c01da40889c3db27cb9e14756af3e7887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:0182fc41acdad483c6cd6e9c2145bf812e1251d6e46a98bbb06daca8c5fec9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242271851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be293172e849e5103da08a60fa9a8e88e8065de991be42a4b338ff29ef96e9c7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e3da201d53cbe4fbbcaa4cc02f44e41d492628732b518c938af4253c64b2d`  
		Last Modified: Sat, 17 Aug 2024 02:05:57 GMT  
		Size: 214.8 MB (214760082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:86132e52205306a043760de158da014f672b2a07152deaa6e37c4b071ac7fcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a06c8953d224f569414d0a1f0e88e0cca93e313641e94a294b531c30e015f0`

```dockerfile
```

-	Layers:
	-	`sha256:5560f5b9fc1e51032038f1d423afef5505255bfbb165dfa7373040557d0df039`  
		Last Modified: Sat, 17 Aug 2024 02:05:55 GMT  
		Size: 2.4 MB (2367821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9e5a94e1f01463816406d71e388dcd93ca406e54376811f642efc15758e3d8`  
		Last Modified: Sat, 17 Aug 2024 02:05:55 GMT  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:40f0e6ca4b4c354c02e73668a5beb7e850c62445e125b75e78482e89f27ba2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238812667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd42a795454a6e3983617cc422b0918673057536b4eb67622d012d20b4588c7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:225bccd4dcf0c36af309c183b56703c6fea3698350be819fd5df57daf7154bc3`  
		Last Modified: Sat, 17 Aug 2024 04:24:32 GMT  
		Size: 212.8 MB (212838450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c8adf65b80b4649aa088baf4923d0adc8ceaddb25556472dd6e5208630ee3f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b3dba9a4b34a086ac4497f176dd0e7018840d9b8b514063939de7e3674d135`

```dockerfile
```

-	Layers:
	-	`sha256:5d0010eb0e608e7edb8911b0dabef2a6e41c1e4283a9c90f189439caec5774d8`  
		Last Modified: Sat, 17 Aug 2024 04:24:27 GMT  
		Size: 2.4 MB (2367553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b89214cf66bae6775070087577baf77fa49393e601d33db030faed41e98add4`  
		Last Modified: Sat, 17 Aug 2024 04:24:27 GMT  
		Size: 11.6 KB (11588 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:46450dca3b1f23fd7021005509e2934e425afcced75bf858fdc7591c9c8e5424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247780341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6a71c9c6f371482b0aeee2d31a4d85e2e977a94aee222a5705f357e76386ce`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:646f16bcac320501fcce1526c7761406602c54a202b49b78763d55fd1d4b03d1`  
		Last Modified: Sat, 17 Aug 2024 03:00:37 GMT  
		Size: 215.7 MB (215703201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6afd746ca2c1b1d031bd6d9fd4dd64cd4816300ee45f9802b91c8a004fafd534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a53d99f734fc47b4126708d0c5d621e5d532f408e5c95f43e8ed92b75caf8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ba135a90a59f04b66852d501a17c8d79d96366602c79d56eab20ff6d47a3a28`  
		Last Modified: Sat, 17 Aug 2024 03:00:30 GMT  
		Size: 2.4 MB (2369685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f565cdc94f7dc1fa36df483ed13109e90659ddaff9a5c53592429710bdbe35`  
		Last Modified: Sat, 17 Aug 2024 03:00:29 GMT  
		Size: 11.3 KB (11277 bytes)  
		MIME: application/vnd.in-toto+json
