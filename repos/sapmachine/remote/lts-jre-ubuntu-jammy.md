## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:be90b701d4d627c6c508fe0e57c018601fb8ee52aca40050046054ac5d027863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1904bde71f4d4db577396ba34386562032a9ebbc0a7fbe014c9edabe63aa4d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86885291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073a4521b37efe0206bc1c7cff0c2fdf394ebedbb0a93dbfe11a6bde72adad9c`
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
# Tue, 17 Mar 2026 02:24:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:24:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d07faf37dfc7bfdd3ed631b9f81b6b5fac38081defda59abb566566497678e`  
		Last Modified: Tue, 17 Mar 2026 02:24:29 GMT  
		Size: 57.3 MB (57346771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08688f26ac1ec21936814a4cbfc4db125b76981c699e27563bdd1b6fd97fb386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2563822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be059ba6c716639d306d6ff3f3851ec598cd3709f0930e2b4e921f29649029b`

```dockerfile
```

-	Layers:
	-	`sha256:1a61e2290933b5bff96e9b40983a333c036449e3a83dc327c70394967fc592dd`  
		Last Modified: Tue, 17 Mar 2026 02:24:27 GMT  
		Size: 2.6 MB (2553733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d650eb21eba8f450bdf47a4a7f17816ae5fc358c205d4bb9b4b35cd290ea398`  
		Last Modified: Tue, 17 Mar 2026 02:24:27 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5ab0afb449cf57203e8a8d261cb2317e34790863095f9ba1fc334c3ad3263887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83650225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9559210f71646c12694b3d1583d835b6fbc2828c1734904091be7f33ded53e`
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
# Tue, 17 Mar 2026 02:30:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:30:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3ea48eb5bb9dab6fa2dfae6ae630408ac3535e604c76e7403f264b9aff8e23`  
		Last Modified: Tue, 17 Mar 2026 02:30:17 GMT  
		Size: 56.3 MB (56261200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f7b24629de70b88d096466924eec71753ca09dfc4a7dc476f4411cda77dabda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2563701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed6c8bec19426208c7ffeba28146089a118ad2c3b9dc7aea1122bb5ec095e6`

```dockerfile
```

-	Layers:
	-	`sha256:042b7cbd0cb5851802d3eaa64bcffe558adc036f85ee860d9833879a8cb9a623`  
		Last Modified: Tue, 17 Mar 2026 02:30:16 GMT  
		Size: 2.6 MB (2553460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27543941d89ebae6014324336d4080c2938ec64cef88d853074462f1bcaa1f2`  
		Last Modified: Tue, 17 Mar 2026 02:30:15 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d9be10fc370bdc871c529d14f33bd04355e65b8321ba487c5ff3015a00250c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92677335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df246d225ad02dc2280127d17b29d85bf365a847d5cfafd2c041ea4ea382d03`
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
# Tue, 17 Mar 2026 09:39:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:39:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 09:39:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63477c9848bd0da8386d704fd6033635ed22329385e0c03b8ec4ea30b667fef`  
		Last Modified: Tue, 17 Mar 2026 09:40:21 GMT  
		Size: 58.2 MB (58223887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:84c84c1535ceb18dac739d10a0780c20040de8dc8845a615e6c13b1586740861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71d30e9222138a9304ded5065e210d981c1b1f3c94c08f09a859e0d184f0d16`

```dockerfile
```

-	Layers:
	-	`sha256:2e44d4ecadfefbf6022406c1b1b71cdad969add8214ca0e6a2a0f91ee110640c`  
		Last Modified: Tue, 17 Mar 2026 09:40:20 GMT  
		Size: 2.6 MB (2552659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fc81630cbf94cd753bc2277ffb3fc2850550fe3352134a6e9aefb091b08769`  
		Last Modified: Tue, 17 Mar 2026 09:40:20 GMT  
		Size: 10.2 KB (10157 bytes)  
		MIME: application/vnd.in-toto+json
