## `sapmachine:17-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:a01ed719f93a7b6ac563241e4c3e9c432e258ce7da992d00c51b60ce94ad2f43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:1aa0dd6e87647ce6ae334534e20faa71e74e8226e1372ad98240e395f791a9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79658953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e669eef2f94ccab3562f7932515f2f15bc54e3f39fd0bddc43986c182ab67484`
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
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d41784e40727284e49db3556c8ca6aab30ffa3c48dabe9fa77b1d22376df70`  
		Last Modified: Wed, 09 Apr 2025 01:21:48 GMT  
		Size: 52.1 MB (52148559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3c543ecabac710dd32f961d5220edd3327ed5da5d7064b8744ecb978a804559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2070357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c76bb56c4fb951d98762b0073d7b3154fad36f9965cc68b8f133183bc1c2871`

```dockerfile
```

-	Layers:
	-	`sha256:62e0e3c65d66102a06432672aa46ecd0e2e0e1f6e6a75d5a8deced058da45103`  
		Last Modified: Wed, 09 Apr 2025 01:21:47 GMT  
		Size: 2.1 MB (2061426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6da6d0d3d7302f98ad9f59558fa19a42948e0024b90ce88c3f59528dafe182`  
		Last Modified: Wed, 09 Apr 2025 01:21:47 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c0f8024e312c19e76b2218b1bd34e2a1e7b713ba360d8a9b52b7e5a06f7bbcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77568708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1887937910b84c6e13c03212416cd7bd18f04d00c2aafcccedf011da9b9e3cd3`
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
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512e855355398a9b13648c9a55d927794d532e028217a18d694a128f9b527ff0`  
		Last Modified: Wed, 09 Apr 2025 09:50:12 GMT  
		Size: 51.6 MB (51591047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:806dc57a03ae76864df4090b4783aeee3d7432a0e57b418de8e80f0b555f5375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2070090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dee7210a83af9ba5e1fe1fbcefb375c98a496dc0e362fb3c1e9f6ff10e68499`

```dockerfile
```

-	Layers:
	-	`sha256:e7e15bdad444af3d6edab33365d6bc64b6d7096efe23ee6f95481f41c6d4dfd6`  
		Last Modified: Wed, 09 Apr 2025 09:50:10 GMT  
		Size: 2.1 MB (2061055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a6d3c24c615d4b7972e98b3eae4a5203b0ad69a5830a291ef190d29a787e7f`  
		Last Modified: Wed, 09 Apr 2025 09:50:10 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f786d89e148b55ab9b8079d6d6660be10174e72f97f34a809c567be44922a039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85206765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743e2f70caf3e87cae1687d1d652eec16a5ec91da5bdd9214841ae213768ebf2`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:055d08940bf119e83e4a9ec6ccf44e14684eed978b663d08c4781abeffbd8861`  
		Last Modified: Wed, 09 Apr 2025 07:28:34 GMT  
		Size: 53.1 MB (53129819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b1f5e563dc80d5c54cc21cdb1204078cf99b88d7a3422c34946ac307323faaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2074105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cbc5cd6a37aad0ad2af71e5a846966c6d8302427416f1c9c68cabd1829b917`

```dockerfile
```

-	Layers:
	-	`sha256:6dd54cb1c3f551f76f3c53653cd9203ff4e17ed09191ffd88c39837cddfd8ab1`  
		Last Modified: Wed, 09 Apr 2025 07:28:32 GMT  
		Size: 2.1 MB (2065130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b34def4cfa781208ace892fdf16f1f73fd2e75221ffb14f08ba9df556662cb4`  
		Last Modified: Wed, 09 Apr 2025 07:28:31 GMT  
		Size: 9.0 KB (8975 bytes)  
		MIME: application/vnd.in-toto+json
