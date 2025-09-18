## `sapmachine:25-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:411b88ec298e9fd156aebad0e188ddf3e4f9b2d1a1a9b8d2c8a5123bd6e4e3d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-ubuntu-jammy` - linux; amd64

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

### `sapmachine:25-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:25-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fb2299529980723e6370ebcb9cdb747e0b2f13d5e289682b7a5ec3d08ebb30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258359557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a8288c4a54363b8b87cf128d185c2c85f12bade76074b9667abec558ff9c9a`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:16d1f431a88a74ac3e9dc00b01b43ce8675ac0979e6dd764daaba0684de30fb2`  
		Last Modified: Wed, 17 Sep 2025 22:07:48 GMT  
		Size: 231.0 MB (230998088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c6d76b0ab5fa141eb1cfd2f8fb24ee8bd0809717bbd90103b5d860eaf774850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9063d450bc8820ed90db2dfc1dd6bb97172792fb0b81643974ef6aa47c78492`

```dockerfile
```

-	Layers:
	-	`sha256:fafddbdf2676f2ad7d5beb742278f6080bdc6f1c5f6d8b32e71d861fd601c76d`  
		Last Modified: Wed, 17 Sep 2025 21:11:15 GMT  
		Size: 2.6 MB (2622121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ccde6db479af7629ab9f1e89c5b9ef9cefe1c7809eb9cf6663b73003f2a6f9a`  
		Last Modified: Wed, 17 Sep 2025 21:11:16 GMT  
		Size: 11.6 KB (11581 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu-jammy` - linux; ppc64le

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
		Last Modified: Wed, 17 Sep 2025 17:44:35 GMT  
		Size: 234.0 MB (233998522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-jammy` - unknown; unknown

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
