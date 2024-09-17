## `sapmachine:21-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:a97911fd7e72a159fe4ee60bf834d14e99d426f888d011d263aa529c1b31f6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:29952a43d32794bafad1f3ea5ead85366b837776f1dbb848968c20022e799e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243533382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc525f377c0a0d218852749a1904e8226bf4d03e2a3b86763396f0a979388e81`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32aa4e2de54fcc083c4024715e825e2e76a128bd7ced1088e25f9ac789a21b`  
		Last Modified: Tue, 17 Sep 2024 01:00:56 GMT  
		Size: 214.0 MB (213997694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e93a79ab16758e093a29e14b757efa6b8e6be1ff7493e9da04954db490aa6268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b411ae1ef2d0d2bb670216b26b9ebb12625d9bec5eb1c2a9c6f9d947ec4e295`

```dockerfile
```

-	Layers:
	-	`sha256:7f4a1f75363d9b0f63466ab83a6a02cf6f518f94b9038616a27cd3b8b78395f8`  
		Last Modified: Tue, 17 Sep 2024 01:00:53 GMT  
		Size: 2.2 MB (2231168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0716496376ba863b707ca9312ddc22570ea7f04e1b021172e467f646dbcc7209`  
		Last Modified: Tue, 17 Sep 2024 01:00:53 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6fd03153206e580d07411ffebc6a2d0b75fc43145a4b7700e399f7f96304c631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239408008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd563cd35c2e92d65913792aac4f425bb941231c0a4bd3f501f5f0628592fd46`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab8206e4b51321f554ef188fb7bef35cd36397a3bbc63b17b131d67256c4ca`  
		Last Modified: Tue, 17 Sep 2024 03:22:50 GMT  
		Size: 212.0 MB (212049679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be1fee7c2b1a6ed6169ac8870d35b667fafad4dfcd994ae991d471b4d3c4b61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723e4383261eb624683011ff56a6153f976f619f89169bc0054002b521241da5`

```dockerfile
```

-	Layers:
	-	`sha256:1e95f4e56c3554cf6f8cda3dd24d52410590434ff1ed6adb68c4e92f3cd8b850`  
		Last Modified: Tue, 17 Sep 2024 03:22:44 GMT  
		Size: 2.2 MB (2230862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a56aee26c0269829566f2976ddbffb67f80fe0f5443a6ef56c3ca637e501de`  
		Last Modified: Tue, 17 Sep 2024 03:22:44 GMT  
		Size: 9.7 KB (9699 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f0e8f9abe7f758fcc5dee67f017469ee0c5c1b286d7754bef1d61897ae5dc8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249591955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf1573075e803bf8912c895081c97ed03f12ac3a6cf4783a1709279634a8f25`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec0c36135d4d92c9052ae53a3aaf4f8521e2ccb2e7ef6ce72b6cc2a3074d42`  
		Last Modified: Tue, 17 Sep 2024 02:39:29 GMT  
		Size: 215.1 MB (215143713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4d12d824bd9ae0b95b38bc90d37b8c29f0c5372d9e2d57a75eed61f8b7443bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fec05c2938c572fdc04e7ea90441ee88e3101308ff97594ec6bfb4a3068041`

```dockerfile
```

-	Layers:
	-	`sha256:b330a2bde5a5df1958ba561c0bbeeff6036777737b3842fb287cbc8cfc317084`  
		Last Modified: Tue, 17 Sep 2024 02:39:24 GMT  
		Size: 2.2 MB (2233140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d78f4dfd5a3ef69238e781d9a00867a34a2037811fdf828d93d8861a2310e4`  
		Last Modified: Tue, 17 Sep 2024 02:39:23 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.in-toto+json
