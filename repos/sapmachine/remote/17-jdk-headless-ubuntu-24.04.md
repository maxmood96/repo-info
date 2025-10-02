## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:6c8b1e017cd3e84b10ae88978d2d01080333f44b8359e8cf9819a11ef7b0dbf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

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

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f5745c71520dfb2d7b684776cdd305306a6533978d675bbcd550e1bb22e1365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236801478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105c3385f32f26e01868ff8a184618fef23c6b810b11b73cdae9125f4f1b2520`
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
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
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
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d191911032a9c9bce40f2576176a4e1b564d92e9c5a3729dbd33e262c1c7e59`  
		Last Modified: Thu, 02 Oct 2025 04:56:16 GMT  
		Size: 202.5 MB (202497931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8cb5ee35d865603d9c90ae590ae9168e4292868829c12d5ebe5f2c481523e207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59864754dd844f6536ee5b6edb5b5686bc8438cb2e3515790b39c6f42754d6e`

```dockerfile
```

-	Layers:
	-	`sha256:646aa3803596be9fc342ae6e6f093956932252be6e55c26a02877fc2b2d076ff`  
		Last Modified: Thu, 02 Oct 2025 06:04:50 GMT  
		Size: 2.4 MB (2350526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52ff4d677f99e423a324b8fb1a65b1d4968b7249f1128186991517f6f96f065`  
		Last Modified: Thu, 02 Oct 2025 06:04:50 GMT  
		Size: 10.3 KB (10345 bytes)  
		MIME: application/vnd.in-toto+json
