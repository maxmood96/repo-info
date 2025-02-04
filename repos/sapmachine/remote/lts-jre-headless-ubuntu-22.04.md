## `sapmachine:lts-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:fe77af8b87e9b4c92167881b1f3eb082781c64414d205ee09fd79309a3e51078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6357eab069e52c7f0e5d0f6e12227724a856f1aa29a93844c2580abdcb5831da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88043649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc109cfd19212439821a55c3793f14a0656b248d4c42f3a959cc6e8cadeb84`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:75cca8a0bacac8f8dfa945ab6c1777fdfc41c7874d574474e4cba653a43aa19a`  
		Last Modified: Tue, 04 Feb 2025 04:49:13 GMT  
		Size: 58.5 MB (58507708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b93e768bd33af7ec50148d12322e94691f73da7754355391e6b2e8d6b6354e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ab0173f6db98ba82f5a6da342a330d13531ee6908fb5ae92867cbcd404857d`

```dockerfile
```

-	Layers:
	-	`sha256:724c362d49cfb32aed6658d347fc8e037d4764f4e0e04a42d665f625f988cb2c`  
		Last Modified: Tue, 04 Feb 2025 04:49:13 GMT  
		Size: 2.2 MB (2166842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4348d8d7ac380af83a9e360c2fcdc4012823c1eb6eb3ef12ee96e4ff43755bfb`  
		Last Modified: Tue, 04 Feb 2025 04:49:12 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b24737379ae4e1cbce3815b43ad8941645fa4aba3e8affdaebb12537d7bccebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85009883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574cabf11c34164b0a16b28ee81b1c46a114ad28b1bc79be68de9a61535d111a`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c86e4aff9668e685170760a8a627a900fcba3b6ad4d26a68e85d60a4a70fb2d8`  
		Last Modified: Tue, 28 Jan 2025 02:42:20 GMT  
		Size: 57.7 MB (57651554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1b004ccdd9bacf7fa24acf4886040b869099b4b26a7491d8e6681630ebb0ed31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32830dc2495f4b420bf81ce2c75173791568857a3ab3521cec01b80ca218bd4c`

```dockerfile
```

-	Layers:
	-	`sha256:108b86375d32b64c72e88500de9953aaf30379d068f5c2166774f7d2058ee77f`  
		Last Modified: Tue, 28 Jan 2025 02:42:18 GMT  
		Size: 2.2 MB (2166538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fadf599b426e0e8f16643eecb9f8caae319ac829d02e69568148eb408fb3f8c`  
		Last Modified: Tue, 28 Jan 2025 02:42:18 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2c2b3e9d62717d0cc26dfdf3ad38873e9a22979b9b614cca329717087a2b119d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94354012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912bf08b384680704994c4adc626d7f9f70445791f31ac9848c7e2ee7134b6a4`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed74ae5890fdd443895685a19e671cc7f1be4016576afb8bd76f942e8666a99`  
		Last Modified: Tue, 28 Jan 2025 05:57:30 GMT  
		Size: 59.9 MB (59905770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd7e54975f8877c87d1397dfe4a6bf995ee0e64d5928768eb11d1405461961a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2180448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19145d4d042bd79aff67471b68770114c5fbf3b49802b8f63504d68e650dc5eb`

```dockerfile
```

-	Layers:
	-	`sha256:7c50d280662168a123d98e4a9090b35bc3bae2d04ae92ea934418bfa3bb483b4`  
		Last Modified: Tue, 28 Jan 2025 05:57:24 GMT  
		Size: 2.2 MB (2170765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5352e00ec451c67e39cb4e654a68747da1f3f0c5e0146f0299cd18b740c1596c`  
		Last Modified: Tue, 28 Jan 2025 05:57:23 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
