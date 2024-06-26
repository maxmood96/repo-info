## `sapmachine:22-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:0eda7bae79c7bc8d41c75b95551aca5d4bb837c7cc788ff39767d18af6d309d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:312bee23b6bccc81c0c058a4f84631c14532c3734b675045c19d94db180f04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242947612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b682ce758c787729ed37267a20509a654c7a32e2e840d56dcea623a264f0ff`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d69270af8671eb969bb9d7cb219fb5f720a6accc9557b5769301133d1e7452`  
		Last Modified: Tue, 25 Jun 2024 22:57:54 GMT  
		Size: 213.4 MB (213413858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c06952964e0a536264127ecfb8cf42e25e2fab448c91743f0332c39bdeba5bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d9c68b8c44a3094a914b25804ff6876da2b546f742f406f0b4fe96387206f1`

```dockerfile
```

-	Layers:
	-	`sha256:ab1ca716a4c224f135d08a94a6366842215fff23e42b9f6cc42ff280a3aebb6d`  
		Last Modified: Tue, 25 Jun 2024 22:57:51 GMT  
		Size: 2.4 MB (2445547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1058d0cf51488b71787812a112ed9f1460dc6bea64aa808adc498b40d73fd1c7`  
		Last Modified: Tue, 25 Jun 2024 22:57:51 GMT  
		Size: 11.2 KB (11176 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e7494a9502e24f0c47fb86c6a5aa10d26c9629ea37c69cfd4f569ba60f478b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238705120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892840ac69cb2470d66b47222ca83d6c0d0b2f2d382ae973335d69b1230b8d7b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ecc79d71e81a3146db081db4c0d376e11d1b21109fa0f3b2e8b6acf34ef66b`  
		Last Modified: Tue, 25 Jun 2024 23:54:23 GMT  
		Size: 211.3 MB (211343338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2923379be1f96459c51ab5d64d40eca03bff48a8fd73ba5284252c8c60ff25cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6659bec65f79fc95a402eb69d7c7de43b0e566dc1a45dea923a9dc8517188cd3`

```dockerfile
```

-	Layers:
	-	`sha256:da396193f2f80509e017710c036075379b1812ebd45a70cf3d713f9bc2e0beb5`  
		Last Modified: Tue, 25 Jun 2024 23:54:18 GMT  
		Size: 2.4 MB (2444692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ecaeae4e8d8a96f0c616ad255e68f8e099827db16cc92d8ccc75d33afa2d69`  
		Last Modified: Tue, 25 Jun 2024 23:54:18 GMT  
		Size: 11.6 KB (11574 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a082f76d9c1a75802861a5fdb2a5660e120018ab1bf787b24e51ed45952b626a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248937612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33b209b5591e1123f0c2603e977acec72b12e37b05b13b8b1307c1019553324`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321167de3e9fec8749f8e3c55be61f8668103d8bd019c0813ef1ad74cdcdb37`  
		Last Modified: Wed, 26 Jun 2024 00:13:11 GMT  
		Size: 214.5 MB (214476919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9992fce2f94594fa9815bc5565d68963a133077a744319b9e2691a9ae3f3abd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc39a7f3e7be523f83d68c13871fbe7ee57ad2b9d592da43400b29532a5cb7ad`

```dockerfile
```

-	Layers:
	-	`sha256:7fa1fe2145a17f4be358efbc89e72a8730af0548d134e670b0d9ba95503bddc7`  
		Last Modified: Wed, 26 Jun 2024 00:13:06 GMT  
		Size: 2.4 MB (2447006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfef4ca5daad0e354342433223e2ff5c1ed744d3937887c6e9144e7042fea6d`  
		Last Modified: Wed, 26 Jun 2024 00:13:05 GMT  
		Size: 11.3 KB (11263 bytes)  
		MIME: application/vnd.in-toto+json
