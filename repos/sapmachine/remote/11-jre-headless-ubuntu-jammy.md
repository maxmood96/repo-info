## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:8a6f431eee6c81ae34787df55edcf293fc2c699eff166dd62ddfd903b26bf33a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:751388e53f04dece45fd07c3cc92da876fae16b7f992c61bf8683126f1db2d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78315028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3aafc3cbf4625a6aeb73a49b157822a6258aedee9f2c309d3f83ecf72dd7b86`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eaf0fcbde625a9fb3101684a889bddca6d2653fb0c552c7f9a8827a2ae8956c`  
		Last Modified: Tue, 04 Feb 2025 04:50:24 GMT  
		Size: 48.8 MB (48779087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dbc307405911b4be7986b3a4423736f440c4006e7546b0e9baf74c4bb8ca1c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f62a4090cc0e9f1e8377b26b6878e1fba72f89b7eba81f3b60e7c80fb14941`

```dockerfile
```

-	Layers:
	-	`sha256:7a0c73ac2bdf5636f6ec40210c7891fe401bdb1499e4283be2fda1dd3de96490`  
		Last Modified: Tue, 04 Feb 2025 04:50:23 GMT  
		Size: 2.2 MB (2170910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eb6c2ebb8000170557b7ce4b4713c5ad4142f78ef76a922128962bb15292f8e`  
		Last Modified: Tue, 04 Feb 2025 04:50:23 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

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

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; ppc64le

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

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

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
