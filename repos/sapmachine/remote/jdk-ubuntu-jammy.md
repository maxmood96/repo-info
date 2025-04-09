## `sapmachine:jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:4070699e430978afd5d2b85a66151574e85a51f839b83dd9df2ad8561c177534
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4265ee1f0f6433df8f54bb326e2e024f987377ad4c14aa89de851f3b0ee93924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261550944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2692392480f258656eb7e9fa04ca29a5225ec3bbc045c22cb21e40e031d42d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4dea772c810200e8eddd0c5358bc28bbe3b2bac51b27a7b053812ce7328751`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 232.0 MB (232018579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:212a73d830ab0b92b18e8cbf84be3782f05eb71b3585cfc4972e506e89f0e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ed3f02d69dfc33daecd485ebc91f49c38763e51ffbfdb0af353e52850d10cf`

```dockerfile
```

-	Layers:
	-	`sha256:5cc1ca4230ec1321146555a47b873ff336157ed260c1276614c188b9c5318986`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 2.5 MB (2484191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b867043e1d6c488b5c5d223e4c9ecc04d29793ca6e1adc3beb9eb6f869ada4`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2a01f256874fe08d6622c1c4148a9afb12d6038f6a29ea8ca23c3e11a2d4f3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257253604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5e75e9cc09cd39bc361e4d2b8e64571200b8bb47c18ba54a958f87f1cd9b62`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0e7b720b4a787789aac5e557184c66b65ab317270bbba3209c6bda6e001def`  
		Last Modified: Wed, 09 Apr 2025 09:21:28 GMT  
		Size: 229.9 MB (229899373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:462e6d46fb6eb846e68730e9bd133e2d289e006f642aa2f2644638b09689f180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49353fcd34f613c7cc888cb0499f65c41426e7333273751dea5013c36849212`

```dockerfile
```

-	Layers:
	-	`sha256:beb02cf1e3e9b171e4a4285e7a852b26301546628cb93cf507b7824863bedf01`  
		Last Modified: Wed, 09 Apr 2025 09:21:22 GMT  
		Size: 2.5 MB (2483918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9882ad674d8700877791d440700a20e9618bf3a683b901ed66dc69dccf8b40e`  
		Last Modified: Wed, 09 Apr 2025 09:21:22 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a962429c30667176c8232a8d13ebdd347fd3511592002b5f850c7db83f6da37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267685386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfbfe0c3986d5530752ec115f27578e0e38a35a623be5609f936869f3ce755a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f91757d648f86453351af5df59e05e10af027a7b7830e05e76a67647e16cbf6`  
		Last Modified: Wed, 09 Apr 2025 06:38:50 GMT  
		Size: 233.2 MB (233242690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5b6f1c3a05d3d1368cf4924d9f54fb0af747bb2cb2ff9887b822f4bbe5f20faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bffe315346a287b54fbcfbaf0ca1fa42367c5eb19e0fe8fcb9c590397d5c697`

```dockerfile
```

-	Layers:
	-	`sha256:43a9b06a3aead0d9b61cb6b7294ce205b2f9351601f94002d7a33184177dd312`  
		Last Modified: Wed, 09 Apr 2025 06:38:44 GMT  
		Size: 2.5 MB (2485632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93578ef29437b525abc13b91d60dd32f9fb69ed06fa8107f1186d8a8ce00792`  
		Last Modified: Wed, 09 Apr 2025 06:38:43 GMT  
		Size: 10.1 KB (10129 bytes)  
		MIME: application/vnd.in-toto+json
