## `sapmachine:17-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:2ca4cffc8a51646f5f2bed79158650ba1404b27acada3511108cacfaf5e29b15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; amd64

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

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3a360e67d7a8403252400b37c041c1bf46ea7b811758e24c542f10ebb0faa3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81414017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9120fd74325c0b76f81baf329473a94b257fa43ae1501ac622a5a54bfac17f52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329f5c6cbbf923fb4e63de5dca0577098c92d9ccc2fe2d6dea8e19e18b78d86a`  
		Last Modified: Wed, 22 Oct 2025 00:06:26 GMT  
		Size: 52.6 MB (52552305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25c014ec3828379116942b17f0adc51369466096e0da799c58580aa8ebc08a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693cca02f6e5bd8651588cc98079f183fe6857002201deac9196f261023f5207`

```dockerfile
```

-	Layers:
	-	`sha256:c68f05afabb13c2fa34d6b66add247969d8d9e287bcc62d48e9607dd4ff0d420`  
		Last Modified: Wed, 22 Oct 2025 03:05:20 GMT  
		Size: 2.3 MB (2272071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:510af0c56da040bb90f1f6c176c2b92b67a7245569c1c53a0ae17d1520523dec`  
		Last Modified: Wed, 22 Oct 2025 03:05:20 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8356233423564fb0eb5280c18ffbe509eb9e789d9223a43a1610ad7f92dca623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88369257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e34121b76045c65c09b8c98783ba23cec27beaa6993b6790785927bf47d3b`
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
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
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
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfa29dcb181368bb9a0a8c11a3b6ec7afb469dda0bbfda4667e04a38e9c56ad`  
		Last Modified: Thu, 09 Oct 2025 23:03:11 GMT  
		Size: 54.1 MB (54065732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0ff028719dcb6e8ad915b20f173702b3f094078b6187d6c35d1d6700fc198ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2499540bee2e50a28e90dba530ea576a041b02bbdc3818d5419f835e9f4678e`

```dockerfile
```

-	Layers:
	-	`sha256:5b720a5514837b66eaf97fcb7b3c1e0dd5f2b9cab7d1bcda3b3d48999c67b720`  
		Last Modified: Fri, 10 Oct 2025 00:06:54 GMT  
		Size: 2.3 MB (2269564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6605143c35eadd2126404e03c5bec4d134ebaac6dda08d75d192ba8306d2d6`  
		Last Modified: Fri, 10 Oct 2025 00:06:56 GMT  
		Size: 10.3 KB (10339 bytes)  
		MIME: application/vnd.in-toto+json
