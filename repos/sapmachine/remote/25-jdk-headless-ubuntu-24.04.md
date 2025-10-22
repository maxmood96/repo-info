## `sapmachine:25-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b55969ae690ba3899e516db217f879a28f6e972b03737493cf2f9e2452aba8f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:595d1dc85fedd4634e3e6290d9f889435852ae3bc50a0f0d41f09ccba9816b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262161705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92a4cbc06bfaf602385c58cf8721f0a90fdab8bdf2fe6bdf9dc2a0cd7b47974`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f6a60a4f74e809c115ee397bab387ca65323edb282e127167c46892ea8b661`  
		Last Modified: Fri, 10 Oct 2025 18:03:36 GMT  
		Size: 232.4 MB (232438558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4ff5251ea43406019dc9be07d1bd9c9be79622dc141e4782fcf23cb62b837bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5f25580acbfa9bfaf1672867d78760a08701a24af1574be065f438022bfc65`

```dockerfile
```

-	Layers:
	-	`sha256:597208cced67927945559b13d7043ca710c43bacc76153f4371e9aac07b4ecc7`  
		Last Modified: Fri, 10 Oct 2025 00:17:51 GMT  
		Size: 2.3 MB (2348697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d2ede034a4cb75b284a422a08ecca2561dc09024dc9ac5055ed0e6434112b8`  
		Last Modified: Fri, 10 Oct 2025 00:17:52 GMT  
		Size: 11.2 KB (11244 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed2f2c1f62014625fe80c0de1883b0077c07d1247230bb598f8ca79b0e16a24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245847547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ea7eb8bc586e9765f319f99c6da6ab7984e4ba8ac1e79121a153eea0cfed47`
-	Default Command: `["jshell"]`

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
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708fa1bf4c0e15388d0d6bc9469e005fd99d7708adbdf58c0e2acbe1ece51a8d`  
		Last Modified: Wed, 22 Oct 2025 00:05:11 GMT  
		Size: 217.0 MB (216985835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7475f99e41fe68a8636120a84023cd4931137a48a9787ec60bb1ba9a98de1aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94e75d89f56f7d5bd65f89755c73732df36ab6900fe449c067a50ccdbfbcbc`

```dockerfile
```

-	Layers:
	-	`sha256:add6266eeec23ce66b9462625a4e0129d71e80eb0c482895a33dc1e91b455fe4`  
		Last Modified: Wed, 22 Oct 2025 03:09:51 GMT  
		Size: 2.3 MB (2348773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ffb6e03231e7bb4e2a6242863fe5747200f5cce72503f1be5a21fab7ed24ada`  
		Last Modified: Wed, 22 Oct 2025 03:09:52 GMT  
		Size: 12.9 KB (12882 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a6a3f85198188f0ea7de1bd2c665c859be6decdd10e0fac57a662494fc1f1dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267415970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56249ccd574479a94753c6787d0e721811e021fd3d9a42f059849405936085d6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d229b20ff0927748171e337cba92c9361e3277178216a23381b750a0d3c06c9`  
		Last Modified: Fri, 10 Oct 2025 21:19:23 GMT  
		Size: 233.1 MB (233112445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ff94197475fc4ccb9c1acb95f6561554d0be459499c8da00fb4605085a42cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2355481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d2ee6addee98844cae59b5fecdbb8d2d47955bac2618a6750e37f488d35782`

```dockerfile
```

-	Layers:
	-	`sha256:e1929af568f5919529df14d8b34fafda3d6ccf59d8ed9ba511c7f1da057b9fa5`  
		Last Modified: Fri, 10 Oct 2025 00:18:06 GMT  
		Size: 2.3 MB (2344151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd1697aa56a53080a641acf54bc35a5152d1c8f15ff20a6ad97461f7ead54da`  
		Last Modified: Fri, 10 Oct 2025 00:18:08 GMT  
		Size: 11.3 KB (11330 bytes)  
		MIME: application/vnd.in-toto+json
