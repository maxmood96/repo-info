## `sapmachine:26-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:e5b1b06c799a7674e9f1cc397dfdc4d844a29902af38ff81929ad8f5a6a5aa44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:d6e58c7045d326b596e157f0a54c8416502942da020283d28e99636b026fa909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88342873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b03a955f20413825bf64752b0eb04da0fa9eba0a4187694de1ae0b7d5ee9734`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:16:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:16:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:16:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001b5807a82ade4437b958ac76253a9624e072d4c5cda89ef6a8c2c3b6ad35d8`  
		Last Modified: Wed, 15 Apr 2026 20:17:00 GMT  
		Size: 58.6 MB (58606375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0bb439d0ad93755479d245b6e865e2129ea34f7f04916909a390821b077eebe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d720b06a89c2745d932143b082336f40b6feda20a75b17eec8207abd4e458f5a`

```dockerfile
```

-	Layers:
	-	`sha256:a2091039fab81b546acb5e72fac00189f8ec381e4105826fcec4b8511e368022`  
		Last Modified: Wed, 15 Apr 2026 20:16:58 GMT  
		Size: 2.6 MB (2551105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aac804a8290aeeea2220f9409baaf20c475967c06786c31e1d7cc52b7913b81`  
		Last Modified: Wed, 15 Apr 2026 20:16:58 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f3fae1f7b6f201af67187bd4b668d0f0eeae5adc2a3c34be5f18cf1edf1fca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85175280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f82b593802c2133222fedb95c2b441d259e4435c259d9c2d496dc13ab7893`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:07:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:07:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578e51e157758e088515994bae48ecee0220660c9719af46636ce4e496060540`  
		Last Modified: Wed, 15 Apr 2026 21:07:27 GMT  
		Size: 57.6 MB (57568737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:503b75abe2722e3c298fc14cfdb3d77fdebcd3aeb64cdf826c503151946c9df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397e65b9a0f12d8b2acf4ef3a95ca8f9f29281b2e9d4c3bee3fe38df13da8f0`

```dockerfile
```

-	Layers:
	-	`sha256:3bee550428a5caf6e3bb60dae5aee2749c323689068efc0887be974b87e79238`  
		Last Modified: Wed, 15 Apr 2026 21:07:26 GMT  
		Size: 2.6 MB (2550784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8cfbae004989bb3e1f2bac64121b4dfed46bc0a61174ebea8620ff1d47a8af4`  
		Last Modified: Wed, 15 Apr 2026 21:07:26 GMT  
		Size: 8.8 KB (8833 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a0bedc2bb9dba05c5d152569d439317da2e7e119fc2979a1ae2fefe0441edf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94322138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7696bb9ab17a157b696394791cbf60fb5b3046d56d3b91c742eabb5a7f4d7fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:24:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:24:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:24:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1a19a4558c99c5a9390c256dd2d817a737635cbde763db2f9c12f0480a22fe`  
		Last Modified: Wed, 15 Apr 2026 23:25:05 GMT  
		Size: 59.7 MB (59673740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b7c214f266f097b3cb90139d973841a77db7af75bc9b03f28626e6ef80538afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41646c42f9103b85a3a0fde1bf4cffd8df15eaa0ca7e6a9c3265fa71c5846cd7`

```dockerfile
```

-	Layers:
	-	`sha256:9a4efc2c94ce5049de49045ca17a24a3b0ed7ca822bfeb09896760a5fae04746`  
		Last Modified: Wed, 15 Apr 2026 23:25:03 GMT  
		Size: 2.6 MB (2550007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:326c727b8200caf72131e5d0a73be73ae52a6f1b70b5a391ffc3746c20f0dca0`  
		Last Modified: Wed, 15 Apr 2026 23:25:03 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.in-toto+json
