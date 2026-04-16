## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:975ae7fc8bb2643c2ee3cd77e0004cdcdef42342965e2a16d13b766adbf6e9d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

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

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

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

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1e5cc6b45e8a3395f3ddb1ce544337b17f6d8b43791ae9fd7e59098139858cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94323543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b112c6961ebc51f7d9668c54f31704d1d935a919a7dc7b9ba2fdc003a77eed7`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:42:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:42:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:42:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad55fa8f2c279f3180d00c92cc7e06ea2b4104c9a4c9bfd79dd3c1087f295643`  
		Last Modified: Wed, 01 Apr 2026 20:43:02 GMT  
		Size: 59.7 MB (59673883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8da743783cd7b8353d7529ea75599102ddb21e20da1cbdac3c11e07fb9ff9bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4311e49d08300163c061a94b00b326c7c243a198bb1b038d0c6a3d7eeaaea6b7`

```dockerfile
```

-	Layers:
	-	`sha256:5159b2715b96db35b2f36c4a0ef6d5c3ef81b95077aca1bfc9f34eea2b3818f2`  
		Last Modified: Wed, 01 Apr 2026 20:43:00 GMT  
		Size: 2.6 MB (2550007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a811aaabe5b1c26dce41de9c5ef1e095a4bda4e444e9378b741911b6e06e3e0`  
		Last Modified: Wed, 01 Apr 2026 20:43:00 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.in-toto+json
