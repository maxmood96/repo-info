## `sapmachine:jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3cf6ee53dbc9a6ad6c1404e372f464284ade14264fffe55fb0881df87b99e7f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:606833ecd8430035a6af815749ebdf3ec89ea67e385cbae51442764dfa258f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254505343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc2201df9ed1caa9b793e4ecc09a52511f4379d7df143c22b687091b9e4dbb1`
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
# Tue, 21 Apr 2026 23:02:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1c86e43d942aba8323ff4bce21c0e1ac9c999f3ce342a046280b018278c1fe`  
		Last Modified: Tue, 21 Apr 2026 23:03:13 GMT  
		Size: 224.8 MB (224768845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:12627a47667e6b1b13ed46318a500a540f4748ac9b3ea3fb435f5a2964d38cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58440f9fe3ed9dc36da50fccba3bfebbfad84619ecef6bd78f3de4faa4df7b02`

```dockerfile
```

-	Layers:
	-	`sha256:3b0db01e3a6c99dad74e554d3bd1563861cd3bac999341c4fbb205cb96c21d2b`  
		Last Modified: Tue, 21 Apr 2026 23:03:03 GMT  
		Size: 2.4 MB (2368279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:879788b0411672f85e5d1ee9f03d7c9873d5dcdbb3c81ec90cdf20edc588f625`  
		Last Modified: Tue, 21 Apr 2026 23:03:03 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:10fd74667cc6fec979c94fe39c1322349136bf687fa2818043c2e486fd2ce47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250198329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ae2d67de55d6c7f0ffd8534f622d3e24e5b8fa2ec2237690be0b26ca2fa8da`
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
# Tue, 21 Apr 2026 23:04:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a269a8d0c6e16c378ee8c578b12374e327ec2624f2f36c0e89ea9c567be89084`  
		Last Modified: Tue, 21 Apr 2026 23:05:21 GMT  
		Size: 222.6 MB (222591786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:26983631fa7492d5156c3732bf473a163c14f8ded10c11391e07f8bfb68e7133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5722a9d289db7eb5932c835eddfb3a5c21a45efc4070250a84273274e735b7e8`

```dockerfile
```

-	Layers:
	-	`sha256:322f94466b73eed01470da407d71f137d250c31640e6a4ac52e28840126e5e0b`  
		Last Modified: Tue, 21 Apr 2026 23:05:16 GMT  
		Size: 2.4 MB (2367972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36cc7ba7a4801b1f93e4beea2f34144794807632e9e2b48bc8243d0326bca707`  
		Last Modified: Tue, 21 Apr 2026 23:05:15 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f7e4b7de8fce31f885afac5c378d95220709d6a7640472c4d055955260b07f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260390228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4873c562b1ee75db46ad353569b9ae5f6b7ee5a0ce469828785c1d46d5bed2`
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
# Wed, 15 Apr 2026 23:23:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:23:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:23:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c73b39a70f07258dad134be6b3852fd48a9df043c67dfa0e49b3a9dd6ea05c`  
		Last Modified: Wed, 15 Apr 2026 23:24:28 GMT  
		Size: 225.7 MB (225741830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f64f304345baddac1f89b385be03d1b6dc1bdb34d9a985f76dcf08362bb3e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d3c3e6270a7d1055b8d6b003011e16db38669c849d9c2436488125257addf9`

```dockerfile
```

-	Layers:
	-	`sha256:39dab1d256910a3e8cedfee5385fae1a8281104f50e0b0a40eb8a1a0e1567d23`  
		Last Modified: Wed, 15 Apr 2026 23:24:22 GMT  
		Size: 2.4 MB (2364425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb70cdfbab805ff0066e4f41471d1f4e97cbafc5c4ff2e89bf18e37c119fce1`  
		Last Modified: Wed, 15 Apr 2026 23:24:22 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json
