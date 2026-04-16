## `sapmachine:26-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:6dc5d807f990e7a71e78c1f78fc19c0289b62115eaebd59dda2fa6c65dfb4e3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:95406e8155b7b0cdd9716b1715000f06e4fb28b9e822dc14737c7acb0ca759d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254492189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3a38ddeb5496c7405a0d71db1a906b3e5095442cb6d371712d7b76010e7baa`
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
# Wed, 15 Apr 2026 20:57:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:57:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:57:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584eef762f3af2500f37ea503ca7f142671f1e2e7af227d5f1e231dffbe1f2e`  
		Last Modified: Wed, 15 Apr 2026 20:57:57 GMT  
		Size: 224.8 MB (224755691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:072f3b1922ece8a5fc35ab19f290e9ef6ebe13f1c96c25c4c95910264b57b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbef691cafd331496cfa6871f73fe9153a9a0e7932f5cb156b3658994037c255`

```dockerfile
```

-	Layers:
	-	`sha256:11ca1554c92e05ff34b7e543b3712e6ccd097e32f06fd84f8ce30251c9a02570`  
		Last Modified: Wed, 15 Apr 2026 20:57:52 GMT  
		Size: 2.4 MB (2367547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4e7f47de42f9656bc26279bc59fdf26acc7abc11fef929dd288203fb08a370b`  
		Last Modified: Wed, 15 Apr 2026 20:57:52 GMT  
		Size: 8.8 KB (8845 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fef5c13e67d09eee391bddc4b8b5fc1c0375b9f98ad196356627250dfa17b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250174688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00f1491118322a5c7e67b9722fffe4d0195add334a78c75c35064dbdcbc5ef2`
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
# Wed, 15 Apr 2026 21:07:03 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:07:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50d7904b0bfcf2b8e040e4c74cae9b96bfe01b0b54da6dc4cbcd74fd375306a`  
		Last Modified: Wed, 15 Apr 2026 21:07:28 GMT  
		Size: 222.6 MB (222568145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c47e5c7a597ff1d12c380c881454229be0f912c982c0328fee5dcaa77931d984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df1427bc1c608bd9a151ae87b6c863a4616070579922ca2f59c5c39d6a48c35`

```dockerfile
```

-	Layers:
	-	`sha256:9fee3cf23169c45a52d8e168ccd9f9158325538e64249dd8d6f146aff49c8f0c`  
		Last Modified: Wed, 15 Apr 2026 21:07:22 GMT  
		Size: 2.4 MB (2367216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d7bcd2464c75c66e57b6704f2f28fa93869dfb8bc08f3abdb78de1eca9e325`  
		Last Modified: Wed, 15 Apr 2026 21:07:22 GMT  
		Size: 8.9 KB (8948 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

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
