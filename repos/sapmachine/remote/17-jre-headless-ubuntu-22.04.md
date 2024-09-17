## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:90ae6a2f936b4dc0b47e793104a6dad335d343f2ab977176d332bb43e5d0c2a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2f4b5b0c2aca64f616df24bb4dc3c09f1d3e0ff04e895e6e4d536b19e1c74c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82020940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeb59fb025cb651815d258a70d57a29103dfdc5bbd0340ea8de509e131b203f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dc623a25c77c829cd9c99a3ff1a223b88f2b3986a8af905aed5bc84ae14161`  
		Last Modified: Tue, 17 Sep 2024 01:00:44 GMT  
		Size: 52.5 MB (52485252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17d5f97c6c66637d194a8229a0a28191c8fb4d983e684283bfce0ef671d8bfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1f917e3004fa7bdee3bc9970353476cfb94e086fee4ed073d19d0e997860e9`

```dockerfile
```

-	Layers:
	-	`sha256:8c9e80900b9bdfa3493aae56a2059a87f27676122bb357dca5e04334a00295c8`  
		Last Modified: Tue, 17 Sep 2024 01:00:43 GMT  
		Size: 2.1 MB (2144916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890c03b7de295cd58c8a7b2608089d910e14f3979deb6350ea9c36228d5145f6`  
		Last Modified: Tue, 17 Sep 2024 01:00:43 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3702194ad476396906bffc79b715926e0b2650c334e70faed6fa5b2744099da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79177410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56a6a1c023cef49c64604b79222e1fa5578a78ed956702574b8fb7ce2152256`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae31c06fccd1da883ae4bdd9736e552b707fec535a1e20f440671e8a6a71d2f`  
		Last Modified: Sat, 17 Aug 2024 04:36:50 GMT  
		Size: 51.8 MB (51818727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c114019fc4814462e2810244440f33012157b4240b2bb21535d6bcb9c5425266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dca58e715b6905da2aff0db381abd7571230d3001cb459ab39f401a29ad901a`

```dockerfile
```

-	Layers:
	-	`sha256:992c8c05e38b1d2fe2e25d944b19e9a42cf36cad76cf6db72a23f7321f986a78`  
		Last Modified: Sat, 17 Aug 2024 04:36:49 GMT  
		Size: 2.1 MB (2144586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8609733a404f99f04d36ec70606beed01e7f830e2afadeca6b11e05cd8b7d903`  
		Last Modified: Sat, 17 Aug 2024 04:36:48 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:33522213a981fba6bafd52feec6b93be586d20ef8176d8fdee16b3b2b2134a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88265451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a9c5951f897eb0431874e47ed40068431d3383d533db1f41000269b0795d8a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c687d6e48e595eb38db7e9226a48e4afaaa7af6c9f74467fbca0d6d844bc483f`  
		Last Modified: Sat, 17 Aug 2024 03:19:20 GMT  
		Size: 53.8 MB (53801273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:82e57ea1a4c9092f63b064e70462430518f689ea7e992e4707accc4ca53a10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814e17372078e802bd21665b7f8e926e31241ac86367a0a7f514584eb038ac66`

```dockerfile
```

-	Layers:
	-	`sha256:49a49220c66acc3647abd4965f5ea5bd655a1bf98a1fdb56d7416879b704a5f7`  
		Last Modified: Sat, 17 Aug 2024 03:19:18 GMT  
		Size: 2.1 MB (2148825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd65243310d5dedb7515236fc9f9ac212a50bea3df7d32b84cceaf312c742782`  
		Last Modified: Sat, 17 Aug 2024 03:19:18 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json
