## `sapmachine:17-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:57581c7615610e8d99a7af2c035ad6835018640fb8cfed8c84b52737c3a73144
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d9206cee08edfc696aae995b18745311792ccf1f1ffd494ed364ce788b722de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79670974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5bda547e1c3302e2ab4277181d711178fab0bd49aceb0945000c1d04cb1de2`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:6f5bc4800e11dca15240d9f8a6816e4e9d9d336544d41ef19a6d2ffde46d5a34`  
		Last Modified: Wed, 16 Apr 2025 16:14:19 GMT  
		Size: 52.2 MB (52160580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:92eacd5cd1dc17721de64313955b825aaedb3affa92ad8019873a024e3c0bfd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2070358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360a6def73c20aaafed912b7278e86222b45a5ca222748e52039202563669da`

```dockerfile
```

-	Layers:
	-	`sha256:97f2521e652c56fb8da14ccffa50e42c842b45414f4a02f8f1fa6a50bc011e84`  
		Last Modified: Wed, 16 Apr 2025 16:14:17 GMT  
		Size: 2.1 MB (2061426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27151e82955e92e1be075451b57930302f03e0c92cd9e32e0fed17f3727cf3b7`  
		Last Modified: Wed, 16 Apr 2025 16:14:17 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:08cbab7ed7766b64c55322792c2a713032299d30a401f6fb3f03b88a633be3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77581323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a4486bff0390c72d2cb214dcee7262e57f76a131940ab53dc960d1d776da7c`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1d5b326470e8f6caa1602b9bcaf5af2da1046628c2bf44630445346d23cf1b66`  
		Last Modified: Wed, 16 Apr 2025 16:46:36 GMT  
		Size: 51.6 MB (51603662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:44760083b387fe95ba8dad4675fd017c65003f1ebb3e1341b2d79fd67c93e02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2070090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b67c8fa5de7c717c5d92c5ff902d83636058347d0b92c2f67891534e05c886`

```dockerfile
```

-	Layers:
	-	`sha256:8cc3554f05ae1a5ec32b857af9e413719fc58777173d20658b719fae3043c80a`  
		Last Modified: Wed, 16 Apr 2025 16:46:34 GMT  
		Size: 2.1 MB (2061055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cdf823a2b9eb0beb925ba637bc4eacfc1853c9c35263f07d81d7ecc7cd49a05`  
		Last Modified: Wed, 16 Apr 2025 16:46:34 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; ppc64le

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

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

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
