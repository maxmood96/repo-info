## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:31c797d2f7961d660bc68aa5cb0fa8de6c7b7e2afdd019b3ede7ac2052e027c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c5ef0df8d8ee798baa913a6812608a5fe73ada3953ba3c812e6c16eb1f5efdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243394747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdc32d8747362c1a30a98e1eff71957d0c215b36bcaef7d6eb5d4293cafde35`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d160000b94e6a2b24bf11a9e5aa25d02d3126a9694b7d34169b3d3fe8a655`  
		Last Modified: Tue, 02 Jul 2024 03:32:12 GMT  
		Size: 213.9 MB (213860692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c9daae1ad6b2c1bc6b5dd464b5182d5d6b102cdd3ab49431b2ec197b6f51554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c6360040f8c68176d22deea3195ace077a5e980b5428c1b49d20cf0fd9f1a`

```dockerfile
```

-	Layers:
	-	`sha256:5b2b42d30e52fecf89d9a417c6ed8df56bdd0b28871a4d1873561372487a0ca7`  
		Last Modified: Tue, 02 Jul 2024 03:32:08 GMT  
		Size: 2.2 MB (2204375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c0cc09f660cb7faf35499a5b7ab1d5ef20a25284d0288bb1443cf10154681f`  
		Last Modified: Tue, 02 Jul 2024 03:32:07 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:834427b31c285cefe8cfb232c8779eb9ac9fbc477133a1e781a9fd0dad9a5f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239268181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa37410d575ce7da1542bba013a4152051f16724719b2ce6d5beb194b01eb9a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22c20abd463383fcd096f33708e463f18c5ba7bd7dbc1f865eb278878cfa6f5`  
		Last Modified: Wed, 26 Jun 2024 00:08:06 GMT  
		Size: 211.9 MB (211906399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99509b487e51d8cbf77599f03ad0e4b0eba75ed7a4778b3ce674f0b19ea50fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e919f01a87fd35e9124458f5d15a4f85d1b864d50c210e0fb14bb9784c25af`

```dockerfile
```

-	Layers:
	-	`sha256:df528925196af3a1a9efb977074aba0d00749cdd64f994046b84d3d0b8900b74`  
		Last Modified: Wed, 26 Jun 2024 00:08:01 GMT  
		Size: 2.2 MB (2204069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24af71df72c9daf786a65038f146226e6bd76ed047f171bfd3df60fb8056d840`  
		Last Modified: Wed, 26 Jun 2024 00:08:01 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7898754b8f2d15773bb228e6aa6914531e4d08dbae6464cedd5d7946532c8a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249462696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731173d43dcdc83671c1bea2a5cdd680cfd5ee2181bf85a60675853bca085954`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a738af18a2008e0390cec80ad3b8a5171bb8c9e1d58c1a41ecb9425ed81844`  
		Last Modified: Wed, 26 Jun 2024 00:35:37 GMT  
		Size: 215.0 MB (215002003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4de502d1f607ccfa96bd2310fb7e6d989444e0923c390ffde74cf373f9c656e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68d004a027357d988b1a325016b4ba5912df0bf9b4f187d1ed7c98369c4ab97`

```dockerfile
```

-	Layers:
	-	`sha256:ecbcefa1639569e5f5021c6cd9ea7c8968edfdfda009c1e650952f41c777b824`  
		Last Modified: Wed, 26 Jun 2024 00:35:32 GMT  
		Size: 2.2 MB (2206347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a86e7df04e15b05822c94743bc6d3024bb21638065281b37dafe53cd9a0dc6`  
		Last Modified: Wed, 26 Jun 2024 00:35:31 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.in-toto+json
