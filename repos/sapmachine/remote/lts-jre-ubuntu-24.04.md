## `sapmachine:lts-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:4a6a6d73c7050bddde2259b6eff4f0ef8e98fb911172449dd9cfe64effb0eb9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e9e17e2021797e7bed6299c2bc23a194f810ec57a0da2cc482b6688f29e8b25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89865351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625e59036db53dd806da86a29f525e6a78a0bdc35fbc3a21f163f3c1f88f4bb4`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0ccc56aee379584c08b0d4ab8666caa76aee7474e0b1aaff3ffced1c114bf8`  
		Last Modified: Tue, 04 Feb 2025 04:48:38 GMT  
		Size: 60.1 MB (60111061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:344c0adde1622045ef99b250429fc2e24114c40fd8e36c47cf09e77c4e112538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9792290ad6b8588e8b09dfd20c7995ea6a01a7e1d86e2335dfdaa26093114c16`

```dockerfile
```

-	Layers:
	-	`sha256:f0df94cb9ecc195957117689b189691d6f5045fbd969bf8de0ee77a81fe3ffc8`  
		Last Modified: Tue, 04 Feb 2025 04:48:36 GMT  
		Size: 2.4 MB (2390003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4484dfb9ee2cae2a241c0aabce15721f583dc57fffb7a4da0d0849cd4999383`  
		Last Modified: Tue, 04 Feb 2025 04:48:36 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5b7c8d31d04be50f401b6725f667732a68e668e3a842a40e2f290804cd7df0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88192610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92755ee9249bab4a3df618c41b26575e8f6161bed980c563f070f7089732e676`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0c2bb0f1f153007da3076075a2282d709fde37eb6fa8e76280a1b158804d3`  
		Last Modified: Tue, 28 Jan 2025 02:36:43 GMT  
		Size: 59.3 MB (59299939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:adae53b23494f45d26307016414ce56ebe9eb8cee5eaea62ede7a73c013f948b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52377e16f5c46834c7e5cd8dd4bb8ca73494cc7391b8fedbc086cae62cbbd53f`

```dockerfile
```

-	Layers:
	-	`sha256:b3ba109e3fb3e13bc5f50aa269e68d6083afccaa9c6845c0ee1de9c3b24e9041`  
		Last Modified: Tue, 28 Jan 2025 02:36:41 GMT  
		Size: 2.4 MB (2386569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c519dfc01be7c91163a7fa8ebb2058b02f5f59a1be35696ddadfeba5e2bdfc8f`  
		Last Modified: Tue, 28 Jan 2025 02:36:41 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d56b0d0cad18f5829686f266d416081ba5619bf580ef86a5a4dc1667907e06a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96199315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41b9432b939c3ef0875ef609c40b225083df8798e7567ebf0ffe1d5a06594a8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4453ee61c0d5c1bd22cf976ee39fb0b14b3ea327d36aa14663002f4a650f051`  
		Last Modified: Tue, 04 Feb 2025 14:37:47 GMT  
		Size: 61.8 MB (61809491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e5462a2719ae1be465cd78b3731759792a9ba33161c9e6eb4c1ea737d9ecb988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad675547915e7b88a2977fae911cda4d414817b1439be012c0bb6fd850d69067`

```dockerfile
```

-	Layers:
	-	`sha256:e82cdee0435ba898b384624ba20b82fda623d4a4df2dcdb772afa14e6024563e`  
		Last Modified: Tue, 04 Feb 2025 14:37:45 GMT  
		Size: 2.4 MB (2393972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68b89c57ae5bbe141ea735143e53104cea21e39368a363a45c40bd0b6056e0e`  
		Last Modified: Tue, 04 Feb 2025 14:37:45 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json
