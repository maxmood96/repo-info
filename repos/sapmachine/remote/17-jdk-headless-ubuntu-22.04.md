## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:b1ecf6119230bb94bcbb88c9b981392dc330212457e72c130737dd5a11376dff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:74ccf5edf3c45a3b6efad9b3989e335941698992cff2064c9ce55593e22a21c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229819494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba9cda6e35c47858ce1ae7cea01a2cad1d7a9f6c0d7279fe5162f539e7a8ebf`
-	Default Command: `["jshell"]`

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
# Wed, 15 Apr 2026 21:00:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:00:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:00:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f632872ec242fc2b4c2a2c28606876300bf1a297ca57defd3641bd51ebfca2`  
		Last Modified: Wed, 15 Apr 2026 21:00:27 GMT  
		Size: 200.1 MB (200082996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95544375d09a1ed23dbf8de5610a3af4c485c7861b96ff1582c1ea526f3469ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46312ebe76cda32f93effd208abef63e187903c1a1caa3097d5e8e33e7e3c567`

```dockerfile
```

-	Layers:
	-	`sha256:711557c94d154c77f26e358db6bf8a5251eaf21cf313c1eee75492cb17c167f1`  
		Last Modified: Wed, 15 Apr 2026 21:00:22 GMT  
		Size: 2.4 MB (2378155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f8d016022e589796ef933012911a981dd9f3b06eeafc42aa5034bd42261e84`  
		Last Modified: Wed, 15 Apr 2026 21:00:22 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a4ab830cd0c7aea57b6e3f84eb04c37e1a7b00e58bf6400c280487da3d526170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226374177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56968b22d4366eb82d88b9d51d0c806fc09e7021713dddea199bdb024b539591`
-	Default Command: `["jshell"]`

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
# Wed, 15 Apr 2026 21:11:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:11:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:11:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b323e10479b3460cd290bb15560c188cd4f4f959e7adebc6ba0dc02c79e8e9`  
		Last Modified: Wed, 15 Apr 2026 21:11:33 GMT  
		Size: 198.8 MB (198767634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c3860a5adb0179fda33ad3001d221fd26d61dfc1802a70f98241041b015cb6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c044bcb215211a93b96c3bc7e1da2fa48fcf6e2b09f858619fb2806f0a690c`

```dockerfile
```

-	Layers:
	-	`sha256:0e0d9c38fbd9707c42506d2376e30b5b31344d33a46f1491019b331638dcc3a1`  
		Last Modified: Wed, 15 Apr 2026 21:11:30 GMT  
		Size: 2.4 MB (2377827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed69938cee5db827065af26a5441e6404e0b9547ec0e6d6992131bb19d951913`  
		Last Modified: Wed, 15 Apr 2026 21:11:29 GMT  
		Size: 9.0 KB (8993 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b40e355c7a2ff91fb1f5789ea8339da2c3e2e4af25e204b4d340cd6b33cdb5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235325161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa55a521fe38e1736944765838db1343819ea6b4cd9ba4321515b3b68f7a5790`
-	Default Command: `["jshell"]`

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
# Wed, 15 Apr 2026 23:43:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:43:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 23:43:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de31122340de8bcd78255891e2316c669c0be0ce66d079106b4f137005025e2c`  
		Last Modified: Wed, 15 Apr 2026 23:43:52 GMT  
		Size: 200.7 MB (200676763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d83c4f8ac08178c574dbd097c39383a07ff561ad08d6d2cd58a56b603898769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a393d56a322ca361265c6644237906fdf1f42bfc5e517511df72dc0dd6031d78`

```dockerfile
```

-	Layers:
	-	`sha256:28bce451c0326c3a7364f4ee3659b420fbe0443dfa697a43b75d65f009ca3b11`  
		Last Modified: Wed, 15 Apr 2026 23:43:47 GMT  
		Size: 2.4 MB (2375651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:205cb63d37653677a2c16598743862f3b97256373d9dc74648020645d59fbf97`  
		Last Modified: Wed, 15 Apr 2026 23:43:47 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
