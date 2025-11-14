## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:1b0d3e37c701e5706be8a08b5ce6e7d9790cec6d2d19ecc454a95c9784bc85ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:675895a0ed85e27aa2736129e4d84cf004bd7f0f08e09fbe34d7f3012ed7578a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89384709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961393fcaf024514e7b6e1d165a5bc74f7b916ce56719bf9d577e71742a423e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:03 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:39:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7e1c1d22357188e696f2105c0d752f28a6e1ae4bb19558a77ef18aa3d8632f`  
		Last Modified: Thu, 13 Nov 2025 23:39:30 GMT  
		Size: 59.8 MB (59847911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:487c2ebab0f985a4601fc4ae0436dea1016e9dba68dbc5e2d076235956ebad55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74af9e1871b71eb2ffe7dd4da0430220cac49a3f00230ad405cca68f329ed1fe`

```dockerfile
```

-	Layers:
	-	`sha256:9fcefc4eefc707b020a07f4d203a1122eb9f7702088d79b2c62e3846bd715cab`  
		Last Modified: Fri, 14 Nov 2025 01:10:49 GMT  
		Size: 2.5 MB (2544889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd70bdb5ddab7f4be53178babb93b347a621c301eff4ad87529e72c6414274ae`  
		Last Modified: Fri, 14 Nov 2025 01:10:50 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ad1b10c3f189daca8ed17596220c602ee1fb55d8abd1f4bab91130666663c792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86368982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d0cdeb6d5c42e97693fd54c2c60b1948222cce02842a8467ec3d1479c38dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03edf874b3661c7dc8f8121ccb1b8b64bc80a988721353377c953a60f4750d34`  
		Last Modified: Thu, 13 Nov 2025 23:38:39 GMT  
		Size: 59.0 MB (58985105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4ca515aefea7623e3f531f662e3ee1f9e817cd3aff6a8d83f74502941cf2cf1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e54fd64d98c0e86ba4993c33d4c78929746719f23bdbb0b52de3dda680c974`

```dockerfile
```

-	Layers:
	-	`sha256:c24d3367252450a80662a4fdc549ea0a55b37d856a9c4f31884103817f1d73e1`  
		Last Modified: Fri, 14 Nov 2025 01:10:54 GMT  
		Size: 2.5 MB (2544571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432cbb85198ccf68cf3f8aab471031ad8b255852a17397da3d92aa79ae779235`  
		Last Modified: Fri, 14 Nov 2025 01:10:55 GMT  
		Size: 8.9 KB (8873 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9d12910c2697a05bd33b499aeaca05677fa25409dea95e6e14220ddc88eb814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95408707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0d3301063fcd3b86044a7eb333c4743c43d2842a3909dec00d4efb21513cf1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4232fb460c9a1645644b37cf3d2c15a5e982e97e5b26bfa1c6911111304a3`  
		Last Modified: Wed, 22 Oct 2025 11:59:46 GMT  
		Size: 61.0 MB (60961918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:41e7db929d40c1af808749a5bbdd740eaeab13b30e969c1ea72c235c0aa8a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb5f0c9d2b1532966c9a81c4ca325108fc7c26872553d2f98d61ddf93c31819`

```dockerfile
```

-	Layers:
	-	`sha256:e41277f8316ec07b1144da6f4f17208dfd59712d7f660f1c4af64c49963a8f35`  
		Last Modified: Wed, 22 Oct 2025 15:08:27 GMT  
		Size: 2.5 MB (2543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffed7cfdc8214db27f990ea297e3b0555d5ed5bf7d328a8140f554b8e945cd2c`  
		Last Modified: Wed, 22 Oct 2025 15:08:28 GMT  
		Size: 8.9 KB (8855 bytes)  
		MIME: application/vnd.in-toto+json
