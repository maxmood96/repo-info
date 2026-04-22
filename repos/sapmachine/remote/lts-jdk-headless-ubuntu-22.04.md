## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:b8e8450d6620db2b17dc8c8edcceba64e5d55c3f03eb3de554f743473a97fed4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:05fa10c5ced4c17243d13731a11e733011f3c88f9b35feaee244b7799156afd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250303968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2694ff7fae77f37029e659609cc0e644ef3848d076817b0518fa51e5fed9e553`
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
# Tue, 21 Apr 2026 23:03:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d71203a52487b42e985a26d2fc05a749ed6c1f42b0254b44b16f531692dd1fc`  
		Last Modified: Tue, 21 Apr 2026 23:04:05 GMT  
		Size: 220.6 MB (220567470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a383422010fc7696931c02584ed02d92a2ed10db1c5a666aa5f294a4ed41cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ebaf399664042a8eeba3aed604928b3f04c1aa2f5682a1775d28ad75c3ebe6`

```dockerfile
```

-	Layers:
	-	`sha256:7ee589945125574f4046adc1d56652266d380b8abb2f1864822f105a88f9ef66`  
		Last Modified: Tue, 21 Apr 2026 23:04:01 GMT  
		Size: 2.4 MB (2370828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f815bd5198572de66ac4a464a58a8aed6e6de4990c971c06ed7880f21c655694`  
		Last Modified: Tue, 21 Apr 2026 23:04:00 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:47ab8b3ae3cdc5dda82faca1a235ed7f8be6a29e150eff356dec9ca318062e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245924876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60588776ff234ee661245aeedcb44fac12e7ebf2aef30c41d7c1c36795e67dd7`
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
# Tue, 21 Apr 2026 23:05:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:05:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd34e203ac75448e134645c12761d826ec0c3f48ed84c99ab047816e1ceca78`  
		Last Modified: Tue, 21 Apr 2026 23:06:15 GMT  
		Size: 218.3 MB (218318333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4920caa86f9c2c99dc5c5d39f5b106ff53491c68eab1725b326d13f0007e433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00479e7ce27d9fabdda7f1e5879cf149bd13516e3b34666cc6b1b93f19a5adee`

```dockerfile
```

-	Layers:
	-	`sha256:5b5c53dfe8f84d8515e042a14f93435448a83ddfa99eabda451660216051da5c`  
		Last Modified: Tue, 21 Apr 2026 23:06:10 GMT  
		Size: 2.4 MB (2370521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d50369a5882931b08bc879942217ed590a2ef243fb3a0d4086b5b2c37ac18ccd`  
		Last Modified: Tue, 21 Apr 2026 23:06:09 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:33fc026a6a506ea3810fc918f29edf07b06f23b598db5ec8819e0dcd0da1b408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255123993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2500c0aad3e69f39e39b50dc29fd5b51007d7432dc419dcea8d50942d33fb01e`
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
# Wed, 15 Apr 2026 23:30:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:30:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:30:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9926529a92a0ab211ba6e77315202b428d03ae540c3ab7c87d02bbaa6422ce47`  
		Last Modified: Wed, 15 Apr 2026 23:30:41 GMT  
		Size: 220.5 MB (220475595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e94e495cb694557a2560e9f6f044c0694989652052dcd3452ac7815424f188a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99374cff64ebfaa47a9397cd6af7048007e3cd7c7836d508696c3d06df6f8a2f`

```dockerfile
```

-	Layers:
	-	`sha256:1cc48e787469e9bdece062f2e3fbf8a31054677452a5f53c855e46e06d1a296a`  
		Last Modified: Wed, 15 Apr 2026 23:30:35 GMT  
		Size: 2.4 MB (2367084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7bbf465f81bc2f9c4ed40f9468b51fcfd8a93fece9895753b9fb82c50f927a`  
		Last Modified: Wed, 15 Apr 2026 23:30:35 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.in-toto+json
