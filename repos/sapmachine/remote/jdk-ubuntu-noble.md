## `sapmachine:jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:d322fa0ec4054f17ef5db0009799f50d91e373ca9ffc569fac4efe00734f2ec8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:102ebfc84c12816dd9a0ab10f2ad6b929ca42d93f4b8afa1c9942a3198dea266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252286118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbb021df98a4a2203ffe9e347d0740ad486de0704ed6acd769394fca00154be`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:19 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:19 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54212467f4e86991837786935847d5fcb18af2832e358678e4b6777f676f7f92`  
		Last Modified: Tue, 03 Dec 2024 02:35:31 GMT  
		Size: 222.5 MB (222534150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a902851e98c8cd50d009e7b3463735f884206547a1c423532dc11b762895395a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f8c750835e508a261a11cd25bf0adc5ccd00226f9f0f63257cdecceab3bf2e`

```dockerfile
```

-	Layers:
	-	`sha256:06f0b664b9677790f96db7dbf4bb5f48f809d829bf578acbacde7bea6f5c394e`  
		Last Modified: Tue, 03 Dec 2024 02:35:26 GMT  
		Size: 2.5 MB (2475792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e565a59dc50f8e730c18b0cd2b2f7992cfae69481c940a1dd57247efec9502`  
		Last Modified: Tue, 03 Dec 2024 02:35:25 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:78f55942b55d3c3b954d466e4407c903efa6fe4d04ec4509176f181b7d8bcb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249410049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4189e5e8ba048bcde329c06afb01be3419851972a0f4e114f88b209c91c29a76`
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
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dffde6282ed84e0ebe3a8a62bafa739319e9d0e19cb7225ff31a04095fb0459`  
		Last Modified: Sat, 16 Nov 2024 03:43:31 GMT  
		Size: 220.5 MB (220517624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1dee31c4335455b60ab096718e3ac7f5d0bfe853962462d8688dc352d5e97702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4f38055a9843c1ad1ff020e8bd2ca32e1fc9b59f50b8bed22fa935b19242d7`

```dockerfile
```

-	Layers:
	-	`sha256:8318399d69d783938a3f9efc3e5eb0fb25f17303aa862a941d2a4d733692b8b4`  
		Last Modified: Sat, 16 Nov 2024 03:43:25 GMT  
		Size: 2.5 MB (2475776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cdcea8926558231fa3dd0773822e3e2b7b714ddf26ae4b593dbd2cf6189b4d5`  
		Last Modified: Sat, 16 Nov 2024 03:43:24 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0ac73af273a7f94274e13bfde8cb18ad9be0c024beb4aa1d516b188fa8cf92b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258071305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b382451bb47bafbb75a87307f4ca7723a5a7f88ecd61a002ec1f2d6f28749c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bc5c2cde44542c4d1c048c701b6d718e1cbe53695e4005e26eb6198d1662ff`  
		Last Modified: Sat, 16 Nov 2024 03:40:16 GMT  
		Size: 223.7 MB (223682483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:19c150e5e07d13ce29ca3b69f1b069bff0c7f5f9021213d828d44f19ee712417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2490638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e3291b028c31050b6075e9c9c61c89998b050739ead46f3b991afe19a0543a`

```dockerfile
```

-	Layers:
	-	`sha256:0871e154d55fa4e13d22680241844159abb084bbc566957284bdc570f0f083fb`  
		Last Modified: Sat, 16 Nov 2024 03:40:11 GMT  
		Size: 2.5 MB (2477225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb4b38bc599ac5e5555383fc9aa7070cf48fb645fa1ae70b1378839362ee6ec`  
		Last Modified: Sat, 16 Nov 2024 03:40:10 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json
