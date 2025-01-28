## `sapmachine:lts-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c249dd6125608f37fc4f38e4a94565cc3b5a3b65eb7e00a486e122007f9ca9ce
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
$ docker pull sapmachine@sha256:14cab4f9a6159246abe72bac74a1ce3c2587c40c56640fd3c2a1e4e0cde1b2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88042995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba7639d47aa823993f3fe685fe8bffdd387258929166bd534d934e016e37824`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9200e792c46e4130ab3f30be56cd8a30e62cbcd0fd09e0d380ed795594f5f3fd`  
		Last Modified: Tue, 28 Jan 2025 01:30:03 GMT  
		Size: 58.5 MB (58507307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b4856c71adac22cf8111c0cc565f5fa60fbe2201dc2d4707f8745a42b07137f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15efb924c4c4714dffd622364c650f7e0f988e4eb2baaff50a4b7b74189d1b5`

```dockerfile
```

-	Layers:
	-	`sha256:0e13483c65757778308c85d7b62918b820f4e0b50cbf157fb80af1385e76b4c7`  
		Last Modified: Tue, 28 Jan 2025 01:30:02 GMT  
		Size: 2.2 MB (2166842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fc1fbebbb1390df0a6114d3086f0a4496327ac6db1762c95c95cc8b5ec6760`  
		Last Modified: Tue, 28 Jan 2025 01:30:02 GMT  
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
