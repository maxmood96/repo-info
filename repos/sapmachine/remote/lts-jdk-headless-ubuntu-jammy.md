## `sapmachine:lts-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a166cc08c740524f9b52081beb7bdbfeef40eebab5934fe5ed27a924f73442e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1a83565fc6e8b213b4ea921baf2ee2bc013d8988a709ba01fbc335180e2954b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250304630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ac019a46dca8b8eb12be8754f115879ccf1cbb20f6cbd5aeea2655ac7e5255`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:21:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed30dac4c179764ea49ea2ef8a2d2f8ea63096e0703c2ff9bcb92de1d2b6d4a`  
		Last Modified: Fri, 15 May 2026 21:21:45 GMT  
		Size: 220.6 MB (220567946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1c70ea4cb13e789a9864ffc39672a38ab4ac85bcf02a1c2aa7fed18020836bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8658ef796d6180cbd1c5ebc581f175aa6ec8281c1cee41fc98c0c07b8c1ee389`

```dockerfile
```

-	Layers:
	-	`sha256:d8e8543dabb4b9295e20136040e5a2d6688779005696567d402ab9428583db2e`  
		Last Modified: Fri, 15 May 2026 21:21:40 GMT  
		Size: 2.4 MB (2370832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68d8f8bf4fd89f17d7b8ac9dc50e72b359804ebb3bdaa64dcfa500295bba64f`  
		Last Modified: Fri, 15 May 2026 21:21:40 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ddac859e39d21bf00beb87f90466fc9104841056be8c35e85f68b0302fb85310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245924158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb24449c18e02265edd3fa2017bcbdb46d6df2509fabc28dab66f95636430129`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:21:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b4ffe5ee01c5d4cd7c53c0f10a21ce0179504cdc7725a780d2e4d2ce59b3e4`  
		Last Modified: Fri, 15 May 2026 21:21:44 GMT  
		Size: 218.3 MB (218317535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:45a9da12ed4d733f276f3e225e695f748b4102b624205f42c81127aea2ab0e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da69d7c72d89366cd4b553b6edd4871503376cb156ac82de12e60d1df6ad004d`

```dockerfile
```

-	Layers:
	-	`sha256:8aa6e62604b88a6c891fc6dab5790221037a9296c4cfa57726a2ac82055b508b`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 2.4 MB (2370525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b440f002ef135bfa840661973e5ed5e80960a2eac1411be87528680d5814c6a`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 9.7 KB (9712 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ec595a9109c4055aa9f98ad1572069810c6ffaf8500e8168de245eb1a5dee1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255675408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7217c9f51a2a16029c5b45d68363b8afceba2ecff7f569e86c2a3a2689df453e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:36:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:36:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:36:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5338f709b2d85d4fb059959fa02e2b2a289364c3289ae98f3b4b377df4ef08c`  
		Last Modified: Fri, 15 May 2026 21:37:00 GMT  
		Size: 221.0 MB (221028688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38d35fab892797af9cd8014b292e9adb3090678ffbc97552042986593369e030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76eb9005bb1b626763f39375c3be8f60bc4db748e28e322f0f3e2255764d7243`

```dockerfile
```

-	Layers:
	-	`sha256:dafc5d026d42fdfe8f868cf3ec06f95cae3443d3dee6c70a1346fde60933848e`  
		Last Modified: Fri, 15 May 2026 21:36:56 GMT  
		Size: 2.4 MB (2367722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2a5eb7f5ea3c642d9676d8d5f3843a571df695416fdbab1db436ae8a999bf6`  
		Last Modified: Fri, 15 May 2026 21:36:55 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.in-toto+json
