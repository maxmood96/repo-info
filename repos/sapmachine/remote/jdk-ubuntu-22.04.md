## `sapmachine:jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:40c66e59fbf4ece9abfb26045df3afeb62abc7288a0e5f9b75332e6f8f5c75c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5d34c762c3c92419bc700d738b0ddf292ba7c496d95b9a1c17cf0e0fe5749ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262769947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5e6f374f832e511009fc6970fa1a0d5945f30ce556639a4bcab9ab846dabaf`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4479888f69aead05026d4570a16b131c441f84e5637d2e0939014cdf5bd6d386`  
		Last Modified: Wed, 17 Sep 2025 22:00:57 GMT  
		Size: 233.2 MB (233233012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:842040ebbba66017e2bf1f08dd599af7e6b3add5136089c0387d3a2dfbbbb9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087aa4a40aff6d2e5bded484867929316b88c14cb63a321c276c3cf6c8736083`

```dockerfile
```

-	Layers:
	-	`sha256:3de3c69606a06c70b1851dbf41d759584848db770179bcf128d1c9736937627a`  
		Last Modified: Wed, 17 Sep 2025 21:11:10 GMT  
		Size: 2.6 MB (2622346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef06f76a9f4ac1c621b114744bca2ab26d37f84ce8bcb243f9582a2239105f44`  
		Last Modified: Wed, 17 Sep 2025 21:11:11 GMT  
		Size: 11.4 KB (11381 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:34a44fed2841265bdef6b078a8d9f1a6118b65b37a2fce5d0eb9b4cc21089619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258381108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a214dda13a5c83135e99ac97476bd159cbee5f542a656db2911fb96302b6726`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cc9e178b6f62e1e1eacc959d3a3cd959b07342d0fc01347faeafadaec3dcad`  
		Last Modified: Thu, 02 Oct 2025 01:33:49 GMT  
		Size: 231.0 MB (230998001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:544295818621958b885f422ebd5c9c1552b30b4845f8d246088beffa26e56f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8795068652f8d6ab37cdd2addb0b9a57b923a4a56c1ca0ab0270adcb5702725a`

```dockerfile
```

-	Layers:
	-	`sha256:69cfe9cb94d996eab088e09da705fad4224ebf557bebf65901a5509f52963ab0`  
		Last Modified: Thu, 02 Oct 2025 03:10:35 GMT  
		Size: 2.6 MB (2622121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f8e8fa4bf3b818c3ee8a842eacea8489892a0647b1068de2856cacb9ba9194`  
		Last Modified: Thu, 02 Oct 2025 03:10:36 GMT  
		Size: 11.6 KB (11581 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4163fd2217f2fb294ff0c61dd2eaed6b8160f7188b5878e9fd22331acb10f5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268441746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bddfdd6514f7d8a7d9dbc7d800b5c120276b56502ceca7394a5dd43c00e807`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:08c93ae43b2c73908de73ea162c78a8a7d6ab06d1f71ae37e5ecdaad14a79a81`  
		Last Modified: Thu, 18 Sep 2025 19:47:31 GMT  
		Size: 234.0 MB (233998522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:362b41a0062aa9ed0f7e943b1b40a01dcd95f624373a4572bff220fd4612af6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edd11c51b3947591fb5ca5a356ee0fdca5ae6686cc69d89fdeb2352f7c5d1c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98e61b02a6a569506119d4cba4c649f0c4b5aa2aa34ba5fae9f471c22540352`  
		Last Modified: Wed, 17 Sep 2025 21:11:20 GMT  
		Size: 2.6 MB (2617945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b4d9d6a56880a011d002565a833864cd96fcde99501a3a75521fc249e04d3e`  
		Last Modified: Wed, 17 Sep 2025 21:11:21 GMT  
		Size: 11.5 KB (11472 bytes)  
		MIME: application/vnd.in-toto+json
