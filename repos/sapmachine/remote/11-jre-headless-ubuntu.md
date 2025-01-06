## `sapmachine:11-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:267de6f06b55c77bf0310a40baa3e43761f09e79639b5c170b32388eba80c85a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:1f2ea9427379b5596f765a44a0423f53e74ee8ff4953606878099d29c7d35af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78951368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7659e50809adfb7d0561d2748fd04ddbd58fab52a282e85b1d6388548266a583`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f67f328e874b3f75ccbcce2054236311f1c707d60e41a5185797054bda9b59`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 49.2 MB (49199400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ef0bfdf59f9ec914990453d8d7ec980c02910998e24608e8974dc25a5f5707f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eb3d43e200dd9e070ac1f01a22d75283bb3a10d64b536a7fd8ddbbef5b6278`

```dockerfile
```

-	Layers:
	-	`sha256:07eb1c9f4c48fd032afe3716a4dddf6a4aeec8b5c65f2186c4a1cf43669984b2`  
		Last Modified: Tue, 03 Dec 2024 02:37:22 GMT  
		Size: 2.2 MB (2153811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae77cd667e98610fafbede61fa0549f1f7081093bc862415f79a99bdad45230`  
		Last Modified: Tue, 03 Dec 2024 02:37:22 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:acb00262b2dd5a8f84c138771f8fd001c3ccb1e8dd901ee27ffbd1a8f9779920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77410008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338db276bafa85ae91851803374a8dca82137762ac4dd9c33bd49a19361ab405`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591f9843753f2d3169270f25c44540b806d153c4da8963981684471d5bc8a60e`  
		Size: 48.5 MB (48517337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d691b030f1066f98e9b332c652e74a993b90af189c88a52a6dbcdf469054a553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ab181f622093c0b402a78e83fc65258ec108411488dfb6c0d118ac383b580`

```dockerfile
```

-	Layers:
	-	`sha256:c7dcd9f0a0cabea358818c104324d65d289f5dd30fceedf5a140d4ea7602db3b`  
		Last Modified: Tue, 03 Dec 2024 10:57:38 GMT  
		Size: 2.2 MB (2154921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982f2de9aa86338a7a9001b59a7b8ed7fb0c1ba9721cd1ca57591aaf8661b9ad`  
		Last Modified: Tue, 03 Dec 2024 10:57:38 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a88a2cf47243ceb32dd2a8196333185a9e929eb54a6c62f2cc4b057aa45909e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82149630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd617ca368781ad753ee6b0c47d7bac3968a35a4726ee70e21ea4e6b5e1e725`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9906cf63617e7a93610a2a658d8bd23e9c409db8e1b1985b6a68022b2989abcd`  
		Last Modified: Tue, 03 Dec 2024 08:50:03 GMT  
		Size: 47.8 MB (47760810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:33801fa7e453c025659bcb54cf8ecb4ecdf95020ea6c2207fe4a734b69d6db19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826c74edca27625bc346c47afe409993cc0d27e1920dd5da11893dca1f070e25`

```dockerfile
```

-	Layers:
	-	`sha256:1459c6dc8f6f83acff3fbec3d3f2cd7744d6b41f3e92822761e4661ee85acad4`  
		Last Modified: Tue, 03 Dec 2024 08:50:01 GMT  
		Size: 2.2 MB (2157703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f4df2b07455f3815b0bfa577d02c610e8614ff2d7cc186e60e0a2a14feee6f`  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json
