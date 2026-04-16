## `sapmachine:25-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:03de8b3789246d5e4dceef3311acecbbe2300938d06fb23b55f87848c0effbed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:be82054fee018a21447caa06c0f4d7b4aa986ae1de7568f12fb387a246949ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251186208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319ce464587662766aabc067d4f7bb9c893db6bf714e3df1e4c0c9ae150c07fb`
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
# Wed, 15 Apr 2026 20:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7261e992e549107f003743f60a1ec623fc178881e63f5e0d7dd4716cbbb2117d`  
		Last Modified: Wed, 15 Apr 2026 20:58:41 GMT  
		Size: 221.5 MB (221453230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d7c20fe63c9fa448de00eae620e1f90137cb1266fe82811c7299bf9d7baad4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caadfdfc92b5260adafd89e45fb21b79d1fc289d10d1ed9c682f8c8dfae06f4`

```dockerfile
```

-	Layers:
	-	`sha256:6da8335c776f62bccccf444da808cde569c24f0e2425be4752b27bb074d16e54`  
		Last Modified: Wed, 15 Apr 2026 20:58:36 GMT  
		Size: 2.6 MB (2598827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8bc5845f731297eb6a0975259ff01a86fc33999f054ca0c5b8cd64d2e7b61b`  
		Last Modified: Wed, 15 Apr 2026 20:58:36 GMT  
		Size: 14.8 KB (14842 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c84675fb223a8012ee1c91f6297c447258e9111463acc6e030a43af08aabffed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248142292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d14caf979b30753f2eca85c0820343740a1db1d6566c6b9027c517ab0872d`
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
# Wed, 15 Apr 2026 21:07:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:07:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8551e8c16388e78ab94c5d6f978fa6399edbcb20e0e40b0012046dd6e9617d`  
		Last Modified: Wed, 15 Apr 2026 21:07:57 GMT  
		Size: 219.3 MB (219266507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e62a85fb2912e05c96671017b565d6ee46f729d8d06daa739fa836bc8d75e292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6244d08fa1aa72abe05058dbfd03188bd2f01a4e8b81b2e89b1043372ca6697a`

```dockerfile
```

-	Layers:
	-	`sha256:8106ee95e68a6d16b6e20061212f0e120ff74f3db162497aea631d4e321bce2c`  
		Last Modified: Wed, 15 Apr 2026 21:07:50 GMT  
		Size: 2.6 MB (2599520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb6c19c06038872aaeac6bdf8a14da3524f94d1c046a328c252ee3135d164bf`  
		Last Modified: Wed, 15 Apr 2026 21:07:50 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8333387541168f14546146d7cdb2f5a4095c0e8aeacb3ee4e52dbf25c60d2284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256666228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c909133e2acad36f332db087ea38da5446853aa5d48ea6e6869bd0aba2054f30`
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
# Wed, 15 Apr 2026 23:26:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:26:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:26:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f9b6b8049499a8cb46748347013393bd725969caa313978b9f1d5d15879e22`  
		Last Modified: Wed, 15 Apr 2026 23:26:53 GMT  
		Size: 222.4 MB (222352050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:46a8e470d44e24cc1c1a0ebf9c6ba54b11db6587b32253d1c30254f4639365b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d77db00c8220cf1b25123163332c44997d848c7b7e90a9096c76cc87d56b7e9`

```dockerfile
```

-	Layers:
	-	`sha256:ef8ffe0f270ee6fdbff6e136bb6786fbaa08bfd2797e073410b33ce8093a4093`  
		Last Modified: Wed, 15 Apr 2026 23:26:49 GMT  
		Size: 2.6 MB (2595851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825e56a05af965fdd3a6333ddb5109b5e68ccf281a28710faf0b533879404ac5`  
		Last Modified: Wed, 15 Apr 2026 23:26:48 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json
