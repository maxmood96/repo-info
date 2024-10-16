## `sapmachine:lts-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:aba35cf7e2eb508ab5b766f55b2ba63079068f48cc7af941211e2e1dcee1ab60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:ac5375bcda5c79fb787207e79ec59159f02ec97096878649d440b22bff459586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245348883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7166c8e1e127b1daf19482c44efef13a97c670e856eb0b4f7136fde4023bdf48`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb619f111cd9a79835f8ab624a1b4713d2326306477299d9d2eaab9daf2a4571`  
		Last Modified: Sat, 12 Oct 2024 00:01:24 GMT  
		Size: 215.6 MB (215598426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:42ee0247575309d01901e88231544cec3b89c839823f911a9bcc7a8da8cceadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6cb3d3efe4069ec3f96b4f9186e262e251cf99ac7473c92a4c414bbadb3bf3`

```dockerfile
```

-	Layers:
	-	`sha256:19697f0d6ae85f115f9d64b9f47858e9931e0306721f1830cdfc99da970c257c`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 2.5 MB (2452815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b9fbe946a28e4e879106b1e1e0e240e950bf939f1934f76758b31362fae704`  
		Last Modified: Sat, 12 Oct 2024 00:01:21 GMT  
		Size: 13.1 KB (13103 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f3170221a88d40db8f2cbbceedca4e446ecffd62e2e46d1f4dea6f81a2cb4770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242588022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16140bea586157585490ea3a6162975711e92351a956560776faa368a0a7d654`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a28fed3dbf5968577de47a9c486a1dbcb073d4158f9b6cc0789039454499f5`  
		Last Modified: Sat, 12 Oct 2024 02:22:41 GMT  
		Size: 213.7 MB (213702406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b218fdf10b59fb534d7f331d976b790f4f2fd9ed8c8e4e2e27f91ef547898764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e8f3c649aa0925b3cdcb941afc8affb4c6715f57fb89d5b2041312b1e829ea`

```dockerfile
```

-	Layers:
	-	`sha256:543caf13609c031a4962a7fae26162952dd57af2449a8bd6b4b0c7d60b47ffb2`  
		Last Modified: Sat, 12 Oct 2024 02:22:36 GMT  
		Size: 2.5 MB (2453450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f9cc82bd4f76dbb2e19903b0862ae7bfbaaa2243909798905d0c55a11f47d61`  
		Last Modified: Sat, 12 Oct 2024 02:22:36 GMT  
		Size: 13.4 KB (13369 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2534386868c882f8dd9d6b098fd4063bc06cf4b1cc6c6d55eb7cb02d4e818ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251438879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d94a388e3a914512e4717b3799f1324dc40f4375cb13d3afe3eca43696a739`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29750f447a590bb81eae87e86e790d6127a344368f944b0836fbe6ec216551a`  
		Last Modified: Wed, 16 Oct 2024 02:45:21 GMT  
		Size: 217.0 MB (217049910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b5b79ed5fe1ac115f833b2cdf961e531d04660ffd6cf927e9ed9fcc05fd1f707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff02bb27ce6c16e70ed7010205db8c3edc17910b6f29e1f465bcb1c186726069`

```dockerfile
```

-	Layers:
	-	`sha256:70d35c5e367f434a81dc95cdef1a74251c5c1cd7484b4899ea9d9a3e14b24eae`  
		Last Modified: Wed, 16 Oct 2024 02:45:16 GMT  
		Size: 2.5 MB (2454887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b079842f52631fed9bfa41cf0687e500be9875f269ad5efaed38cdf65eb12dcc`  
		Last Modified: Wed, 16 Oct 2024 02:45:16 GMT  
		Size: 13.2 KB (13225 bytes)  
		MIME: application/vnd.in-toto+json
