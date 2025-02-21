## `sapmachine:21-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3032c74d67b3843583e05667313e06f089a9efcc33a95fef37f1b4f7d6875586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a76ff51c6a439a32f955a03512ae0291c321a2cba776f5f3cf6c16456c217718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244182178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662af7b971d3020359837877a7b0908c15cc56c59d8ca5ba318cc3303bf9b701`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4c786965c6dffbde9a8be0bc639cb122e4e020d2e2d1796586ebe383849159`  
		Last Modified: Tue, 04 Feb 2025 04:49:26 GMT  
		Size: 214.6 MB (214646237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4120b6a11d75e4aba61ebbaea1112c436a7f032cb1f29f1bec4288b53a34e078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0705b10187b92ec5727a4556abf6e2ca166528284ac0f877ef5f07bcf775617`

```dockerfile
```

-	Layers:
	-	`sha256:90f6236210127c9082daf9a7daf84c378d76957e158dd7abbf0654f88f8daf74`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 2.5 MB (2494735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034e9bc1224821adc24e72c18303b29c6e3248f7642bf0c10fe2b77504333f20`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 11.4 KB (11444 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9da1346be495a8a040fcc4763d618e97d2699165d1cd1843d18f341187001f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240199709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2aeb619bfa3a8f5a55d26501277af9baad21a2e399edee4cc4963a54fc46cf`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd040793c136137b4fa7f4616d0cb835917a65d18f13fb8bc8ad13ba00aa424`  
		Last Modified: Tue, 04 Feb 2025 15:29:47 GMT  
		Size: 212.8 MB (212841527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4bfe3490ea3ef83d6af31ba90ef23e2d288d870c479a2101972012c9bbaef4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2506158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2fc19dac18d2da74e81f10f8d55d586cfe5dc770e2ffa7bd303e5b27341781`

```dockerfile
```

-	Layers:
	-	`sha256:3d9fc8a2bbf644b31ae9384987e1c9cbe16e9869c014910b85c1a34cd3b40ce9`  
		Last Modified: Tue, 04 Feb 2025 15:29:43 GMT  
		Size: 2.5 MB (2494513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fb302a5c364952ab207360f6ac992f825d586440b7824a80d0d37fa170e706`  
		Last Modified: Tue, 04 Feb 2025 15:29:42 GMT  
		Size: 11.6 KB (11645 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:45cf35892fcb7c024eebaa570640fbed7bc9b4785f7186ba2136ff65ca8d84cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250394277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430dfc307312d9e7077f709ce287bb9899ca7c13281b61d5fcee6e27d55dbec`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe755ab69d41c73a2df0436676d7a55400e7c102649efbe5eda8adcc4c2cfd3`  
		Last Modified: Tue, 04 Feb 2025 14:41:38 GMT  
		Size: 215.9 MB (215946342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:71386d7c0095a6c59d25b2e7eb4715a26d69a7a82d581b50552bd600cdbb3a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e37a94c2a832418210bf1a6577fbf7b2e02696066fe9581d27afe45806cf2a`

```dockerfile
```

-	Layers:
	-	`sha256:d939711828e3db0c0a33ef4fd4da6c6744a85dd072b0959216f518dfef7e6dea`  
		Last Modified: Tue, 04 Feb 2025 14:41:29 GMT  
		Size: 2.5 MB (2496818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce2f81da5f42d5139360b46a57901f318a68fa506043689abeb6ff6501a7b74`  
		Last Modified: Tue, 04 Feb 2025 14:41:29 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
