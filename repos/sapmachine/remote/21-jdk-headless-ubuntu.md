## `sapmachine:21-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:68d281c2f51df0dccde4b90e8efe6cf73e0f758102dd62e306c7c842e2960f41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c194133c30066a9f4e4990949b72b571efa3b44a2efa00dd0e6d84e34123cc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243898740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259d28cc84730cd2c36daa1878a86bd689a21e7b13482e058c78d11235bc7bfc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe1d07a3b5cb3f86879b74bcd964b3cbf1beed26174dd67aae4d99338d7854`  
		Last Modified: Wed, 22 Oct 2025 07:33:48 GMT  
		Size: 214.2 MB (214175593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4f2ec67bfcbdc9316fe597d3250a67f8b95721a49fb9d7c8901cd48670cd869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc030175f5f608f5cb1f52f240c828a926e5269a73233f88332f15d0a7b6e5f`

```dockerfile
```

-	Layers:
	-	`sha256:db20bb12b385275b3fa0d48394d32cb7e0589bcec834de90270daffd15156a61`  
		Last Modified: Wed, 22 Oct 2025 06:09:57 GMT  
		Size: 2.4 MB (2356331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01530f22f15772173a08ff2a43bcd26f4066d86926165bc39558dd41df9084e`  
		Last Modified: Wed, 22 Oct 2025 06:09:58 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8eba0f005c87fef14d7e77e0d6fdbebe01c57f3df477e6992db0ac840a7dcaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241277249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ef6c64a8c50f7de8f74313306b2adc7dab972bcee70afc53235f91473883ac`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f43ac5511a77c025d6ddfd43d06c2d0e036b85a74f638e11d889afead1e191`  
		Last Modified: Wed, 22 Oct 2025 00:05:36 GMT  
		Size: 212.4 MB (212415537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0911b7393f8ef4d25be89807ab1ca4b9d668a2438007e6f124274a419771ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab58e30910e5a85222592d52def0f238a451f1bdbc26d27c8fb584876ac0ebcd`

```dockerfile
```

-	Layers:
	-	`sha256:8984c494681c4384c1ff0c9889e46a7f2e4ee2f9f50057793a0086501b475d60`  
		Last Modified: Wed, 22 Oct 2025 03:07:15 GMT  
		Size: 2.4 MB (2356838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f892106b4993b5b66f7a95eb7e428f6d894652314ed8eab16c95f8e8bec4ceb`  
		Last Modified: Wed, 22 Oct 2025 03:07:16 GMT  
		Size: 10.4 KB (10416 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3b0500a47a7babe7be32b8a17fec9b6683ccd1b68ba899684f0ba4fee87724d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249224261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e80811210f75370e9a10c5081a276db0a3bb49c7929c384d99278c9c73ef14`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167a6fde701a50fb92bde38568b7fe4227ffe080d87fed9250b65f078550e1de`  
		Last Modified: Wed, 22 Oct 2025 11:48:59 GMT  
		Size: 214.9 MB (214920736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:487d79b191cf03c4cd95b9ae5be186986fa173316c9556148d2d46e4fd0c0fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae07ba94bcb8f41bd4b7cad8ba4f7d17a3a51da7a67b3fbdef8f1284ccc2a65`

```dockerfile
```

-	Layers:
	-	`sha256:84eef12e521effa74f4a880ee44bb0c948a96cb712d5623c449167a4c6cbbd21`  
		Last Modified: Wed, 22 Oct 2025 15:07:27 GMT  
		Size: 2.4 MB (2352385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0266f172cb1e58b9ee0a7841e481ac9d7d8ec7f2e8cd2f6023d485aab742141`  
		Last Modified: Wed, 22 Oct 2025 15:07:28 GMT  
		Size: 10.3 KB (10332 bytes)  
		MIME: application/vnd.in-toto+json
