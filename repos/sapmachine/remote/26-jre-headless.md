## `sapmachine:26-jre-headless`

```console
$ docker pull sapmachine@sha256:362bc61c990c887ac26858101bed7935e6225e0d60f73b0fe565102adf8f0f6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-headless` - linux; amd64

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

### `sapmachine:26-jre-headless` - unknown; unknown

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

### `sapmachine:26-jre-headless` - linux; arm64 variant v8

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

### `sapmachine:26-jre-headless` - unknown; unknown

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

### `sapmachine:26-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1829ed7f9a19edd722003d5feff884f557692fa2b921769289d494ce20488584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93093825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb4d86f1ec79bbd64728540b24aae4b70b6bc59468fe1182f1ddc1599628654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:22:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:22:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:22:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf37b78b31981032f66e306bb901837a2eb7f70f8acb9691d7158c83f84fc6b5`  
		Last Modified: Wed, 15 Apr 2026 23:22:43 GMT  
		Size: 58.8 MB (58779647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:98489880257ebe71a811b41980e341d59df1281760412882a99e692d37d14c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11a49610218e1077893025731a1f18486ff84aa8539737c18736d80dec6a5f4`

```dockerfile
```

-	Layers:
	-	`sha256:9c04a22473e804b3c423b931567193bb4e227f0802470d439ce97f2c716e71fa`  
		Last Modified: Wed, 15 Apr 2026 23:22:42 GMT  
		Size: 2.3 MB (2277831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90d119eb31604e9c12bd9f0582ba9309473cc3b1129679c75e1b3cf9e90e702`  
		Last Modified: Wed, 15 Apr 2026 23:22:41 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json
