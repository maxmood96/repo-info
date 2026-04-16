## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3f67dbd783c556590b60b44aa62abd931cfbc56909e2a46fd20e4499e9724f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a460d7ecae4f1ca79ead6a8bd56e23297a738f631eccf8982d951272cbd90011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88863418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79a5c063b62940a885ff718021d73254b9daec604c52fa89dc723c6c3082862`
-	Default Command: `["bash"]`

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
# Wed, 15 Apr 2026 20:59:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 20:59:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfbd80003d81ab58b829f5892df29c3001fecd48f252e9196f264917ef1cf24`  
		Last Modified: Wed, 15 Apr 2026 20:59:29 GMT  
		Size: 59.1 MB (59126920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b6d486565e7c1946dd0161054f39f0938ea1764f196acac595cecf8dcff37d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe7b4dc7c0e6a0e55e68613a09a55e49c3f4d33825acde0786804ed3acafcd6`

```dockerfile
```

-	Layers:
	-	`sha256:4d6d3e364036e265943354d92003a2e56bf94c9e5a2a4424dd5e2c0527db9205`  
		Last Modified: Wed, 15 Apr 2026 20:59:22 GMT  
		Size: 2.3 MB (2296537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2be063c98079cc22e88bdcc024c410e936df3d94a3851af6d937cf38be488e69`  
		Last Modified: Wed, 15 Apr 2026 20:59:22 GMT  
		Size: 8.9 KB (8909 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:35f09b16f1215b13eab442a5ae176639f9c7f3afdbf134e8a24944e23b398b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85889078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8e3976768d171406bcd0bbc4430d72fb224f229f4b9f66977041d00c6e89b5`
-	Default Command: `["bash"]`

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
# Wed, 15 Apr 2026 21:09:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:09:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 21:09:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5d925d22319bf3c62fb0559b948e9b37f859dc4be18765da2333e8fc1820c`  
		Last Modified: Wed, 15 Apr 2026 21:10:14 GMT  
		Size: 58.3 MB (58282535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5908806f1915735b86e70db6e565bfaf273aba31be5fb36e44506962c4247c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c571f3aae8d4c5a4b5052c44b8e553b7cc0364634d2aff3b5a059f26c2a4578`

```dockerfile
```

-	Layers:
	-	`sha256:e37d370f8296ea2a0cf1fe4b41781e8c6f0988894688594e5d42d99934043b81`  
		Last Modified: Wed, 15 Apr 2026 21:10:12 GMT  
		Size: 2.3 MB (2296209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d55834489ac7b911e3f7ea59dd654cc211cd71e15c4f81ce8e6f7f091a67677c`  
		Last Modified: Wed, 15 Apr 2026 21:10:12 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ef3eb572b7fc1ec643fc60046e449d98e303c4ffd659b052da2a60ed6b79e7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94828514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec69d928262a2007964cb6a34ae614951b2fec3b870a8676234710b50d3fad3`
-	Default Command: `["bash"]`

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
# Wed, 15 Apr 2026 23:37:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:37:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 23:37:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528901158bfe90ffd940d7f0aa9bbdb73b0d6bf931e010821db19992cbeaeec9`  
		Last Modified: Wed, 15 Apr 2026 23:38:24 GMT  
		Size: 60.2 MB (60180116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:555d1be2a5ae3f0954172e2431f189f0bd0da55d0518a73548b69f29ccf5dd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e123eb8da16a50cee91cf5a2e793c4649d9bc65afc02f47086d7753e6f47c9f3`

```dockerfile
```

-	Layers:
	-	`sha256:fe4922493f8eeca57d98c65b3755d7aa836450313341357668f2baa004b7bba1`  
		Last Modified: Wed, 15 Apr 2026 23:38:22 GMT  
		Size: 2.3 MB (2295979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4604b7d67a5b30169aeac70f79d6ecb9cdaaddec0b4771261ccb40079c5cdad`  
		Last Modified: Wed, 15 Apr 2026 23:38:22 GMT  
		Size: 9.0 KB (8953 bytes)  
		MIME: application/vnd.in-toto+json
