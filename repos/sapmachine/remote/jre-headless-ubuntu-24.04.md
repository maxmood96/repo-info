## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:3100c0e6de1d1aca4fb844faaae1ca6c6501eb188aba6e13152667d50ed1dd66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:51bd029dbf8786901c582ef27bde08e713c2c28268fd691acc4873d871828491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87537527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88974b07298ce89e7b7d5c3986a6de1d412438e78baf70f0d2c3c6c95ae25228`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:57:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:57:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:57:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84e305af4b5d14dc4282cd74f2f8bfa9452741d3227cf15bb6b02a91d721ca7`  
		Last Modified: Wed, 15 Apr 2026 20:57:33 GMT  
		Size: 57.8 MB (57804549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fcad23cbc39e909d205392b34e95f6adb61c1bb68cd97144617ac9f9d5f7ffc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7659dcaad69c7459eab9d1aea728f0756f3d4b19cfcb8fa5b2b2dba3bbe55335`

```dockerfile
```

-	Layers:
	-	`sha256:aa853515e7ff52cf3650dacb37822d9a2ca5261efc4e18295cec1243cc9cd4a1`  
		Last Modified: Wed, 15 Apr 2026 20:57:32 GMT  
		Size: 2.3 MB (2279044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13cda348b7ef802b1d3042769ac95abfeefce626eedf111182b5f875764d6b1a`  
		Last Modified: Wed, 15 Apr 2026 20:57:31 GMT  
		Size: 10.2 KB (10152 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0ae3c21f3f901333a86e5a408ff95305ec4e34592f141b7467168bb0ab4fcb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85685254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eacd60c7814620d05276152a015653c9a86b0468e9ec391c73b149531c990b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:06:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:06:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:06:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e23deb1158435f7d339fd4abc5e566480648de244f9bacccd7cc37f5fdacca9`  
		Last Modified: Wed, 15 Apr 2026 21:06:24 GMT  
		Size: 56.8 MB (56809469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ee97e0236f8116bc291cbd611a3fc5de3066e01615966e0826fa4ed0540a6d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36823881e580ef80ca24a015a12f471ba97c4965c2d5faf9a28ea5b8c2f1f88a`

```dockerfile
```

-	Layers:
	-	`sha256:8d0fe14657e77d334d0372d3bec36db225ac136ae0fccabdf8b926ffdce4f40c`  
		Last Modified: Wed, 15 Apr 2026 21:06:22 GMT  
		Size: 2.3 MB (2279548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645288d681524f9a7a4d2489bc5aceac19ec05dc36d086fac8bd524f589a5f6f`  
		Last Modified: Wed, 15 Apr 2026 21:06:22 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:14b35e502103397cc2207fb5eac4b2751262ce16e03a30982e5bfced186e431c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93092786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c13dffed96b26d26a080333c34bde65edaf0b2e1c745c05c47b4c1ed259807b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:02:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:02:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 09:02:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f98154d322f56db364a8050c7a741355a27a4a4cadbc8c09ec238f7b379000`  
		Last Modified: Tue, 07 Apr 2026 09:03:09 GMT  
		Size: 58.8 MB (58779452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bfdae44850fee740ae21e8c982ced17110c5daee2e043cfe068bc8a4fdbef49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ceaa1e80e071c36978459260fbdf8ff090110f787a6f948ace5f2e2df9b565`

```dockerfile
```

-	Layers:
	-	`sha256:54ad142db09a3e98da44c6c82e37439700f64fa7422a9c4c7e1aec48fcead88b`  
		Last Modified: Tue, 07 Apr 2026 09:03:08 GMT  
		Size: 2.3 MB (2277831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bca651b7e644494398e5308d8a080337f987d24c6682b2dbf86583f3cf833a2`  
		Last Modified: Tue, 07 Apr 2026 09:03:07 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json
