## `sapmachine:17-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:28afffb52096429361e2155d6e79f9d593b2c129ad6c1684820194014ec16eb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:abc03d9bfdc4a64f0412f58ee143d6e7457edd24479e7d60fda97861707090b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82782084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ea72397e4fcdf09628c474ef2ca62b1ad8e8ccb84325b973efacf1d740acdc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70be12e3b0dcae673376995b3ac7e2861d63e98a57fdaad3bb129836b514458`  
		Last Modified: Thu, 09 Oct 2025 21:28:09 GMT  
		Size: 53.1 MB (53058937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6fbfc2e2506f5cd772792ea9ce7855799daf0f73e0be2b39c55ac39addb36114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fccb2e8e3c7eda7ad3369c3f07742ec1850009c78ada72bd032000c9e1575d6`

```dockerfile
```

-	Layers:
	-	`sha256:cba1364785503007bef7c9b5680c9214b1e911ae6b6b447adf295a2fa62d557a`  
		Last Modified: Fri, 10 Oct 2025 00:06:42 GMT  
		Size: 2.3 MB (2271564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8386fcff7237fdec2db50a1efe90659b03690449fad38d7f22cf8eb02aabd0`  
		Last Modified: Fri, 10 Oct 2025 00:06:44 GMT  
		Size: 10.3 KB (10271 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6c94f0993be259b341411ec1f29f488450feafea94865138e569e7d56bcf817b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a4afc65a4011ce5cbb47b949ee9d662e6e4353a8614632c728aa3ac0cb9387`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4250cdcc9cb63be9d15a684b1fb1b0a301d188dc3da8ea82904a95b2c398325`  
		Last Modified: Thu, 09 Oct 2025 21:28:08 GMT  
		Size: 52.5 MB (52487639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d9a627e797b2f02eb4d1a1dc5a2e5f00c9f7327bd1f90a9f98f3b097ffd95c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e3f33529c2cbbb03f59d6af61831022834ef245a063c3ac7fb648013e34b49`

```dockerfile
```

-	Layers:
	-	`sha256:aef484fba67c103aca278733062f9461bfab4329323f70aed4a364d822e9404c`  
		Last Modified: Fri, 10 Oct 2025 00:06:49 GMT  
		Size: 2.3 MB (2272071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7e95813ca7293a6ac7630fc8b1d458119cacaf9787ccb634f90b38a91af43e`  
		Last Modified: Fri, 10 Oct 2025 00:06:50 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:08abd169508927480fefd4c3c03c9125bf850404a92f57559c6104a8f31292e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90993559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a374222491b4b6b258c92d26adc52e2b8257eb14ba9cb03d65a8a4a422115dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f798a61df963ba3097a5728a4161f7f50cab989b986ea1fcbe4b36efc1bea63d`  
		Last Modified: Thu, 02 Oct 2025 04:46:58 GMT  
		Size: 56.7 MB (56690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0d53e111fc059a20de60ee1fd6e758ba617536df8cec79c75e8f6453c368f0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616f88cd721169b9c29de09a50b944f118726ca98c6f1efee7535c3bb659c9fb`

```dockerfile
```

-	Layers:
	-	`sha256:8fceebb55a6213a79ad33ec3e1df9249d0059ea4f221e85be9b888b93669eb12`  
		Last Modified: Thu, 02 Oct 2025 06:05:29 GMT  
		Size: 2.3 MB (2269564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1377935d881fe3650aa28ae4706d9d1154f371c89c79117aa58adeac052971`  
		Last Modified: Thu, 02 Oct 2025 06:05:30 GMT  
		Size: 10.3 KB (10340 bytes)  
		MIME: application/vnd.in-toto+json
