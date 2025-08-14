## `sapmachine:21-jre-headless`

```console
$ docker pull sapmachine@sha256:a548765937d3b71e1fda642364f20e6665ddda204b6063f770f0efaf041e3c12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:c5abe1f2053cf1d6833dd951819792ad06c83581ee334c60d6a50d7f4f602a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88738758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fc09435e3d7c1ed64166cea1508af5ad9b73866c07d90d6d9c931fe58163bb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81c72abf83458292364cc107cbda4f477fd2c03ca809e3e40816e5502dc9098`  
		Last Modified: Tue, 12 Aug 2025 18:06:08 GMT  
		Size: 59.0 MB (59015543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32c6405638075ad03ff8e792c2291ab9ee6789c2c9331cead1123854d5ff51e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a25877bc9a2eb83b423069f03b6f7348ebce4b2070505bdeec984e8d023aaba`

```dockerfile
```

-	Layers:
	-	`sha256:d462f2924297cbc723c14cbf4613a52227410d77e3abcd763b32ca0bbfd94c53`  
		Last Modified: Tue, 12 Aug 2025 18:06:19 GMT  
		Size: 2.3 MB (2273850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f129e3057a661067791258f273cb24d274b6aece10501c65e6a34853fcb11d0b`  
		Last Modified: Tue, 12 Aug 2025 18:06:20 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e18db071aeb5bde2f41d65e60ce53197a5a9e5d11e4e2b077b45710b6737d2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87046881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0147861f097ae65275f49e46871a3e9b81c2607a78ccadf03833caf3493930f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc14555ecd73547111ca142cde542672a9add73f187d07fab159ff48e40d8cdd`  
		Last Modified: Tue, 12 Aug 2025 21:24:10 GMT  
		Size: 58.2 MB (58186504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6145520403f09958eda964d077268640ac3a685b65641975d8d8359a11518491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547e33c0a6c6f96294bbed37cf0a199010f892040c900dc4f14f3f3f3129b4cb`

```dockerfile
```

-	Layers:
	-	`sha256:1595b3f70a58995f05d1e0767f5ff1f48096b4db872113f013c8e063312c752f`  
		Last Modified: Wed, 13 Aug 2025 00:07:30 GMT  
		Size: 2.3 MB (2274393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a330450961cfb10b248a946b633301f5d26c74668d243eb0e3d3eaba8b10b5f7`  
		Last Modified: Wed, 13 Aug 2025 00:07:31 GMT  
		Size: 11.5 KB (11495 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7d33b7a6e3bb6772b579f1d7ea3516c4d9e42963b5bc8ca6997e0492792b364c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94386349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9192bcd971a469643441060bdecd02fd638c1df7c04a955ec1480acfce93e9c8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51dc6b6595c2f554aaca3ff90546f7ca50bcf495e414fd8779c97131831e49`  
		Last Modified: Tue, 12 Aug 2025 22:42:06 GMT  
		Size: 60.1 MB (60056699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b572380828cc4a6e88abf9632e39d0fffedd1e04b25028dc4d12797125ecc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba14677354f0584239df2a0dd7b47aea7aa266006a79cbaa299d0d9b2fda05d6`

```dockerfile
```

-	Layers:
	-	`sha256:7f0898274bf5519e3b451357befb6acbbbfdf9df9cab384225cbef00ac81afa9`  
		Last Modified: Wed, 13 Aug 2025 00:07:35 GMT  
		Size: 2.3 MB (2271868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b18cd2208dea94db06202ae5b327a3e9632bbee8b457925d4ad63921ae1e3d4`  
		Last Modified: Wed, 13 Aug 2025 00:07:36 GMT  
		Size: 11.4 KB (11393 bytes)  
		MIME: application/vnd.in-toto+json
