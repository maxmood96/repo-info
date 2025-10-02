## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:7159964d9661d1b2d437454900a93656e25bdbb1e5889d796dbad188296bd21d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d704dc5e7a3c58c2e6a6174bee6f0ca73534104465be449a7d174997e675169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229020446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227c82f0b848fbb5d0a5c84f166de1b5ce45fa913ecbd7746a4c296ef32869a5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9f339b919fe2e16fd937d8a56193781169acdb225da048b759d7781fc216c1`  
		Last Modified: Tue, 16 Sep 2025 00:35:36 GMT  
		Size: 199.3 MB (199296996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:30f71c53290155ae1fe28e111d6181732322cfde1eaea3856e7350b590af1211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5d8fa2395bc92a8dfd3a00b1221bbd3181da21593c7961b5397b0f7fb633c5`

```dockerfile
```

-	Layers:
	-	`sha256:064f7d438c7f752a7687e0c36e4057ba50846cf0f4245e32b64750a6b44a3469`  
		Last Modified: Tue, 16 Sep 2025 00:05:54 GMT  
		Size: 2.4 MB (2354472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d171e51c868fe11b761bf654177e5f5183e5498bbecbedb9277648d38f73e9`  
		Last Modified: Tue, 16 Sep 2025 00:05:55 GMT  
		Size: 10.3 KB (10277 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fbfd33ab760e2412ed5d9a9e8f56334ae03ed164c14db82c8b31851a0372ee08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229088106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe866d6a94db00f8fbd831763bb3a2dd317158b209341f5e71e0495657afc379`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d42e00c08bdb040da44a5913290b4d3b007aa274104c1300d22f8f7e1a1f39`  
		Last Modified: Thu, 02 Oct 2025 01:34:57 GMT  
		Size: 200.2 MB (200226531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0cbc2e9864f272b9a183384c8e936fe03c6b81123e23bbdbf7d485f2dbbee8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a129ae60cdb8f0ebc119941d71defcaad0d10809d889f66fdcaeef63a3e3335d`

```dockerfile
```

-	Layers:
	-	`sha256:1c826eaebf90339890fa99cf49a69fef448ae150c17838a335481de5a74c0acf`  
		Last Modified: Thu, 02 Oct 2025 03:04:46 GMT  
		Size: 2.4 MB (2354979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ef5013c4adbee9eb9ce2ea714bf81b116265eda44c708500fabed28078ff56`  
		Last Modified: Thu, 02 Oct 2025 03:04:46 GMT  
		Size: 10.4 KB (10429 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:dd754b140433f85a0367e5d6f001060219461969e19c8d0bd1c67107b9a61099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234177683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec678a3eda2796a998ac96a686269cd02c09610b3f70260f20fc7c1e319032f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d913ea51cb7ac64349b2caa30f8822e634dd7d1e1e75e6da73675ae4118a97b`  
		Last Modified: Tue, 23 Sep 2025 19:16:06 GMT  
		Size: 199.9 MB (199874556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f7ec51611cb8d29586d71aaca7fc9c5b71df12c4b3995b727dcc0f9f3e609de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefb925537252aea4305465a3c45bb110647c32eec806233058a986418a12683`

```dockerfile
```

-	Layers:
	-	`sha256:63e04832e60629d8043cdb5846c2f25b3a585b090460d2d8f18f78b050d985b9`  
		Last Modified: Tue, 16 Sep 2025 03:04:53 GMT  
		Size: 2.4 MB (2350526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33bfda92aec259c2ae83f188304555d8676efac56ac9e41fc73a815086a94beb`  
		Last Modified: Tue, 16 Sep 2025 03:04:54 GMT  
		Size: 10.3 KB (10343 bytes)  
		MIME: application/vnd.in-toto+json
