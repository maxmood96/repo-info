## `sapmachine:17-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:663c9435b181a3ffbc0ec9dd2bffebfc3f8cb48c4f156d64c49db8933a4654b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7e2e4127f196795c79459fb3b281bb242b30da8ba5a73d3d6a6ed71839b8af15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79558262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646d833c49816eef89dfb5793b8e5a58481b586474b318eb61b0735d53ba734a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9040c90474068f69c2fa34c6f1520dcee8f380227612958e50d990c9d1dd07`  
		Last Modified: Sat, 17 Aug 2024 02:05:58 GMT  
		Size: 52.0 MB (52046493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f488126dddf88ce5dd398df4af67206835290e66f58b421d5a8bc76a23ae86ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa348cfc9420907b1ef1ab1123adb87906648c4da13cf1c5ffee81e295bd2ac`

```dockerfile
```

-	Layers:
	-	`sha256:790818e702351b5779facc0f11e2e49ded705355d7c29d720a96e7c6d012acdd`  
		Last Modified: Sat, 17 Aug 2024 02:05:57 GMT  
		Size: 2.0 MB (2042354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92185d806bbf8ae320d716b651377ea48b658cf6ef01a686cc8f07822e11f3eb`  
		Last Modified: Sat, 17 Aug 2024 02:05:57 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6d7e0fe00b7d82944614ca9b48736c9910b8c1ee580f0266c130686fa8bc9203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77399521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebfe2e6f406d1d79e7eeff8e746a690e0030b0aef36dbc80704c715415150b2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab0927452410e3ad661161d735cd6a7c00f339a087162adf4866185f45e4d58`  
		Last Modified: Sat, 17 Aug 2024 04:40:47 GMT  
		Size: 51.4 MB (51425304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6d57e9bcfa1d8cfa43ec43a615aa290f4924fd7a3af0edbe107bc41afcd2559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2050960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e115b698fb43838f0530e76f53e03e676aa8fe2101c08cc1cdaf06fd161b8`

```dockerfile
```

-	Layers:
	-	`sha256:67a58e8ade6fba492c161e97c3456779a4e1ee3b1529fe60116015759e548676`  
		Last Modified: Sat, 17 Aug 2024 04:40:46 GMT  
		Size: 2.0 MB (2041981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0982a4f2521bbe87c2d709ad6bdda65255debdf98d7c322b4aa75a46f2aa18e2`  
		Last Modified: Sat, 17 Aug 2024 04:40:45 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4da720fe2cbacc37be4206ad1293794b9c89007515200ce6e09eb511af858ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85075554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99509ded3129e82e90f0867be9eb58dbded728bbf7349421e8e07ff8290b655a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc42ad9501eb7a09bc4d2d85cb47977670fb2771746491ccf565824f644178e`  
		Last Modified: Sat, 17 Aug 2024 03:26:07 GMT  
		Size: 53.0 MB (52998414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bb97ed1928c6e3fe5a4f0155d44de0d88cfd8bf4aee136329244a63e7aaa283d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b9e80a614e67449d53438295c3ef3f5296756f86473553762b7f9e58ed7661`

```dockerfile
```

-	Layers:
	-	`sha256:b3e6bcf6e8541174ffef28487aa928c6446b983faca78d780a9737551da983a4`  
		Last Modified: Sat, 17 Aug 2024 03:26:06 GMT  
		Size: 2.0 MB (2046056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71cecaffac2159ffb640968d9ac11ecc2ea8ec50a0a913c3e4dffcfe8bd1dd4`  
		Last Modified: Sat, 17 Aug 2024 03:26:05 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json
