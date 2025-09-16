## `sapmachine:jdk-headless`

```console
$ docker pull sapmachine@sha256:b17daf3d74e9edf946aacc279b33e6dfbeabded9685dbb0456fd34911ecef77f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless` - linux; amd64

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
		Last Modified: Mon, 15 Sep 2025 22:27:09 GMT  
		Size: 231.3 MB (231274995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless` - unknown; unknown

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

### `sapmachine:jdk-headless` - linux; arm64 variant v8

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

### `sapmachine:jdk-headless` - unknown; unknown

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

### `sapmachine:jdk-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:45fe5f5006d175bf19cd6dd44b8a1e378aa137628fafd90a2f70f69bfad0a3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266276624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf700541b749c5a2631b9f092791764d85d8202ebd86f5613b86e09961e28847`
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
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
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
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0164bf69d9a88f9dabb7f8ba9561423887318a60e2be40f509f8a5581ace463e`  
		Last Modified: Tue, 02 Sep 2025 01:50:24 GMT  
		Size: 231.9 MB (231947091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:770d3b33d5f573d35dc1e1298d78271b0a67fb4c337ed1bfe5d546430e363241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2355544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df37d830317138333892bb46a64d4c34a7b7e4e9fb0d9fef559ffaf09bdb965`

```dockerfile
```

-	Layers:
	-	`sha256:31f1af73c47764c1f098b25fa2abac73ac8052cc2030c095e869600b15f7b4c4`  
		Last Modified: Tue, 02 Sep 2025 03:09:17 GMT  
		Size: 2.3 MB (2343851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db047c955b37759ed0a649729f34a2d7be6e7f7e3c1063a636a257165563f854`  
		Last Modified: Tue, 02 Sep 2025 03:09:18 GMT  
		Size: 11.7 KB (11693 bytes)  
		MIME: application/vnd.in-toto+json
