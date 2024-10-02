## `sapmachine:21-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:3b0c291ed66c8bfe820b25fbf5625c72ad4d8af66570979357a793d934fcbc2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:62de4d8034f072c628f855bf9b254c17cafa9d72f1f30df436e1d8bec5ff49ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245347502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46effe96c41e37c7d6091d0a1b4bb52d23c87e52ccf99ed99eb1e851d0b5643`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
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
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbd2fba33b9f47a07eeed106b85e07b1807cca4d2d576da95e17c743a95818e`  
		Last Modified: Wed, 02 Oct 2024 02:00:01 GMT  
		Size: 215.6 MB (215597642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7a517099e00ba604a59d5e303501c5ba1e790051fe941fd0fd5e437d72285ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51fb32e2f0e025fe5bacfa3e2f3f857b3eb92e6883a1fc9f8f3cb051aec33dd`

```dockerfile
```

-	Layers:
	-	`sha256:a351c54868c840f16d5941155ddde8937fd044bc92ae109b4de732fe471a396a`  
		Last Modified: Wed, 02 Oct 2024 01:59:58 GMT  
		Size: 2.5 MB (2452176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942dc3685c5311ad10ac855a4828145f69e2f2dbdf8dc545f96fa790bc08629b`  
		Last Modified: Wed, 02 Oct 2024 01:59:58 GMT  
		Size: 13.1 KB (13070 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b939baf7cee801aa747a7a394430c9abd72e716ffc1398a635f9faca5cd67e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242587260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1210c13b9049853d4f61c4a50c3bcd4d5ca71f7cb7b8bb3dfc4faf2b375a84`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
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
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f410376e3ea641c8d322f9d6bcda25406671f32829386bd1c91c532d7254e`  
		Last Modified: Wed, 02 Oct 2024 03:49:37 GMT  
		Size: 213.7 MB (213701830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f393df2dff67988ace1a819bf39636388c5a9f346ba27e34155416282692960e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a028e97f3f8a0aa47ce2b9032eacae5423106a4d6363004c463c65d2e55369c`

```dockerfile
```

-	Layers:
	-	`sha256:f1ea0fb4fdb30bb44c536442841024f3bd6f729017b7c99f8649d4291e5e434c`  
		Last Modified: Wed, 02 Oct 2024 03:49:32 GMT  
		Size: 2.5 MB (2452811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73d7e01a3274a73058b8dd8a88d3ee620ce91f07549b2ea32c80c945c2c6bd74`  
		Last Modified: Wed, 02 Oct 2024 03:49:32 GMT  
		Size: 13.3 KB (13336 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d3e476276ff47e43d5ae1183a82f066e8cb1db03ad709821df77c2133553ddf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251441597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac55f7cd098974256270a54b320518dd0469f8d51b19e6df55e7da957e203dd7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
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
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0928bff6b1e4da21216542e45d22ab1fd079cd88f8e7bb7adb765c59f7affac`  
		Last Modified: Wed, 02 Oct 2024 02:57:39 GMT  
		Size: 217.0 MB (217049576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d33d2eb4d055c52a45c0af2ec87141b28d1c54dce9e01ad482bd636f33f93290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22e81ab4920f1f69375c166f469ce82e30fc43724fcec64ec0d13fb87927615`

```dockerfile
```

-	Layers:
	-	`sha256:b06075ff5d406dc4e015ec7508f5bd0b7dbf49d3f2f35976d1d4760ed2d80040`  
		Last Modified: Wed, 02 Oct 2024 02:57:33 GMT  
		Size: 2.5 MB (2454248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce97dd39e6cd2f48cc3637200852709d80987f99f0635e16a9a21be943a9eed7`  
		Last Modified: Wed, 02 Oct 2024 02:57:33 GMT  
		Size: 13.2 KB (13192 bytes)  
		MIME: application/vnd.in-toto+json
