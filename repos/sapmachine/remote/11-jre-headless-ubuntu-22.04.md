## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3a0541bb51d0b3730cc31223c4bdcbe704ebcb3a5556cac81644a6cae7553ab3
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
$ docker pull sapmachine@sha256:f9d129860293164ff9205966e88bbd23270a4ea1a99ece718d837e7225d547c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78318429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eeca9bc4202af682fed79cb5097223899d0bc7aa7fd03bd1fc35c6447b47eb6`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0670cdffe2587699f0d2e60bfe6acab060c79b8971680c6b24e58468f7a343d3`  
		Last Modified: Wed, 16 Oct 2024 18:59:47 GMT  
		Size: 48.8 MB (48782741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76e52076fac714e5e34e96f7fc3cfa8845246ddc9c2f46a370fd834e8c915403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11a017382599947ffd11f4071098b0035717721150118bebf8f7875bfefac43`

```dockerfile
```

-	Layers:
	-	`sha256:23cd15a92ca217b2726bc70111e0eea5999256cba3ad93f16a28aa3089018780`  
		Last Modified: Wed, 16 Oct 2024 18:59:46 GMT  
		Size: 2.2 MB (2157629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7822c68d63e236650ba73e3216d6834703e4496f3466710f16fe1c6804d588f`  
		Last Modified: Wed, 16 Oct 2024 18:59:46 GMT  
		Size: 8.7 KB (8715 bytes)  
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
$ docker pull sapmachine@sha256:03eb5af12f1708b2070399b1b74d5deeef4da0a5af12567f0b13eae0a49ce68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81635993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb39eb1f6ebeec9da4edeb516b7d417fcab472d572ec49a2f21af6e9d85a99ef`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53f90dfe10705baadf19de6fc07d7f229c5b45e8e1ea7bcc8b732aee9b53eb0`  
		Last Modified: Tue, 17 Sep 2024 03:10:39 GMT  
		Size: 47.2 MB (47187751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e883274baf001f93b9f4dba62cecfb1dd9662f99a31679fe310ebdebb707f742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb38045a379c4b7d5f61d582537df066c2914aa52721cc1b1ed4b4a3ef89e40`

```dockerfile
```

-	Layers:
	-	`sha256:bd8f8087aa9b09a51e00dd7ad97e14dd6b8979ff71c3e7dbc3088dd83c2c1b6f`  
		Last Modified: Tue, 17 Sep 2024 03:10:37 GMT  
		Size: 2.2 MB (2160897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c034e6ecf284f4588956f2eb2664f554450ae7126163005a545690e8b7c8cec1`  
		Last Modified: Tue, 17 Sep 2024 03:10:37 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json
