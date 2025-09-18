## `sapmachine:lts-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d33ecb2a1678bfa5d8fc981fa971b8741d5410c760b9c99a9526011eafa6ecc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:a63fa9623f5a5c5efbdc36f84071f508f92198820597325ef567296d01e9caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261558840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c18219ca1f2c61c4d23c574b85af740b546766f8daf99c93dd07be6138a224`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d831fb60ac6f44984b62cf0bfa75f203a69ab68c41a21d1782da6556bb69c`  
		Last Modified: Wed, 17 Sep 2025 22:10:09 GMT  
		Size: 232.0 MB (232021905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8197ee6dfb3e1c72139ae84e5a72914645ee22cb6d29250bdfd97fbb34fe5203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2884f4eeaa7d9a247989b97600a445977a851ea461abf43d9c6e1fe9a408c9f`

```dockerfile
```

-	Layers:
	-	`sha256:bfdf2a24430694aa55c61db5ff5bc526a4d09f569a724cd8348ce2ebbb04581f`  
		Last Modified: Wed, 17 Sep 2025 21:10:51 GMT  
		Size: 2.4 MB (2369684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f033d882eb0179ccfc3be91d960cfe346ca861528b27af6147953e568096f874`  
		Last Modified: Wed, 17 Sep 2025 21:10:52 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:857b676ad9ac1a2faaf018cd5b7397ab827184d353287dd28a56ccd5e4ab13d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257141249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50064ffe200dd0be515c4920a7e7e3cfd5fe34f318f84893396b57a903d34073`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05606f9950c552e41e643a00a1c6fb8702f5ded4f866393ffaca01980430f16`  
		Last Modified: Wed, 17 Sep 2025 22:48:00 GMT  
		Size: 229.8 MB (229779780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ae31ef39b089f7cb67bd8ab174893786b9fbb973b5edcd3024c42097dc43e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11f1d1765929e63d7bdc9792373d96c7ef067d606429ef7ac6c2db60f8d5bc`

```dockerfile
```

-	Layers:
	-	`sha256:9c6895d0cd59af4a8f18202bc7b212dd2e9b4c9cf50bd460a34611097735c835`  
		Last Modified: Wed, 17 Sep 2025 21:10:56 GMT  
		Size: 2.4 MB (2369377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccf8ecc6cc714f127e9fa241846379170b17047cf64ccc7b4d336ecc62725d6`  
		Last Modified: Wed, 17 Sep 2025 21:10:57 GMT  
		Size: 9.7 KB (9720 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3c08b2a0eb644d0b07722b755aa3c7028caffd2085efce38d404d3a096caf391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.0 MB (267045368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d2b1e5a98ab3227085d6d0a83aafff7303b5d411abe3687fc241a98f5ac26d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9787f86bdbf283339a05d8ab142d7ca0e83d00fa886a8d82237e933b1d530742`  
		Last Modified: Wed, 17 Sep 2025 17:46:46 GMT  
		Size: 232.6 MB (232602144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0fed806325e47d538b98917fa172d1f1cafdf9cee5b871da755ff2c65352106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0148e3519076279c63bcdfe218941dc8f8bfc4f1186c01e8582b75463503f751`

```dockerfile
```

-	Layers:
	-	`sha256:cb0c3f2e55d669751c3ab62b11c1e1477b6b321ccc5139464f4d6e8d4297c79d`  
		Last Modified: Wed, 17 Sep 2025 21:11:01 GMT  
		Size: 2.4 MB (2365157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac1297139c9bb7bacf5ba98e7c59f5d95f8dfc1b27c978d661e04b26d631dec`  
		Last Modified: Wed, 17 Sep 2025 21:11:01 GMT  
		Size: 9.6 KB (9647 bytes)  
		MIME: application/vnd.in-toto+json
