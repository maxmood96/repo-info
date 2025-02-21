## `sapmachine:11-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ca63489fdff1efd5b6a0424fec85bfe56460ae976d06102e1a0487e69b5974ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:593da175da8e9d974f285eed06c9e087eec1cf18a35dabc959c6ca38156f5326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78952005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7fc5d1bc6b6ba5e2eb5cdef199312062a096868afd824a7217790695ff37be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f54c17eb2e5e1029a447f4bf49c6e694607d93e829fc5bc6f47220ff3a0fd1a`  
		Last Modified: Tue, 04 Feb 2025 04:50:03 GMT  
		Size: 49.2 MB (49197715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e18bfdaf8e1d25c907533e57ea1f3785a7e3f43905d4e8d8340fb3aec7116e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b251609eaa940437dc81fd1e942fbca9af9e43a6d261c8f5e7fd4b4d0263a8`

```dockerfile
```

-	Layers:
	-	`sha256:ba8489a67c709deda23918f1caf0cb59a1087ac37a02d0d1526bfb148150a29b`  
		Last Modified: Tue, 04 Feb 2025 04:50:01 GMT  
		Size: 2.2 MB (2156933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33efd82a5dff2065db0fa5627b569614fcd2c3d437fd9045bebee4cbc70a764`  
		Last Modified: Tue, 04 Feb 2025 04:50:01 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; arm64 variant v8

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
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591f9843753f2d3169270f25c44540b806d153c4da8963981684471d5bc8a60e`  
		Last Modified: Tue, 03 Dec 2024 10:57:39 GMT  
		Size: 48.5 MB (48517337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; ppc64le

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

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

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
		Last Modified: Tue, 03 Dec 2024 08:50:01 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json
