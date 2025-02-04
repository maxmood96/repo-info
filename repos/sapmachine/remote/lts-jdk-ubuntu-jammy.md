## `sapmachine:lts-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a8feb63f30e66c60cb697678374d9c52e7c2391d05a697cd5f42104a6bb927b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:a76ff51c6a439a32f955a03512ae0291c321a2cba776f5f3cf6c16456c217718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244182178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662af7b971d3020359837877a7b0908c15cc56c59d8ca5ba318cc3303bf9b701`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4c4c786965c6dffbde9a8be0bc639cb122e4e020d2e2d1796586ebe383849159`  
		Last Modified: Tue, 04 Feb 2025 04:49:26 GMT  
		Size: 214.6 MB (214646237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4120b6a11d75e4aba61ebbaea1112c436a7f032cb1f29f1bec4288b53a34e078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0705b10187b92ec5727a4556abf6e2ca166528284ac0f877ef5f07bcf775617`

```dockerfile
```

-	Layers:
	-	`sha256:90f6236210127c9082daf9a7daf84c378d76957e158dd7abbf0654f88f8daf74`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 2.5 MB (2494735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034e9bc1224821adc24e72c18303b29c6e3248f7642bf0c10fe2b77504333f20`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 11.4 KB (11444 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:817a337fee926e0bc148ac53e2c05b3431850bd142a77d5f1673d37bcb472661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240199526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba43ebb3f407f4161744a31c3ae816f85bfcedcc436a56201c0eb030834ea2f`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:88d148cd550aac27833307636df707eb7c720ca3f150a3d215da4ebf02498803`  
		Last Modified: Tue, 28 Jan 2025 02:39:06 GMT  
		Size: 212.8 MB (212841197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d9909d5f2f3ee578f0fcbb8de18182220041a46f311db5e2fad58ea607f14c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf2338414cfd3f038e9014629101575d86515e1a0310ee800e47ca91cfc17f3`

```dockerfile
```

-	Layers:
	-	`sha256:0861c07c237c276bc646eb918b10b9b4df4c3b8ba50d4aed79425527e6dab600`  
		Last Modified: Tue, 28 Jan 2025 02:39:01 GMT  
		Size: 2.5 MB (2494513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ec2e29b3bd60300d610adf363b2fc5e833c82019696bac207214e059fe79d5`  
		Last Modified: Tue, 28 Jan 2025 02:39:00 GMT  
		Size: 11.6 KB (11645 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:45cf35892fcb7c024eebaa570640fbed7bc9b4785f7186ba2136ff65ca8d84cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250394277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430dfc307312d9e7077f709ce287bb9899ca7c13281b61d5fcee6e27d55dbec`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cfe755ab69d41c73a2df0436676d7a55400e7c102649efbe5eda8adcc4c2cfd3`  
		Last Modified: Tue, 04 Feb 2025 14:41:38 GMT  
		Size: 215.9 MB (215946342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:71386d7c0095a6c59d25b2e7eb4715a26d69a7a82d581b50552bd600cdbb3a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e37a94c2a832418210bf1a6577fbf7b2e02696066fe9581d27afe45806cf2a`

```dockerfile
```

-	Layers:
	-	`sha256:d939711828e3db0c0a33ef4fd4da6c6744a85dd072b0959216f518dfef7e6dea`  
		Last Modified: Tue, 04 Feb 2025 14:41:29 GMT  
		Size: 2.5 MB (2496818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce2f81da5f42d5139360b46a57901f318a68fa506043689abeb6ff6501a7b74`  
		Last Modified: Tue, 04 Feb 2025 14:41:29 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
