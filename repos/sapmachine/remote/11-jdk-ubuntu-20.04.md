## `sapmachine:11-jdk-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:7d1818e3bd62ae13cf30e10eebe1790d898151f52863cb91518689bdd4c51dcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2566ca7a9841b61064d0cc2dd2321f96da9d9cab6d6552f3a74cc0ac89fcaeea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227794719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af86f42b2654dbabf75652764aa148c77fc7fe02bc6138b362c048b994ab9d39`
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
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a120efa7584cdf21b6fad6334ade663aaf0186d7632bcccec0f5236e8b4fb517`  
		Last Modified: Fri, 19 Jul 2024 18:00:51 GMT  
		Size: 200.3 MB (200282950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dd673bfb6a247a470c2723a278a96551000f4e831a20b644e98788d64138256e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2231090864064fdc0d4f482a4558d560eeac84aabf64fbac9a67479d7106b1b5`

```dockerfile
```

-	Layers:
	-	`sha256:de23ff95db20fef07f328ae8159653fbb56ba47b8c0a9ec987d0313650722854`  
		Last Modified: Fri, 19 Jul 2024 18:00:45 GMT  
		Size: 2.4 MB (2381931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b9d7684d2a1b0cdac02776b49af930fe35db361eeae2dcf935487ccba626ce`  
		Last Modified: Fri, 19 Jul 2024 18:00:45 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:16dd5c8e50cc30589143708ce1a916fbd887fe0e2f3c7418e6cc2350c76991b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224742700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a4fca7677f0f11d069d9d8af9275a62c30916cb0a11dda1a96913dda1b7327`
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
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0670172a89d1a15be0c235536b84ee3aa63e7d266e9819f62b4204defce49ba`  
		Last Modified: Sat, 20 Jul 2024 00:41:49 GMT  
		Size: 198.8 MB (198768483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7dcdb03c1b81c493ead0abb65d4f7f28bdcbeefc5220c6990be4f7df9dc9ba94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625e5507424fa3c4522cc34382d5a3457859a4c435ebbd4b00176a1ba28f4423`

```dockerfile
```

-	Layers:
	-	`sha256:f3e59aa36f8094b558330f498ce6e48bbed662935793d8b6e7559b0cfa457790`  
		Last Modified: Sat, 20 Jul 2024 00:41:45 GMT  
		Size: 2.4 MB (2382243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89da3ac0e639e9a91575e5af7ba2d414b76aa9a7f44377dfa44d28e845082cbc`  
		Last Modified: Sat, 20 Jul 2024 00:41:45 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1cdaab3cb26a7b884ed97eecc0778060ed3521bf5553a7238ce180e2d02d33da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218626023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86e57ca87935bc44c8b9a6b4186c307a378b6430b1eefb343198ffef9bfc8a2`
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
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258f80864c1ec48d9c260ffe0aef85eeafa2dfd8345e82bb250c51141a5cc6fc`  
		Last Modified: Sat, 20 Jul 2024 00:04:16 GMT  
		Size: 186.5 MB (186548883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:606ef05cd119f5f1b582500bbf1d09e9d0c8f42ee50c1a18a8d70e240a40b8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb1ed06a1b167ca1bf87ed5083d820d7406701a039693ea6f7800e0e9c93853`

```dockerfile
```

-	Layers:
	-	`sha256:eca0ac4cc9680d5d5c4b9ee1a479864915496a77a1a2f7c7a0ea7a13412799c8`  
		Last Modified: Sat, 20 Jul 2024 00:04:10 GMT  
		Size: 2.4 MB (2383146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8217edfca602aef2547829c5f3fab3912244cc0e737d9279a923500233619fc`  
		Last Modified: Sat, 20 Jul 2024 00:04:09 GMT  
		Size: 9.9 KB (9945 bytes)  
		MIME: application/vnd.in-toto+json
