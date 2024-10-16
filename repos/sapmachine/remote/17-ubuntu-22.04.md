## `sapmachine:17-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:18bec345d8a4553e97599c08cfe812edf7c65ff70ecc3d5c70583e57e3918951
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ffde6e23a55eb2c41a6ea47d0d8e851375b1d331b362152dad326d36fb9825c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229352400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5767ba2a0b09565f1a5f9c7fa19f775a2334cbd6fd0b52a2d1cec0cc1c7ce`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3ea74009af129a86501fb8a4f8bb4a9b89f94cc369f90543d847769eb76379`  
		Last Modified: Wed, 16 Oct 2024 19:00:24 GMT  
		Size: 199.8 MB (199816712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0606fac36f4e19b2d91c57152776e5564ad4990d4f09658ef27dfd6f4b32a9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379aedbe79b968ea81fa882f32f46402cc1c1b7e77997b07de12032ae35c808d`

```dockerfile
```

-	Layers:
	-	`sha256:94aa87c2e9a206f5f41ec596f393ec97c9f78ef6fcb3521e77d6ab2969ac3774`  
		Last Modified: Wed, 16 Oct 2024 19:00:19 GMT  
		Size: 2.5 MB (2477876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d7c07f5a3039f37160f9969e3ca59adb177bf7e0ccc095d4cd9c92bb3d402a`  
		Last Modified: Wed, 16 Oct 2024 19:00:19 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0fff27a79e1d70f78ea1832b0af6fb167ff2eff83498bc8ae1621efa29031a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225845037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6aafec2d3aec6a4242855d19e6fd5efa5910084376cba84887edac673290e15`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78831f785ca35855fb01d61dac13d4db0f05c78c2b60fbe5b9803fe10bd0a73`  
		Last Modified: Wed, 16 Oct 2024 19:33:03 GMT  
		Size: 198.5 MB (198486708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f82f64a929e7c76893e1e8f6699b106ae1f1766264320d99fa907bd2726143d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7d11b68719dcbbf6407ae69cce6ccb6b7385fa5a920f324230e98ff9211a63`

```dockerfile
```

-	Layers:
	-	`sha256:3eb10bafa45ba2237294e6cf0a14991f1e2ff5e9ce32464b82e0024ed0475b68`  
		Last Modified: Wed, 16 Oct 2024 19:32:59 GMT  
		Size: 2.5 MB (2477604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce7fdda43f1f85464dfd5284d76020d1d116cd407117a803d3d8fd7003ec5f2`  
		Last Modified: Wed, 16 Oct 2024 19:32:58 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:15aad906188917d2b2548bea1f841e904303806186a689e42b6a4fc456a16a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235572970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26689dafd466162c6b1430c1de249731f926a94139665e8b2d9ac646689b8c79`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2bc761bb5a527b8846e26aa935dd08952ab95bc4b1c812db6c5ff5e339fa3b`  
		Last Modified: Tue, 17 Sep 2024 02:51:12 GMT  
		Size: 201.1 MB (201124728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e90132c85173778b74f76c8cea1988d578c18c99fcd06b39108dca94dc20c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a03950d4dd10541956ff316198d07e6d80e52c21644a53179031247fcac2005`

```dockerfile
```

-	Layers:
	-	`sha256:23f4abd76e969f71172d03c2b0232e1bbaed5309839685bea6901f70e62a8acc`  
		Last Modified: Tue, 17 Sep 2024 02:51:05 GMT  
		Size: 2.5 MB (2473271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03748582f2ac654eaccda8b31d7963423851b7448ce3e954f0bb5031d7509a54`  
		Last Modified: Tue, 17 Sep 2024 02:51:05 GMT  
		Size: 9.9 KB (9945 bytes)  
		MIME: application/vnd.in-toto+json
