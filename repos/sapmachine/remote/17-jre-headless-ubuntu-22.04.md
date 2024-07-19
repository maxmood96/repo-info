## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:7427b1671d006d7650bc9ab47435f600428ef39388a192554dca16f2ba52976c
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
$ docker pull sapmachine@sha256:9d4f07c99872dbf496c40423a4dec23834d33e728784b59707dd139a54be81a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82019305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a31a033908c40028d422862972732cdd0611409e0395869a543afdcc4096952`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbc101c45c86f185f82a0d36fd9f35ab934822b252a2668d707f506ff939e80`  
		Last Modified: Fri, 19 Jul 2024 18:00:11 GMT  
		Size: 52.5 MB (52485250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c60394af52410773cb0ee189552c55a255e11a74594dcb80a0c9adabd0c6d8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734edbfb79c8d6b1db848f03280d68fa815eef0e315296c2ea83b8734af68865`

```dockerfile
```

-	Layers:
	-	`sha256:5ca240ca62e0b027ca63ffb11c00a3e6617785f6ad2102c8a65a01b6d8cfd39e`  
		Last Modified: Fri, 19 Jul 2024 18:00:08 GMT  
		Size: 2.1 MB (2144916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d8107ae941fce3fe7ad13b2d1dabc4ec48066f669792cc3e001cc2111075e9`  
		Last Modified: Fri, 19 Jul 2024 18:00:08 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3bbb0e6a92a25d1db65eee37345a7f35423c88898b6608b5d80627d4bb3737bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79132717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286da6296b3d85b969adfc0059e97f552f299e000dd5565445cd5547dfb27437`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2899e912d4bfabef6a1bf57251345d8b1236ba999e4c1919f2f85804b9277b86`  
		Last Modified: Wed, 03 Jul 2024 00:05:09 GMT  
		Size: 51.8 MB (51772692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c56e4e5d9eafcd21b316e5dcdc9498591abf74467736075c060a47ea1c8e7671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2127426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc68c6aaa90e221b587f4dec0e5dfa71ad36736bf42e3c8036e64ef10761692a`

```dockerfile
```

-	Layers:
	-	`sha256:e0a440cbcf21c288d53b625130c64f74c4803e18a6fb44940b04eb301c300fc2`  
		Last Modified: Wed, 03 Jul 2024 00:05:08 GMT  
		Size: 2.1 MB (2118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8db59b7017a7c4be25f80deff0a58d030e9c579231a8a1cb9aa9e793eed1f6f`  
		Last Modified: Wed, 03 Jul 2024 00:05:08 GMT  
		Size: 9.0 KB (8997 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5f04224da8aa4baf899f0f45249786f50189f6525b0085b425ecfcd5f1431151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88203359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cda9a7dda053f87b23701a5d3403c2c33a6820cace67a609b559cbcb1e4a39b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2829244eaa182f3ec72b0023744caa19bf46fcf798d9b5b32be49e1f6f1e243`  
		Last Modified: Tue, 02 Jul 2024 21:35:48 GMT  
		Size: 53.7 MB (53742278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7d830ea1e1e392f685ad0fe5969b4e56f50259953c1d71fcf92d768795907a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba9b2d64f41e7f7865f13e30352885eb57426308395173cfe74718436f27c21`

```dockerfile
```

-	Layers:
	-	`sha256:a323490133aa1a72a64d3b45165202e8c64979b219daca38a76ac06023ed9add`  
		Last Modified: Tue, 02 Jul 2024 21:35:46 GMT  
		Size: 2.1 MB (2122668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d686579a332fdedc11c27c81956d700aebdbd31589166ac97cd9c834faea504`  
		Last Modified: Tue, 02 Jul 2024 21:35:46 GMT  
		Size: 8.7 KB (8734 bytes)  
		MIME: application/vnd.in-toto+json
