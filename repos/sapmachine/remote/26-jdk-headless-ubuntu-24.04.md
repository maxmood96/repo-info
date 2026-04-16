## `sapmachine:26-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:1f192d7505159dba1162e88e8ee48d48af51a64241635bee84f2762604c49ee7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:40b7fcf413eae62b486a84184b998cd6669db705f30575bb987c9e62691c2ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254912062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d6dde541ce51839bf331606361c47767dec27ab9cc9d06f81ccb96f119c7a4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:56:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:56:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:56:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7872d22198d1f0d2f9b8efc4653c5a815e4079ff009d177707568b0847ea7`  
		Last Modified: Wed, 15 Apr 2026 20:57:06 GMT  
		Size: 225.2 MB (225179084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d7658d2eda220e4f7cf75d01d02666eee68ca28630978e7141c2be3dd3bbd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416c794e3eb85e333231797dd546949bb02e4df26dbba150a70aafe6035fdbfa`

```dockerfile
```

-	Layers:
	-	`sha256:374bb35044cc87231974cb1f03bd2b7e73b2124dc6227b891ba1f219c8544844`  
		Last Modified: Wed, 15 Apr 2026 20:57:01 GMT  
		Size: 2.3 MB (2346248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b9183014aeaee94ab0050627a6492acf5d9ee9dbb4e577d05c066e6ff5cc8f`  
		Last Modified: Wed, 15 Apr 2026 20:57:01 GMT  
		Size: 10.2 KB (10157 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b6bfe585b0a60ff4f5f8d2d18b13daa5408d3d9b6922b1d14dd735ba921532e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251914477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5cad640143108b9ec61ea84a5ceb17a4b55ce19e92d97de1424c61d0f5cd5a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:06:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:06:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:06:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f13cdb53303624c96fbc942e5323e93ed1c852644e79504ea6e8149f2491`  
		Last Modified: Wed, 15 Apr 2026 21:06:50 GMT  
		Size: 223.0 MB (223038692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:61d18deef566bc0cfcc179289e58e2fff3de1e01e9d450990f00a90ef482bfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2357061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc27644f125b4e0a3464a82e9a4ebfd9cf8ecfccd6c7d23f16d9c4084a70acb9`

```dockerfile
```

-	Layers:
	-	`sha256:865b6e00ad59d85b42edb5ccf601bf5f50bce6fb8696554181b71e81617d8e02`  
		Last Modified: Wed, 15 Apr 2026 21:06:40 GMT  
		Size: 2.3 MB (2346752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88e1e6b11f48a4161b2cd95dbcbadfe9e910aa986dd899f125e96c95891cb3e`  
		Last Modified: Wed, 15 Apr 2026 21:06:40 GMT  
		Size: 10.3 KB (10309 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6aef7471ffb8fe8afd928a11bc43867070e595af8fa9a69b59e7bdf4926698ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260547893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a199ca9438d1ab789367a7e25cd03b9532b8abe6c21f995beec3415e1aab41`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:20:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:20:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:20:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24add61aef6069e4da424453f230a31da983b0e3453bbfc0dc6edd47055d4b6`  
		Last Modified: Wed, 15 Apr 2026 23:21:21 GMT  
		Size: 226.2 MB (226233715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0328bb1a4ff01f64182092abbf18c799ec78493dbb69e24a3d5146bdc2cdffe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d49f93fbf1719a18a17c3363323e1de14f93b697e75455931eccfbc4b592f2`

```dockerfile
```

-	Layers:
	-	`sha256:9abc3abf32a2dc2de4b25bcb77ef6e6fa1c47c37ad62db1571878c900fb79b75`  
		Last Modified: Wed, 15 Apr 2026 23:21:16 GMT  
		Size: 2.3 MB (2343101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5ee7d975cddc029e58a113c687916c8d9d9f9c1251eb0e3fe8dddf85f3cb5f`  
		Last Modified: Wed, 15 Apr 2026 23:21:16 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json
