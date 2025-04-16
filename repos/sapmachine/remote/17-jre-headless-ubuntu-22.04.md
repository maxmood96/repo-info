## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:63d91b7a48558e83e60443e1233b118a6683ccb2bf2df80ea1f340a9451aaa2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:75a6e3d2b5ce13392940c3f1b53fca123a7f6b7fc1efe2c3eb839f4b908079c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82134749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843919b98a87f5352643caf21bdd739f135c9d383ba798e39450e3b74220d76f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2bf162e83f3149acb16f2338fb690baf858228cfaac1a2d7bc01028726ea01`  
		Last Modified: Wed, 16 Apr 2025 16:14:14 GMT  
		Size: 52.6 MB (52602384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:399ffdfa7c05aeedee1703b57623d4ffdb142dac791c03870e610fd4b385c960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6580adf55d749a1e54c82fcfa99f4576f656845c9a9b90a2b89a187e36dc2466`

```dockerfile
```

-	Layers:
	-	`sha256:a0142ef85375b245b0223f4e90c3cc2423982a533414e1b7a2788c527b74f933`  
		Last Modified: Wed, 16 Apr 2025 16:14:13 GMT  
		Size: 2.2 MB (2164976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3778fe81f15d38ff09afbd0257251dace300c2e99f6e055443869d6a8b22b20`  
		Last Modified: Wed, 16 Apr 2025 16:14:12 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8febdff02f6dd4b85b38e4b75addb246d29162992316f44c72e7cf305540536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79361441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32eb31c3e83718bc652014f712ab5b2913e75c14d0a03284f4712c0328b5f52`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2053120a60bdf19eb5f24490faf291ae8c04b21395b01126ff7e58cd918c6d`  
		Last Modified: Wed, 16 Apr 2025 16:42:52 GMT  
		Size: 52.0 MB (52007210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e2527403f37cf238d4109991f4116161675fe288c84e5c245064168c23927a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2173683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96040f082f2b5492dfa53da803047db30e0a16247346e909a20854fb0b788af7`

```dockerfile
```

-	Layers:
	-	`sha256:7703509b0083b6f4fa4493de812e0c625cb2b75db79e9a51c813df8dc98dc659`  
		Last Modified: Wed, 16 Apr 2025 16:42:38 GMT  
		Size: 2.2 MB (2164648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f973959f825ff8db60b7ac54bba50e3466153a903d181492fd79e6c479c4de9b`  
		Last Modified: Wed, 16 Apr 2025 16:42:38 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ac20fbb97b23a30f59118087fe5819aa32442bcc891d6f4a538ddb4df2e63200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88369375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324204402f3940ad28691b502c0da713d854db2358bb24d8644873d1d20b6439`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c1b1bdac5ae8718c9477a774600dc114837a88516a8750047c02553cb6ba00`  
		Last Modified: Wed, 09 Apr 2025 07:20:22 GMT  
		Size: 53.9 MB (53926679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:31a3442a62f74d170b2d77b21f092ba3e116dd88a2bbea376ddf0dcaf134dbdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e0543719dcb3741def5f6bab91f21af220ba9be07d1249277c2da4b9dd589e`

```dockerfile
```

-	Layers:
	-	`sha256:a32f1f14024291e061a173761e61a04146a99b6ff60d107271a7d5e70079e5ff`  
		Last Modified: Wed, 09 Apr 2025 07:20:20 GMT  
		Size: 2.2 MB (2168887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5d4d912d1cc4ff529377240bd53db0c08bde8d180ac54fa85e9dc994b3ef43`  
		Last Modified: Wed, 09 Apr 2025 07:20:20 GMT  
		Size: 9.0 KB (8976 bytes)  
		MIME: application/vnd.in-toto+json
