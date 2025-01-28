## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e6f2e5a62176cb026b758bec654b4454e55a2a268c6a1b41ffbf67e2fa43ee86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8cdb54215df2fcedd7aa58bed1bb0e55842422dc0bb962d64047e0170fc7ed6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78314398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cb2321d2273b92c68e6e1c71508648e4d0edcda89950a3f45d869087f8abdf`
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
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6aea569dfe3691ab6f554161a8730fb9cfa33437a644e51d10f93d15be4c754`  
		Last Modified: Tue, 28 Jan 2025 01:29:08 GMT  
		Size: 48.8 MB (48778710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b8efff43222599ee5d54317af0ddfd0e59f60550a3a020aeb1f09ad507cf373b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68ba978eb7b959034604b1fee9951a529f53e819510370f9883e713901563b8`

```dockerfile
```

-	Layers:
	-	`sha256:b0f4245117f5266d65090b6c81bd6b4cde3d3193905716539b7b70813a41b4b4`  
		Last Modified: Tue, 28 Jan 2025 01:29:07 GMT  
		Size: 2.2 MB (2170910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61890b60dfd35ac92a6fd67dacc18ac8ea38a2f0b94acf22cc55f525be5424b9`  
		Last Modified: Tue, 28 Jan 2025 01:29:07 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cc0ca6a10311cb9db16250d59c1092381f228f7876a18a7eb0692258d931079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75420843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3addb882f09c0a42cc5d1532e096d450f433f1cfd0b1ffe9a2b0303436ac726f`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38032949bd5a497bb9c5daa96eac83ec8cca2c05a91db5d6254126fe2f5914e`  
		Last Modified: Wed, 16 Oct 2024 19:49:40 GMT  
		Size: 48.1 MB (48062514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eef83ffe2fcd77094cc3f1e9bdb7d915ba6a3b8ec6b956247daeed39e7ab178e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8298f0ee6fe00ff8006b25eb24357a43ebc3cfdf9ed50938e059c0304f30bae7`

```dockerfile
```

-	Layers:
	-	`sha256:aead3d243f714a3eddc304940de6e570e4f02f9fb1a8c56003bf85e0f5665044`  
		Last Modified: Wed, 16 Oct 2024 19:49:39 GMT  
		Size: 2.2 MB (2157927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722d8b5552146fe076df8950908676e8927a43355c8abd6c139082a551ae01c6`  
		Last Modified: Wed, 16 Oct 2024 19:49:38 GMT  
		Size: 8.8 KB (8814 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:31e9aaf0eb0beae18be248c4d9d152962910616e8044adc318195b695badac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81687449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca5527bc7a8742d1f0a3100906e9c35f595e8607ddfe6e5da979fcf61345f6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea55b381cdc10da20f27a9d483fac5b24a039acc8e132cd9584890fae64b76fc`  
		Last Modified: Wed, 16 Oct 2024 20:26:27 GMT  
		Size: 47.2 MB (47239207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c7f528d27217d83c5e6972fbbb11c21339bca17f3c18153354d354ec1c4b185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f982aa82ec140dacfcf237e36dff9cef2e954f0b05a20e6a53fb18e5194ac5e8`

```dockerfile
```

-	Layers:
	-	`sha256:6b5cd3cf867b1c23413b1d03666c9dc8bb3ef2ac0457016d0f206fc418372f9b`  
		Last Modified: Wed, 16 Oct 2024 20:26:26 GMT  
		Size: 2.2 MB (2161544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5748f7f293e071ff98eb269bb9e51518dc131dbc2d873270e8cebc5196f5cd45`  
		Last Modified: Wed, 16 Oct 2024 20:26:25 GMT  
		Size: 8.8 KB (8753 bytes)  
		MIME: application/vnd.in-toto+json
