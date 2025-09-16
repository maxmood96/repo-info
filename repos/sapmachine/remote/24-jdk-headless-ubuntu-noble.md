## `sapmachine:24-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:2227510aa8ff3a84d2d4cc4f35902236b98bbad37610b063d87fce016f072262
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:a5887ec339ec90c68593b014fe0013460f07cec2fb96f01c0f5038479563831d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260998445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c74f7254546d734973e0fef17ed8a164f456f90928300fad90921b824750edb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201dfc257e5f34f16d4466a2b2bfdcffae9bb825d4b97ca82b0626aacd33b8f`  
		Last Modified: Tue, 16 Sep 2025 21:06:25 GMT  
		Size: 231.3 MB (231274995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3ee695a6da63fb7546e112dbc6c8137b01328e6f36be0c2399e7a70b223e19ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98062f41d1cd45cf4c6190ef0fd845b8b368c2b7bed4ac5801f1e608472649d`

```dockerfile
```

-	Layers:
	-	`sha256:023606c29333ccd9da333b9c415237e9b244f6bd0f909108ea5ebb7946829e82`  
		Last Modified: Tue, 16 Sep 2025 00:10:08 GMT  
		Size: 2.3 MB (2348395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcdf07566ebabf87348fe49a9fa9d50d47894cb729f517a1e569f425effaca9`  
		Last Modified: Tue, 16 Sep 2025 00:10:09 GMT  
		Size: 11.6 KB (11602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:47235a985c25cbee38ab7ca6f82ef43c212abe1d94f46619b014abb6ca84217b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258064613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bb58b5d7b82093b04569e6b9c8af9c55ce735a4411475b0749f02f4c402f0f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb99d96022f69a85705591b56d9f79ffd89b2ce23b3d08dcbfdb744022606bd`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 229.2 MB (229203296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:63846d7a0f3b210761da55f342a8931e8351689d702d37db53f0267c5e34811f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6341da11a7cdd637906b0713c6530efcb23ccd4c553df27913f219bf1906d8`

```dockerfile
```

-	Layers:
	-	`sha256:83bec98891b9916f79b1e293f7c34840e3e60b4e704ef83ff0ebea1b52acfe07`  
		Last Modified: Tue, 16 Sep 2025 00:10:13 GMT  
		Size: 2.3 MB (2348947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcb98fb86cc8b94250bacba7d109ba00f2c4c89d5f5b028e0d4b320de6e31096`  
		Last Modified: Tue, 16 Sep 2025 00:10:14 GMT  
		Size: 11.8 KB (11801 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e72197134c33b70583b514e48c067bf4226d306fabe01fc0f1ceb7c7d325b883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266250355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c662174b18641a7e99859199e6e0ef575c8b0c537da56affb58155fc25eb2124`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210f35b9f50914bc68174efb60afe2e55f79f3c13ca24315489aea1930aa4ab`  
		Last Modified: Mon, 15 Sep 2025 23:36:54 GMT  
		Size: 231.9 MB (231947228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c011811a555a671e3f86e4c8b6019ace88435aa29ef93b111377fe9860846cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2355549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36bf0f17c3270a5deec73c33a20b613078d94caba1bd15fe9aae86806e34e91`

```dockerfile
```

-	Layers:
	-	`sha256:4796e0eef46c1a5bd0265100c8ac6a966e7f11d60dfd5b5485adbdfc6a4e85b5`  
		Last Modified: Tue, 16 Sep 2025 03:08:35 GMT  
		Size: 2.3 MB (2343855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b99857cf4f0095a3e14479adbaae1def1dde88d10311dc1b2c1038d1508362`  
		Last Modified: Tue, 16 Sep 2025 03:08:36 GMT  
		Size: 11.7 KB (11694 bytes)  
		MIME: application/vnd.in-toto+json
