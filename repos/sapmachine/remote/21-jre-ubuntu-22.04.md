## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:1254c2725f813c29ef69319cad1361aed9b035601872bcf59dc8cf4080bfefce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:69e244f05f9584b91ad6800962c7f3e6f53086a2488375f3d29eae2c163d2664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89385208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eba61e92866e6f713f9919957dcd32ef7bf1e2d22c169f69b7a40ebd74101fa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:43:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f5a8a60327f19b1e9230ffee47ab076334b3d78dabb41b312caea8d24cdcff`  
		Last Modified: Thu, 15 Jan 2026 22:44:01 GMT  
		Size: 59.8 MB (59848541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4007788a68ddf14799d213e1a38c2d1f1a2675a32eeb53023250c4d0112df632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816e0564541e577b39cd7f845ca17ec198787aba23a344335ad56149f7fd85d7`

```dockerfile
```

-	Layers:
	-	`sha256:23d54bfbc124497a97b88b8801c08400ebbd47bcafad600d3fc09398868bb4cc`  
		Last Modified: Fri, 16 Jan 2026 01:12:38 GMT  
		Size: 2.5 MB (2544901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40263de42f1ff10ab4bcd48d9d60a3f0b77c7401cdf777c302d70aa4d636ea40`  
		Last Modified: Fri, 16 Jan 2026 01:12:39 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7a4af16dac36ae494acef4964fe0cb895920ec7ef8be07527f12ed05d92dafe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86365076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98984a9523bc4748c123d01f91d6e02b5c986e2b82954facb9761d8f55192c58`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:47:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:47:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:47:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647a9a3e66b227a7433e231102ab6a1cf6ea10c3002a477875dcd3b6f8cb423`  
		Last Modified: Mon, 19 Jan 2026 07:10:01 GMT  
		Size: 59.0 MB (58981579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3159defc8cc9f46121c78bc04dab34dad8a293fe69bd137566b9d6c7d749362d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1a70010cf9edd993bc158eda00df4cab61db858f58649226d36c011ff4493e`

```dockerfile
```

-	Layers:
	-	`sha256:e730b1c5122958d3bc079621b39e372b0dc67106840bee0b07ef7f0e5737e433`  
		Last Modified: Fri, 16 Jan 2026 01:12:43 GMT  
		Size: 2.5 MB (2544583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0760d3cc646635fee81437b503dfad3ded55f22e8ca8f971d2f79672e46df087`  
		Last Modified: Thu, 15 Jan 2026 22:47:15 GMT  
		Size: 8.9 KB (8873 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:47b0cbdc6b245efb5fc89f024c30690dc0e9fffa0b8039abb1bf9d751fc2f496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95408692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c09281a6fd8951e759ddbadab7d74caa5c493bf6c3fb6c2d4ede8af05e3788`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:39:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:39:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 23:39:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d3d85050a56bb1ade868d514dde479aa8159c59cdb68cd74829ab26973f51`  
		Last Modified: Thu, 15 Jan 2026 23:40:24 GMT  
		Size: 61.0 MB (60961730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2059eb2eda566bc280b62e75b425d24dd54ce671beb0fad96e71406d5dfdaf5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c000a94581efd8674096d2d1dafdabb71429a677f4bc9c32e68b9494391c5f61`

```dockerfile
```

-	Layers:
	-	`sha256:48a700882469654e3063fd60336f53a32a538f77bb728cbc5078ce3694f7978d`  
		Last Modified: Thu, 15 Jan 2026 23:40:23 GMT  
		Size: 2.5 MB (2543016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e40b43337067a555c6ffec69a8c06ca91bc570489e746d845ae647e4565959`  
		Last Modified: Thu, 15 Jan 2026 23:40:22 GMT  
		Size: 8.8 KB (8812 bytes)  
		MIME: application/vnd.in-toto+json
