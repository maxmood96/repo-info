## `sapmachine:21-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2de6f75ccd5d945236b3466d76650900c1c226866baba0b1a5f4a5ec4c15e177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:eb00a6e2a4b59e270293ec41a06efe74515e8a7e0e8c23e7e6f9c8361768eec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244695580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3934819ef6c59fc91b2aea55eddcbc6bb77f049569ad2d1fa5c86b48f9141c81`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4665ddf8590cff01ed85dad480fe139cbc7547245750193897acc91288ab5a`  
		Last Modified: Tue, 03 Dec 2024 02:35:49 GMT  
		Size: 214.9 MB (214943612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4cd918608f535a6be0acca02e0e9b45208c45d33def423e59ea363e959bb1481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8af13e4f699aba7c2a910c2cecf7e852b5d0de1ca4037ae1cfb8dc5477090d`

```dockerfile
```

-	Layers:
	-	`sha256:3f36e0079d8c5565fa52be29ea2dca6f0bd240d9424a64c94b715fd72325a761`  
		Last Modified: Tue, 03 Dec 2024 02:35:46 GMT  
		Size: 2.5 MB (2473885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1323fa76312f0c25914c64fbe1a8477484ee93519643a3e5a1fcf690601a9d5`  
		Last Modified: Tue, 03 Dec 2024 02:35:46 GMT  
		Size: 13.3 KB (13319 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:40eaf682a1fc213be64aba88fd38854bebb0e8b96ccb66008a819064fac03edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (242037848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799064659efaa71951a370c9a9ac0a420b6783b108eaec0ee7f6ae9c2108d56d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c778935a0b47d72cae383e9d4fc4831f38fd060bbaca4476cf0becef046700db`  
		Last Modified: Sat, 16 Nov 2024 03:47:13 GMT  
		Size: 213.1 MB (213145423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:776661a1f570b6da1d3f1714399c0565ba1aa5326cc09fa6f5a807c175e01b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba4c416b057e41fa56b0fdfb5e01ea2bb42008dd3ec81657da13aaf939a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:4852b0a1ecd11050405ae253fe60f49b069b92af591b6a916cbe024f996e72b5`  
		Last Modified: Sat, 16 Nov 2024 03:47:09 GMT  
		Size: 2.5 MB (2474500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b30814567331cf39bb0b736083724d34994a797cf28bd7dd3f732fce654e0e`  
		Last Modified: Sat, 16 Nov 2024 03:47:08 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ffed03fc6e93594eacb69fa284a936d2def1178b27047fb4c39487cfb769a7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250783442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557933f1344a5fa23a8324b96cba998eb91feb0e36e083283d0a32feb48df327`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b106e86f46944f37ef70bcbbcd8cf9c35dac2857840b740b6b6e106e42e3101`  
		Last Modified: Tue, 03 Dec 2024 08:32:08 GMT  
		Size: 216.4 MB (216394622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:58eeb591295879ce1ba33816d8dedc78edda56190e63b5cec2847e66126747b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5ea51fa1b016d2ff0d148dd278a25be56e05ab799426dcb3870e680d564351`

```dockerfile
```

-	Layers:
	-	`sha256:1fc4cd42f3eda02312b9f57787085ef697953aeb6711d17ab480448e33982ae4`  
		Last Modified: Tue, 03 Dec 2024 08:32:03 GMT  
		Size: 2.5 MB (2475957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df9d3a892e961535e8b8d9b83dcffdcc4a7d2e69bae5c69edce4fa0b662648c4`  
		Last Modified: Tue, 03 Dec 2024 08:32:02 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
