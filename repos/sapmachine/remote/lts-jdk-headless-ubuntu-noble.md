## `sapmachine:lts-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:0699fb39852073126fa8611780961652268876b582acedd0d16e7f04aea599c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:8ca8dfa3ea663f851091717bcebd1dd6e46eeb91f78e5ae8792165a401623295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248958697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d443137d3d8d5eb7ea1a336173b22a034714a8fd5cc39a535474305caf008cf6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c5eb071acaa435cc2efd77295b3caf7adfdd85f93c632bfcb0d4ba1a06ee6b`  
		Last Modified: Wed, 22 Oct 2025 06:24:24 GMT  
		Size: 219.2 MB (219235550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4cdce88bfa8a139f7c78dff575fe8f66dd2fd324981cdf4bfee9eb559f82b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fafa444d517ea8072736b3d3e2f3cdea118a8ba9c84522f1b1222d882277a9f`

```dockerfile
```

-	Layers:
	-	`sha256:b277ac628413be889ca9ba8a85830e06455f9c2382893ba253edd7f7a022e136`  
		Last Modified: Wed, 22 Oct 2025 06:13:13 GMT  
		Size: 2.3 MB (2348185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc6f607bb23ff66edc0b16a302475d47a7431aa784b59f35f664246dcbeb114`  
		Last Modified: Wed, 22 Oct 2025 06:13:14 GMT  
		Size: 12.6 KB (12646 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

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
		Last Modified: Wed, 22 Oct 2025 06:21:28 GMT  
		Size: 217.0 MB (216985835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:lts-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:01f365962946e0191b2a8a54982797def0d3548d812d792f4ffa4381c179345e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254183347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5600180c008f7620e34ab3b68ff2f400602b9a40de515c07afd0d8aa2fd4d0c5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca34daaaacaa7292f2f0dc373948e5c979c26b983977c2c7771785e598fe750`  
		Last Modified: Mon, 27 Oct 2025 03:35:16 GMT  
		Size: 219.9 MB (219879822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd931eea5296e432edd1103dc1b1e163d9372418ac642103944e9f3c2f87ada0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8e1d489989b456c868bc9a36398d02fc42b032c57aa90ebb6ef68f01eb4e6e`

```dockerfile
```

-	Layers:
	-	`sha256:f93b7278d4582e5dc569757d7dc6018b5f0f44d95172b7a2d3b7996f7e76c2c9`  
		Last Modified: Wed, 22 Oct 2025 15:10:06 GMT  
		Size: 2.3 MB (2343663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64dbe4912b78a92538378a28c17ddb5bc1cbc7c441993712c31b384370780fa3`  
		Last Modified: Wed, 22 Oct 2025 15:10:07 GMT  
		Size: 12.8 KB (12756 bytes)  
		MIME: application/vnd.in-toto+json
