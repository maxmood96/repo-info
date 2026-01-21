## `sapmachine:21-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e912652ff7fa0dd8671eecb68ab829c8b8749f0e44df4756aa1e29934f0095a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ac77675336006574f38148319cc7471109787c5a07204b7ea60183c58f5de9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89949643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f9ccace7e56987685e4ee3c1a7e23e5ad547d7fb1ac36907caeb92b9bee23f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:40 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:43:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16880190dd203928fe5791bca42ed58f94f48168933eeaf8a11591789db06108`  
		Last Modified: Thu, 15 Jan 2026 22:44:06 GMT  
		Size: 60.2 MB (60223632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c86855bc308490b05d99b19d3ab8b0897943c175a5bab61d60911718186538f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0341344464dcdff1dfdbc380f3a85817a74f720b155b21125419a95c00b6a5b`

```dockerfile
```

-	Layers:
	-	`sha256:3b0c11a23c22ee93dcc458580669d5200f2cb19583bdc067001a65899c649236`  
		Last Modified: Fri, 16 Jan 2026 01:12:00 GMT  
		Size: 2.5 MB (2518644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b250d0877c0920091291cf35f43a2d4f49f257a16b86948fb6ccce5f68e77f69`  
		Last Modified: Fri, 16 Jan 2026 01:12:01 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:398ba3ec533a686d44d63730ac80c3f546c99f628e7224407fecded86c5dd01a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88289451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85161c4e5ffe878cd288f11043e1327f17da4401de5fd9bbb8eaafdc5741710b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:46:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:46:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:46:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46430ab50871d8c16b4919088fad71330aae83ebc15341cdc34e2ce78152b5`  
		Last Modified: Thu, 15 Jan 2026 22:46:42 GMT  
		Size: 59.4 MB (59425627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bf34c5a040fdc08b22f31f541c1efc784161dcf1b39b41b0911787d44a2ebaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99912a4a3bedee689e5bcff2c9e3c0c4f4447c10379b0d48b0fa45d1fda59b85`

```dockerfile
```

-	Layers:
	-	`sha256:1337c626cf55748f4c05735cf4c99c4109f16e95202a6794be08c46f85d2476e`  
		Last Modified: Fri, 16 Jan 2026 01:12:05 GMT  
		Size: 2.5 MB (2519160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c196a3ad534a94b645922e04acdf14754865d818d969ae64ae340c26ae6995`  
		Last Modified: Fri, 16 Jan 2026 01:12:06 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:114b928756b3dfdcf85f85fa15b55035f71ca93a95e1457cdafcce73894ccdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95760424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c326cfce99e659405f1f2567b8811d69098389d867915c40e23ff5249db31d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:35:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:35:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 23:35:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 07:12:18 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61050a9c53f88ae003ab12ee17d4edb4b3c35326ee8a75972079bf433bccb9f3`  
		Last Modified: Thu, 15 Jan 2026 23:36:33 GMT  
		Size: 61.5 MB (61454265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb018032327198be567050dee02ddbbeead2231459269e3276c0bf34726014f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d551cef6f2a13619662ba4cd849ecc93c1f8910ca9dfef40f9c0b8356d52c9`

```dockerfile
```

-	Layers:
	-	`sha256:22116e23427e5784c9a5c8501871a4b668cc8bb8b676fc73b7d8d570b9f64069`  
		Last Modified: Thu, 15 Jan 2026 23:36:02 GMT  
		Size: 2.5 MB (2516725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70dffd1d53d57364c540f53639901041b71d0331cd2948f61f0f2be7dc2adb1`  
		Last Modified: Fri, 16 Jan 2026 01:12:11 GMT  
		Size: 10.1 KB (10105 bytes)  
		MIME: application/vnd.in-toto+json
