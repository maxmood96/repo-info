## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:2e2d7453cbc41c9a13f622e063de9e98c4dee58b850ea87bf62b10789a4aac8d
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
$ docker pull sapmachine@sha256:c51043df89eff56e9debc74fc4d8386ab9325b170dc12481d97e28b72c82ad7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88665433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf83ada190d27f59980d37dfa6e73e57940eadfc9ae04764bc5da4d8e8612dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:58 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:24:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87bf7b58804712d566754219d7689ee34ae64d43a4ef0bccd5f4cff5999eb06`  
		Last Modified: Tue, 17 Mar 2026 02:25:11 GMT  
		Size: 59.1 MB (59126913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d7dd300c9366b3266eb45c1c0e2e4c83143a50e3a0cd72e745c369922e385da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a7b242b6053299ae1782b6d255dde7024530eb109b2c33306e1a4c5bc31232`

```dockerfile
```

-	Layers:
	-	`sha256:c3ba76f957fe8a657a7ffc6651657746c2f049227f31c8d54c93e1fcd0cfc1b3`  
		Last Modified: Tue, 17 Mar 2026 02:25:10 GMT  
		Size: 2.3 MB (2296537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:103186896c1946bdc89ab6111b9310c26984b24331d8e7a6e175752e844d82db`  
		Last Modified: Tue, 17 Mar 2026 02:25:09 GMT  
		Size: 8.9 KB (8908 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:21b35c367dc3dd347dc8e6bb8abf6f38b138b9336a177a466dcd94bf926f64a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85671454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c208559a4393208d7b839b4c804a2c926ced12f64e9dc0314f619c809d0b23ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:30:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:30:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45624940fe6336283a0fa11f26f1f8381cff89cebba6bd718ab0c7cf11739b85`  
		Last Modified: Tue, 17 Mar 2026 02:31:13 GMT  
		Size: 58.3 MB (58282429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:29e83adcfea25c8be3510184836bf782b265a3d5aa6dc0330d0370eb5e8aae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea700adac79d7f1081b84beaa116f09559883c2cc0fb70e3f785147bfcc4a30`

```dockerfile
```

-	Layers:
	-	`sha256:0950080fe4caf64caee88c032548100ecb17a40a77abdc9e77867f63860e2575`  
		Last Modified: Tue, 17 Mar 2026 02:31:11 GMT  
		Size: 2.3 MB (2296209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e804242ef99ad186f8bfc5202ceef32c823ea53807e640b65cabf20b17cb0d64`  
		Last Modified: Tue, 17 Mar 2026 02:31:11 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4f1a51f18c33f7b0c1dbe93eedba829b57ecb86c5e9b84e8c11f1727c33a51b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94633435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db428225ff40e72ffe9badd1fc7db9484ab0632fa3b2a1f4bfc622811e37a7bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:47:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:47:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 09:47:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461fe905c5e7d722e9833e105d4db1b8928ec6d4c89a312c1596c142c7212947`  
		Last Modified: Tue, 17 Mar 2026 09:48:13 GMT  
		Size: 60.2 MB (60179987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a0405dddf0e5ce713073dc30d4e04a5163eaa67fb4a3cf5af641e3b7ed5cfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464efd38cb2f864d2f279ee8dabd338bd82fc630f2ec2b2704afaf2a16de532d`

```dockerfile
```

-	Layers:
	-	`sha256:813551a16c02d5195b4a34cefc9d7fddef1eb523e46e5f2940f2f51c7058687e`  
		Last Modified: Tue, 17 Mar 2026 09:48:11 GMT  
		Size: 2.3 MB (2295979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdddcf985ec05a1a7d8d8f6d5c4a50886d020a73d545a000390c7f698d3132a`  
		Last Modified: Tue, 17 Mar 2026 09:48:11 GMT  
		Size: 9.0 KB (8953 bytes)  
		MIME: application/vnd.in-toto+json
