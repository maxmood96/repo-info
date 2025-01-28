## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5c0fd5459ca6d43bc81c321b77007396dc94d96243094badf0310e841cec16aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:77cafbd1cb54f21609ba451f40a9a30e494557434e7dbd4452f896adcd28296f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228868279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8acbaaa7622ce390f9353ec952ce7137042b4fc020130fc219144b6166852c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2088593b9da334c154167c461ca37195ab5c3328caeb6f5decba2974afcc04e`  
		Last Modified: Tue, 28 Jan 2025 01:30:45 GMT  
		Size: 199.1 MB (199116311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0dcef7782c615b88a9d3667ea0ba36557608b8382cab097a2ac64b5a7e68426b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2239475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16790cbdb6d7fdf6481800ab6074741ffb977110bc3f3e519908711181d8c11`

```dockerfile
```

-	Layers:
	-	`sha256:88e96330d44b7f10be8adafebbd415d7ba2ca1f1afbeb737053c321350ee2aed`  
		Last Modified: Tue, 28 Jan 2025 01:30:39 GMT  
		Size: 2.2 MB (2229857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae23a5231e4f7612c8bf98d90c1e8268f8d0459ff0cb2a5850884d024dfaf17`  
		Last Modified: Tue, 28 Jan 2025 01:30:39 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:450034630f488020d80446271f998226b8088e54e3b6cfe6d8abee8bf54f6a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226759210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b2e1c3625c7a320fdb2bbf16c0a67bac9fa91e4e5ea08b165f2800c4f896ff`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63714d304844773908e14ad77da88ff71e5bb8b68cfcc1c753f48d73611e5d49`  
		Last Modified: Tue, 28 Jan 2025 02:49:36 GMT  
		Size: 197.9 MB (197866539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:931fbb8bf49ff74543b3a20f52297f1156474cdb127f15dbc86e97aaa42fcad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43e3eeff963be5f9ca77e7574ace34c6c304d503097bd5c1967a6c85b1d68f1`

```dockerfile
```

-	Layers:
	-	`sha256:ac45b5bdaafaae949ea05137587ac1bb2c75779d39d8ed2b5b879924f97a2d6a`  
		Last Modified: Tue, 28 Jan 2025 02:49:31 GMT  
		Size: 2.2 MB (2230340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9e0d6b185a74d2cd793fcb04269ba7fbf4afb57ad983835d0f9a6c9e9aa8db4`  
		Last Modified: Tue, 28 Jan 2025 02:49:30 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:10fc140afbee8b4ac07e43b74090c13330df75f2cad6522fed44d407c95e2aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234520990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c76e78531946b7f6ae900624a71d252655c68dcd0a40c92d23a0a6387d7d791`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac948d6560425280907e603c22cc6d4305ca2262f057811a2bdba39c3efa629`  
		Last Modified: Tue, 28 Jan 2025 06:11:01 GMT  
		Size: 200.1 MB (200132170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17936a47aff9b49abc53bfa2e2d9eb255baceb43c3d311429e807a931cd133e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db4873382172849a0128024ffb341a2c90f8181ef71c5673a24fd8e4a4c4c16`

```dockerfile
```

-	Layers:
	-	`sha256:d55ff4f213cc3a08dfe9e94a636f8cd67dcb140610ceaa3be4ae93b410edd6d0`  
		Last Modified: Tue, 28 Jan 2025 06:10:52 GMT  
		Size: 2.2 MB (2231799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeff06be2d3eee19cff3c48772111ae535908f79a91893fa92103d10d8a86bf3`  
		Last Modified: Tue, 28 Jan 2025 06:10:51 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
