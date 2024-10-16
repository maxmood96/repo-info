## `sapmachine:lts-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:003fab8bed82e2a3c6f7f01ed19f59913c15bb1e2e35c0340d3bc82d91faec37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:48c3c061432e142edfc689730936cfe38ca04cfea3a87ccc6f4225113f067d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245348685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae56b25c6e6bf6f267e34945228df4976a6965778d7975fb2e54a7689195f218`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46909f55793d3c8be1406a2209eb718254a19d146abb6f6f094c6efc0b8b998`  
		Last Modified: Wed, 16 Oct 2024 16:18:12 GMT  
		Size: 215.6 MB (215598322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8f55a546257d7f3f87462db0af4cff9f3fb016ed681be43da10c106c9da973e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533d82dfd048ed18069e593418f5485d30a520b32a2b87a7b9c95229022148d6`

```dockerfile
```

-	Layers:
	-	`sha256:d5504aa4c88ad4124e723e29fad74e143e8941185ec6cdc85d165ac48be81c8b`  
		Last Modified: Wed, 16 Oct 2024 16:18:05 GMT  
		Size: 2.5 MB (2452815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32dcf16ade080ce36df1297a9914b817a4c287c4cc2b3f1eaa7e93a69cfd135a`  
		Last Modified: Wed, 16 Oct 2024 16:18:05 GMT  
		Size: 13.1 KB (13103 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:dea203b1ee37863c069cc5413318d50fb8d192db9fe07d482ff444d33657b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242588161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea2d0e4af4535384d1fbe3d7f8a285e664e3abc5b57a85cedc8e68074a15f8f`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d486aaca535484d6a5bec6a0457215b55c12108c8af61866b415b275a4e7cbd`  
		Last Modified: Wed, 16 Oct 2024 04:29:04 GMT  
		Size: 213.7 MB (213702316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ab9c2ccc30839b6b12fd76a63d228bf9b683875d4ed65999f18e8b3217d0ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a428224143ae18dba409ed6e9bb7112cf02182c25c6a94b2292abe070da3b2`

```dockerfile
```

-	Layers:
	-	`sha256:11e1a0dba7cf08cdbb251ce9e033bf954c27514dcc9772e84dce68f5ceae5f88`  
		Last Modified: Wed, 16 Oct 2024 04:29:00 GMT  
		Size: 2.5 MB (2453450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2388adef707b9f579c8cc085bdb4ed00c8e27f8d67d1f84e29f4fdbe6e2ddf93`  
		Last Modified: Wed, 16 Oct 2024 04:28:59 GMT  
		Size: 13.4 KB (13369 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:lts-jdk-ubuntu-24.04` - unknown; unknown

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
