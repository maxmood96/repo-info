## `sapmachine:17-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:29729ac327d03fe480ebad868e5078402ea48f716a0f0f6718e37611cbddc1a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:58974f1109374478953b54a0220434d898bc25e28e532aa01ad934f543349f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225866002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a49b603799b3c3095268998112bb4b6a6327047b2b97acc8f3d69e334328366`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5d45d9c585aae1401cc0f65a74e945a74e826ba45324b8a5317e8e6a06aa1e`  
		Last Modified: Wed, 16 Apr 2025 16:14:43 GMT  
		Size: 198.4 MB (198355608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b7a91c80722a61b1ad3dcc5611d6e3a56b07a340c394c365b67c5232a0a46af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6f6710426d62ced9e79543cdce4295e223370dd292095ba16bf8c48ad0fed`

```dockerfile
```

-	Layers:
	-	`sha256:155ba859b82a44f650ef66be38dba78d480b8f845e3db8ead1a7bfa2fa362a89`  
		Last Modified: Wed, 16 Apr 2025 16:14:38 GMT  
		Size: 2.1 MB (2144334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ddb8be409c8e6e59d81d28df967fce5119e580bff251dbf6d7ce684887f99f5`  
		Last Modified: Wed, 16 Apr 2025 16:14:37 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:51e64e893757e6e7e9a660daef2f7c0ce2b7cf1cd1f2702d93a9639b2b0e2ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223086603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31746c204eb314cacb14a36f69c7fdd0edc6e58c635116ca6b8eacd90f20398e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69538eb3816e7c091d8d5668733cda5860ad55177ee79aa51966312dffac8d38`  
		Last Modified: Wed, 16 Apr 2025 16:45:03 GMT  
		Size: 197.1 MB (197108942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d17e8f2ec6f0ac15c06e567fb588c83c8bd9e763e57f19926970a5090311b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a635b3903d67579199e748bc7556eedb6e5d5115bef3f543e5854be42ac85bc6`

```dockerfile
```

-	Layers:
	-	`sha256:9e52fb6db5a9790375d734c7d527ed5d1fac48c1f1fb54456e6e2f0b60c76eee`  
		Last Modified: Wed, 16 Apr 2025 16:44:59 GMT  
		Size: 2.1 MB (2143963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef7a0d9b58c29b484952b298a11f0381aebc518c78e7a417118ea8df352739e`  
		Last Modified: Wed, 16 Apr 2025 16:44:59 GMT  
		Size: 9.0 KB (9036 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f0b6d42ea2bcfa0fc4263522b733cbec6bdb59bab377a56f1f0511ad3dab2634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230881440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c999886945ab388f63343ead3d83f2e87dc045412c52756385dbcc2f76a01d4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc669c7b4e0f5824f56de4c33403a2ba51efb205a85c876f22c11b255443b628`  
		Last Modified: Wed, 09 Apr 2025 07:25:03 GMT  
		Size: 198.8 MB (198804494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:49163a61e5684c4323c4c410428f38995ba66b2c3922ce4323ae557181a3396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de01152049c3b340723720573d8c6fba21d1dfc3f00846bc59d3a03de0e3e369`

```dockerfile
```

-	Layers:
	-	`sha256:99a6fc3eaa436051253b8030b553fc77579b5aff528602733da3dfeea5b76d12`  
		Last Modified: Wed, 09 Apr 2025 07:24:22 GMT  
		Size: 2.1 MB (2146092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be72a60708c22344f9b8982be692d4105ffef473d8dfb0e2bb07a011f288778`  
		Last Modified: Wed, 09 Apr 2025 07:24:22 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
