## `sapmachine:17-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:fe8727f8204dd5052f2fb98d4d5fd1caade59a242d0050e8a6e4341739d0bfaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d7315b327b85d1e02d743e789630882a4d9c72336c9a7fff0e97e6efe42fe21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228870768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8d6924833e01a93db45044834d96cf51eac8254ad494ec82f22bfdb13fc155`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc4e80818ec2e45a8d557f1a0ce8e75621ec1489b73f0c286bba21d82ccd5b`  
		Last Modified: Tue, 04 Feb 2025 04:49:49 GMT  
		Size: 199.1 MB (199116478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bb757841a91e73bb24c0e59139145af8e85c7baedcede7666b303c32bfae97a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141144a2f8dc4e096698a31c73a913b89de31680fa7bf7778a0a959633562480`

```dockerfile
```

-	Layers:
	-	`sha256:7cfab3eaff4e035bc408646d244f34f076d635b53a38157e0f8f656866271989`  
		Last Modified: Tue, 04 Feb 2025 04:49:44 GMT  
		Size: 2.2 MB (2233819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743870a148547f5ae2aa6db083318095eff821b8087f1c0c522789b70970458e`  
		Last Modified: Tue, 04 Feb 2025 04:49:44 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

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

### `sapmachine:17-jdk-headless-ubuntu` - linux; ppc64le

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

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

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
