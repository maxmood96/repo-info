## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:fb0b12a95b254b1deb6bd56c37827715234288e358705562162a7fc8efbf2287
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:1b07353f70f1a66e288e4ffcc7cc7154c9a3a887480c50c4cd4b375414297a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242962172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea2f550fa153a662af40c4eb4c6eb7a4d3d35be6f6b8f8b16616bdf22e7be5`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc052a312bd491e238099988ef12f4f6b5dd903c978be8729ca879bf4ef9e997`  
		Last Modified: Tue, 04 Feb 2025 04:49:23 GMT  
		Size: 213.4 MB (213426231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09f43f9b05a6b6c4711a7df584fd3385d4b7e061198f2641a52374bacf0e33b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694445c082348ff56300971e8b8223772c0f8f23455ee5daefa297dd8a738a54`

```dockerfile
```

-	Layers:
	-	`sha256:21f2848b9eb1153d80700161abff75e97647cb8b27362511900dbe52d4b87094`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 2.3 MB (2250363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e63e3460ecb62554c166381e3c1c2e3240a5c2419049c71d71224e96fe11652`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3dad840902d836b20ad77989baae6660b79ab00c97c516aac511334cb8581843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238983244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0bf92e03f382b4d91bd2c054910138e90d49ae4649f030ddc893e1f4502357`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc02b3bb1a91dd00efe1b9de06045977508bdeded60d8ff9237351dfe21cbba`  
		Last Modified: Tue, 28 Jan 2025 02:40:24 GMT  
		Size: 211.6 MB (211624915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cbf5871599501e508ea7ad0dc4d4a39c6a931be2ad4b1d37ec5052592bc7e60f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7efb6b584617eb46e0ea823222aef16c5940b05d382b191db6e536b3dc2af6`

```dockerfile
```

-	Layers:
	-	`sha256:92328b3fa160327695bbee4e3f6c84642ebf7ec6608186d0ad4bb3ecca716b9d`  
		Last Modified: Tue, 28 Jan 2025 02:40:19 GMT  
		Size: 2.3 MB (2250059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdca3ffddf50abb666e0f17a00c3ddb6b0d47a61aa5732acea42a7d2b9138a9f`  
		Last Modified: Tue, 28 Jan 2025 02:40:19 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e6fa2f3d77ad2f15141caaa4dcc0f75a5efc26e31c76ad5d7723144647aec685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249001925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f46f9e562c35511d9b16274cec6d800b82460e7670b6f924c425f4cde84202`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be735cd36cbe7c054332ebd99a8e55e7d1c3a9b6ff9d66e32e494e671f9acf6b`  
		Last Modified: Tue, 04 Feb 2025 14:43:47 GMT  
		Size: 214.6 MB (214553990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:528b5a4c10183a4f9b0e1a7043c96961fb3559fddd4277fc2eb22a6371f60233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1601789f319f06b20c3db0ba898ba407cb8cbd18505f6cd0e1af89e8ebe31876`

```dockerfile
```

-	Layers:
	-	`sha256:3ef84ef9732e8925c70f6d3d8f3d9aa988eb821e5ae2a31d80c8d9ec2a1ad210`  
		Last Modified: Tue, 04 Feb 2025 14:43:41 GMT  
		Size: 2.3 MB (2252340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5626c6a2023883765c33813f44cd36b7bcf1de270711a71798311a59edf0ba`  
		Last Modified: Tue, 04 Feb 2025 14:43:41 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
