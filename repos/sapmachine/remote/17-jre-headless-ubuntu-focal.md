## `sapmachine:17-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:08c8e6099f3effc96fced3cf1e4f055523a2c06b3314d9d904f83091ec929f5a
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
$ docker pull sapmachine@sha256:c167a4d95186f6dc40a43788fd9ec7d27f5096e21776fd22136a4ad68dc35a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c6eb7cebf70163a1fab9d16a9882e5c645964a3da3bd3a0cc3e49572e829df`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b07d3aac8327e2674df722a402b55c09ae9d66f4aa101eebd7c577855c1a844`  
		Last Modified: Tue, 28 Jan 2025 02:59:41 GMT  
		Size: 51.6 MB (51590445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c4d33389db538aa799947dd5900c995299ab87b6983c6a4f4fe4af71b9853be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2070025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf6e63c6d6c0b0427320b787fc62c1aa11b8ac97156b30f261b53adf3bb39e4`

```dockerfile
```

-	Layers:
	-	`sha256:7f09d3f317d07981893d9c5683e45dea070a5f5cc3637c9798f5f446953659e4`  
		Last Modified: Tue, 28 Jan 2025 02:59:40 GMT  
		Size: 2.1 MB (2060989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1f91a4e94ef67a0c89590ba5138e8d79e92452620f0345555f449540961be4`  
		Last Modified: Tue, 28 Jan 2025 02:59:40 GMT  
		Size: 9.0 KB (9036 bytes)  
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
